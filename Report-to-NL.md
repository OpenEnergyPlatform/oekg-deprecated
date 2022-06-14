
# Report to NL

⚠: This file is partly auto-generated from PDF-annotations. Do NOT edit it manually!

The file is created from an annotated version of the report and contains some manual regex-hacks in order to strip all the annotation-metadata. There is no pipeline for this conversion (yet), so this file is for viewing only.

## Notation

All sentences shall be decomposed into structures similar to RDF-triples (SPO), but shall be remain relatively close to natural language. A little like Manchester Syntax.

### Formating

Bullet-points at the same indentation level shall be considered as being attached to the same node.
A dedicated notation for **reifikation** is missing currently.

- `classes` are formated as **bold**
- `individuals` are formated as *italics*
- `properties` are written in snake_case

### Indicators

- `content-start` is just a meta-data snippet in order to keep excerpts in the right order (Sorting is still a TODO)
- `🟢🟡🔴` indicates a basic progress-meter
- `EOS` stands for "end of sentence" and is needed in the PDF-annotation due to a minor rendering issue
- `C0000000000000000U0` are unique identfiers in the PDF to directly jump to the annotation 

## Sentence excerpts

### C20220613195140U0 🟡

content-start: 38784 

> dass dies für den Energiebereich eine Klimaneutralität und erneuerbare Vollversorgung bedingt. 

Assumption
- scoped_to **sector** energy
- states scope
	- is_a Klimaneutral sector #OEKG/add-translation 
	- has_supply erneuerbare Vollversorgung #OEKG/add-translation 

### C20220613195148U0 🟢

content-start: 38888 

> Szenariojahr 2030  besteht für Deutschland zudem das nationale Klimaziel, die Emissionen in Summe um -55% bezogen auf 1990 zu reduzieren und im Rahmen des Klimaschutzplanes feste Emissionsbudgets für die einzelnen Energiesektoren festzulegen  (BMUB 2016). 

Target
- is_a national target
- scoped_to temporal-region 2030
- scoped_to spatial-region Germany
- contains **emmision decrease**
	- quantified as 55 %
		- is based on reference temporal region 1990
- contains **fixed emission budget**
	- scoped_to sector
- EOS

### C20220613195205U0 🔴

content-start: 39655 

> Aufgrund dieser Heterogenität zwischen Statistik und Modellierung werden in der Studie die modellendogenen Ergebnisse  2030  nicht  auf  die  beiden  Sektorziele  Industrie  und  Energiewirtschaft aufgeteilt. Stattdessen werden die Emissionen der Strom- und Prozesswärmeerzeugung sowie  für  Fernwärme  und  Industriegebäude  immer  zusammen  betrachtet. 

Modellendogene Ergebnisse #OEKG/add-translation 
 - scoped_to **temporal region** *2030*
 - originating_from **sector target** Industrie
 	- is NO individual component #OEKG/find-conform-model
 - originating_from **sector target** Energiewirtschaft
 	- is NO individual component #OEKG/find-conform-model 
 - combination #OEKG/find-b-node-model
 	- contains **emission** 
 		- originating_from energy 
 	- contains **emission**
 		- originating_from process heat production
 - combination #OEKG/find-b-node-model  
 	- contains **emission**
 		- originating_from Fernwärme
 	- contains **emission**
 		- originating_from Industriegebäude
 - EOS

### C20220613195213U0 🟡

content-start: 40011 

> Der  andere Teil  des  Sektorziels  Industrie  (Emissionen  aus  Industrie-Prozessen)  wird  auf  Basis  der Klimaschutzszenarien  KS  80  für  2030  (und  KS  95  für  2050)  abgebildet  (Öko-Institut e.V.  und  Fraunhofer  ISI  2015). 

Modellendogene Ergebnisse #OEKG/add-translation  #OEKG/add-reference
- scoped_to **sector target** Industrie
- contain **emission** 
	- originating_from industry-process #OEKG/refine-class
- based_on **scenario** *KS 80*
	- scoped_to **temporal region** *2030*
- based_on **scenario** *KS 95*
	- scoped_to **temporal region** *2050*

### C20220613195223U0 🔴

content-start: 40249 

> Das  Sektorziel  für  dezentrale  Gebäudewärme  mit  72 Mio.  t  CO2  (ohne  Strom,  ohne  Fernwärme,  ohne  Industriegebäude)  wird  vereinfacht auf  Basis  der  Arbeiten  des  ifeu  im  Projekt  der  Agora  Energiewende  „Der  Wert  der Energieeffizienz im Gebäudesektor in Zeiten der  Sektorkopplung“  (IFEU  et  al.  2018) abgebildet durch das Szenario Effizienz². 

