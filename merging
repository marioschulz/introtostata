clear
set mem 500m
cd "/Users/Mario/Desktop/Stata_Training_2"
use "/Users/Mario/Desktop/Stata_Training_2/CPDSI1960-2011Stata"
keep if year < 2001
replace country = "AUL" if country == "Australia"
replace country = "AUS" if country == "Austria"
replace country = "BEL" if country == "Belgium"
replace country = "CAN" if country == "Canada"
replace country = "DEN" if country == "Denmark"
replace country = "FIN" if country == "Finland"
replace country = "FRA" if country == "France"
replace country = "FRG" if country == "Germany"
replace country = "IRE" if country == "Ireland"
replace country = "ITA" if country == "Italy"
replace country = "JPN" if country == "Japan"
replace country = "NET" if country == "Netherlands"
replace country = "NZL" if country == "New Zealand"
replace country = "NOR" if country == "Norway"
replace country = "SWE" if country == "Sweden"
replace country = "SWZ" if country == "Switzerland"
replace country = "UKM" if country == "UK"
drop if country == "Iceland"
drop if country == "Luxembourg"
drop if country == "Portugal"
drop if country == "Spain"
drop if country == "Greece"
rename id country
sort country year
save "CPDSI1960-2011StataMODIFIED.dta", replace
use "CWS_data_extended_KOR"
sort country year
drop if country == "KOR"
merge 1:1 country year using CPDSI1960-2011StataMODIFIED
save "CPDSI1960-2011StataMODIFIED_mergedwith_CWS_data_extended_KOR.dta", replace
