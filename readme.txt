;Example 1
2+3*5

;Example 2
a = 2;
b = 3;
c = 5;
x = a + b * c;

;Example 3
angle = deg2rad(39);
a = 19;
b = tan(angle) * a;

;Example 4:
hex("7E5");

;Example 5:
bin("11111100101");


;To add this plugin to Npp context menu edit and add next lines to file %appdata%\Notepad++\contextMenu.xml
	<Item FolderName="PlanetCNC" PluginEntryName="PlanetCNC Tools" PluginCommandItemName="Expression" ItemNameAs="Calculate Expression"/>
	<Item id="0"/>

	
;List of expression functions
if			- Conditional statement					Usage: if(1, print("Yes"))
for			- For statement							Usage: for(i=0, i<10, i=i+1, print("Loop", i))
exec		- Executes multiple expressions			Usage: exec(print("One"), msg("Two"))
exists		- Checks is value exists				Usage: exists(_param)    = 0
notexists	- Checks is value does not exists		Usage: notexists(_param) = 1
nop			- No operation (returns zero)			Usage: nop()           = 0.000000
nan			- NaN value								Usage: nan()           = nan
def			- Sets default value					Usage: def(nan(), 100) = 100.000000
defnz		- Sets default value	not zero		Usage: defnz(0, 100)   = 100.000000
abs			- Absolute value						Usage: abs(-123)       = 123.000000
sqrt		- Square Root							Usage: sqrt(9)         = 3.000000	
sqr			- Square								Usage: sqr(3)          = 9.000000		
sin			- Sine									Usage: sin(0.524)      = 0.500347	
cos			- Cosine								Usage: cos(1.047)      = 0.500171		
tan			- Tangent								Usage: tan(0.785)      = 0.999204
asin		- Inverse sine							Usage: asin(0.5)       = 0.523599
acos		- Inverse cosine						Usage: acos(0.5)       = 1.047198
atan		- Inverse tangent						Usage: atan(1)         = 0.785398	
atan2		- Four quadrant inverse tangent			Usage: atan2(1,1)      = 0.785398
pi			- Pi constant value						Usage: pi()            = 3.141593	
rad2deg		- Radians to degrees					Usage: rad2deg(3.141)  = 179.966043	
deg2rad		- Degrees to radians					Usage: deg2rad(180)    = 3.141593	
e			- e constant value						Usage: e()             = 2.718282	
pow			- Power									Usage: pow(2,3)        = 8.000000
exp			- e raised to the given power			Usage: exp(2)          = 7.389056
exp10		- 10 raised to the given power			Usage: exp10(2)        = 100.000000
exp2		- 2 raised to the given power			Usage: exp2(2)         = 4.000000
log			- Base e logarithm						Usage: log(2)          = 0.693147
log10		- Base 10 logarithm						Usage: log10(2)        = 0.301030
log2		- Base 2 logarithm						Usage: log2(2)         = 1.000000
rand		- random value							Usage: rand()          = 0.100845
inc			- Increases value (value,limit,default)	Usage: inc(5,10,0)     = 6.000000
dec			- Decreases value (value,limit,default)	Usage: dec(5,0,10)     = 4.000000
min			- Minimum								Usage: min(4,6)        = 4.000000
															min(4,6,3)     = 3.000000
max			- Maximum								Usage: max(4,6)        = 6.000000
															max(4,6,3)     = 6.000000
round		- Round to nearest integer				Usage: round(0.56)     = 1.000000
															round(0.56,1)  = 0.600000
roundup		- Round up/down to integer				Usage: roundup(0.56)   = 1.000000
															roundup(0.56,1)= 0.600000
floor		- Round to nearest value with decimals	Usage: floor(0.56)     = 0.000000
ceil		- Round up to integer					Usage: ceil(0.56)      = 1.000000
trunc		- Truncate to integer					Usage: trunc(0.56)     = 0.000000
center		- Compensate hysteresis					Usage: center(0.3,0.2) = 0.2
															center(0.1,0.2) = 0.0
centerex	- Compensate hysteresis					Usage: centerex(0.3,0.2,1.0,0.8) = 0.044955
															centerex(0.1,0.2,1.0,0.8) = 0.000000
															centerex(1,0.2,1.0,0.8) = 1.000000
															centerex(0.9,0.2,1.0,0.8) = 0.619110	
not			- Bitwise complement					Usage: not(10)         = 4294967285
and			- Bitwise AND							Usage: and(10,3)       = 2
or			- Bitwise non-exclusive OR				Usage: or(10,3)        = 11
xor			- Bitwise exclusive OR					Usage: xor(10,3)       = 9
nand		- Bitwise NAND							Usage: nand(10,3)      = 4294967293
nor			- Bitwise non-exclusive NOR				Usage: nor(10,3)       = 4294967284
xnor		- Bitwise exclusive NOR					Usage: xnor(10,3)      = 4294967286
shl			- Bitwise shift left					Usage: shl(10,2)       = 40
shr			- Bitwise shift right					Usage: shr(10,2)       = 2

lnot		- Logic complement						Usage: lnot(1)         = 0
land		- Logic AND								Usage: land(1,0)       = 0
lor			- Logic non-exclusive OR				Usage: lor(1,0)        = 1
lxor		- Logic exclusive OR					Usage: lxor(1,0)       = 1
lnand		- Logic NAND							Usage: lnand(1,0)      = 1
lnor		- Logic non-exclusive NOR				Usage: lnor(1,0)       = 0
lxnor		- Logic exclusive NOR					Usage: lxnor(1,0)      = 0

eq			- Relational equality					Usage: eq(10,20)       = 0
ne			- Relational inequality 				Usage: ne(10,20)       = 1
gt			- Relational strictly greater than 		Usage: gt(10,20)       = 0
lt			- Relational strictly less than			Usage: lt(10,20)       = 1
ge			- Relational greater than or equal to	Usage: ge(10,20)       = 0
le			- Relational less than or equal to		Usage: le(10,20)       = 1

hex			- Converts string to number				Usage: hex("7E5")      = 2021
bin			- Converts string to number				Usage: bin("11111100101") = 2021

sleep		- Sleeps n milliseconds					Usage: sleep(100)

datetime	- Current time (seconds since 1970)		Usage: datetime()              = 1616502112.792
year		- Year from DateTime value				Usage: year(1616502112.792)    = 2021
month		- Month from DateTime value				Usage: month(1616502112.792)   = 3
day			- Day from DateTime value				Usage: day(1616502112.792)     = 23
hour		- Hour from DateTime value				Usage: hour(1616502112.792)    = 13
minute		- Minute from DateTime value			Usage: minute(1616502112.792)  = 21
second		- Second from DateTime value			Usage: second(1616502112.792)  = 52
millisec	- Millisecond from DateTime value		Usage: millisec(1616502112.792)= 792