**Target**
- scoped_to **sector** *dezentrale Gebäudewärme* #OEKG/add-translation
- quantified_as 72 Mio t CO2
- excludes energy, Fernwärme, industrial buildings #OEKG/add-translation #OEKG/verify-translation
- depicted_by **scenario** *Effizienz*
	- contained_in **project** *Der Wert der Energieeffizienz im Gebäudesektor der Sektorkopplung*
		- created_by **institute** *ifeu* #OEKG/attribute-tense
		- part_of **project** *Projekt der Agora Energiewende* #OEKG/specify-predicate
- EOS

### C20220613194119U0 🟡

content-start: 38434 

> Es  wird  das  europäische  Ziel  einer  Reduktion  der  THG-Emission  bis  2050  um  95% CO2,Äqui. in Bezug auf 1990 betrachtet. 

**Target** #OEKG/attribute-implicit: political
- scoped_to **spatial region** *Europe*
- scoped_to **temporal region** *2050*
- aimed_at **reduction of THG-Emmission**
	- quantified_by 95 % CO2 Äquivalent #OEKG/add-translation 
		- based_on reference **temporal region** *1990* #OEKG/shape-predicate
- EOS

### C20220614081915U0 🟡

content-start: 38564 

> Hierbei wird unterstellt, dass noch 5% Emissionen im Bereich der Landwirtschaft und Nicht-CO2-Emissionen aus Industrieprozessen  im  nichtenergetischen  Bereich  verbleiben 

Assumption
- scoped_to **emission**
    - originating_from **sector** agriculture
- states scope
    - quantified_as 5 %

Assumption
- scoped_to **non-CO2-emissions** 
     - originating_from **sector** industrial processes
- states scope
	- part_of  **sector** non-energetic

### C20220614084658U0 🔴

content-start: 40693 

> Auf  der  anderen Seite gibt es von europäischer Seite Vorgaben, die Emissionen bis 2030 in Summe nur um -40% bezogen auf 1990 zu reduzieren1. 

Target
- is_a political target
- scoped_to spatial region Europe
- scoped_to temporal region 2030
- specified as emission decrease
	- quantified as 40 %
	- based_on reference temporal region 1990
- EOS

### C20220614104317U0 🔴

content-start: 42064 

> Ambitionsniveau  für  Europa  auf  -45%  etwas  erhöht  wird2.  Hierdurch  werden  dem deutschen Klimaziel vergleichbare relative Anforderungen für Europa vorgegeben, was zudem eine ausgeglichene Stromhandelsbilanz für Deutschland 

Target
- scoped_to **spatial region** Europe #OEKG/refine-class 
- specified as emission decrease
	- quantified_as 45 %
- EOS

Assumption
- scoped_to spatial region Germany
- Stromhandelsbilanz ist ausgeglichen
- EOS

### C20220614085623U0 🔴

content-start: 42307 

> Für Deutschland  wird  zudem  nach  dem  Agora-Kohlekonsenspfad  ein  Ausstieg  aus  der Kohleverstromung bis zum Jahr 2040 unterstellt mit entsprechend reduzierten Leistungen in 2030 (Agora Energiewende 2016). 

Assumption
- scoped_to spatial region Germany
- scoped_to sector Kohleverstromung
	- scoped_to temporal region 2040
		- quantified_as 0
	- scoped_to temporal region 2030
		- specified_as production decrease #OEKG/find-conform-model 
- based_on Agora-Kohlekonsenspfad #OEKG/refine-class 

### C20220614090145U0 🟡

content-start: 42518 

> Im Koalitionsvertrag 2018 der Bundesregierung (CDU et al. 2018) wird ein EE-Ausbauziel von 65% am Bruttostromverbrauch in 2030 definiert. 

Target
- is political target
- based_on Koalitionsvertrag 2018 #OEKG/refine-class 
	- created_by Bundesregierung 2018 #OEKG/refine-class 
- scoped_to EE-Ausbau #OEKG/refine-class 
- scoped_to temporal region 2030
- quantified_as 65 %
	- based_on reference Bruttostromverbrauch

### C20220603093347U0 🟡

content-start: 59204 

> Im Bereich der Industrieprozesswärme wird die Endenergienachfrage des BMU-Klimaschutzszenario  KS  95  für  2050  und  KS  80  für  2030  nach  Öko-Institut  e.V.  und Fraunhofer ISI (2015)] unterstellt. 

Assumption
- for data Endenergienachfrage #🏷OEO/_MISSING_TERM_ #OEKG/add-predicate 
- scoped_to **sector** Industrieprozesswärme 
    - based_on **scenario** *KS-95*
 	     - scoped_to **temporal region** 2050
    - based_on **scenario** *KS-80* 
	     - scoped_to **temporal region** 2030
