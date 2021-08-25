---
description: I campi di bit del subset Unicode (USB) vengono usati nelle strutture FONTSIGNATURE e LOCALESIGNATURE.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Campi di bit subset Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f0fa4791e62f397e62a99a78d41dbcdc67c55299a650b1bc78bea685205399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787991"
---
# <a name="unicode-subset-bitfields"></a>Campi di bit subset Unicode

I campi di bit del subset Unicode (USB) vengono usati nelle [**strutture FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) e [**LOCALESIGNATURE.**](/windows/win32/api/wingdi/ns-wingdi-localesignature)



<table>
<thead>
<tr class="header">
<th>bit</th>
<th>Intervallo secondario Unicode</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>0000 - 007F</td>
<td>Latino di base</td>
</tr>
<tr class="even">
<td>1</td>
<td>0080 - 00FF</td>
<td>Supplemento Latin-1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>0100 - 017F</td>
<td>Latino esteso A</td>
</tr>
<tr class="even">
<td>3</td>
<td>0180 - 024F</td>
<td>Latino esteso B</td>
</tr>
<tr class="odd">
<td rowspan="3">4${REMOVE}$<br />
</td>
<td>0250 - 02AF</td>
<td>Estensioni IPA</td>
</tr>
<tr class="even">
<td>1D00 - 1D7F</td>
<td>Estensioni fonetiche</td>

</tr>
<tr class="odd">
<td>1D80 - 1DBF</td>
<td>Supplemento estensioni fonetiche</td>

</tr>
<tr class="even">
<td rowspan="2">5${REMOVE}$<br />
</td>
<td>02B0 - 02FF</td>
<td>Lettere di modifica della spaziatura</td>
</tr>
<tr class="odd">
<td>A700 - A71F</td>
<td>Lettere del tono di modifica</td>

</tr>
<tr class="even">
<td rowspan="2">6${REMOVE}$<br />
</td>
<td>0300 - 036F</td>
<td>Combinazione di segni diacritici</td>
</tr>
<tr class="odd">
<td>1DC0 - 1 DFF</td>
<td>Supplemento per segni diacritici combinato</td>

</tr>
<tr class="even">
<td>7</td>
<td>0370 - 03FF</td>
<td>Greco e copto</td>
</tr>
<tr class="odd">
<td>8</td>
<td>2C80 - 2CFF</td>
<td>Copto</td>
</tr>
<tr class="even">
<td rowspan="4">9${REMOVE}$<br />
</td>
<td>0400 - 04FF</td>
<td>Cirillico</td>
</tr>
<tr class="odd">
<td>0500 - 052F</td>
<td>Supplemento cirillico</td>

</tr>
<tr class="even">
<td>2DE0 - 2DFF</td>
<td>Cirillico esteso A</td>

</tr>
<tr class="odd">
<td>A640 - A69F</td>
<td>Cirillico esteso B</td>

</tr>
<tr class="even">
<td>10</td>
<td>0530 - 058F</td>
<td>Armeno</td>
</tr>
<tr class="odd">
<td>11</td>
<td>0590 - 05FF</td>
<td>Ebraico</td>
</tr>
<tr class="even">
<td>12</td>
<td>A500 - A63F</td>
<td>Vai</td>
</tr>
<tr class="odd">
<td rowspan="2">13${REMOVE}$<br />
</td>
<td>0600 - 06FF</td>
<td>Arabo</td>
</tr>
<tr class="even">
<td>0750 - 077F</td>
<td>Supplemento arabo</td>

</tr>
<tr class="odd">
<td>14</td>
<td>07C0 - 07FF</td>
<td>NKo</td>
</tr>
<tr class="even">
<td>15</td>
<td>0900 - 097F</td>
<td>Devanagari</td>
</tr>
<tr class="odd">
<td>16</td>
<td>0980 - 09FF</td>
<td>Bengalese</td>
</tr>
<tr class="even">
<td>17</td>
<td>0A00 - 0A7F</td>
<td>Gurmukhi</td>
</tr>
<tr class="odd">
<td>18</td>
<td>0A80 - 0AFF</td>
<td>Gujarati</td>
</tr>
<tr class="even">
<td>19</td>
<td>0B00 - 0B7F</td>
<td>Odia</td>
</tr>
<tr class="odd">
<td>20</td>
<td>0B80 - 0BFF</td>
<td>Tamil</td>
</tr>
<tr class="even">
<td>21</td>
<td>0C00 - 0C7F</td>
<td>Telugu</td>
</tr>
<tr class="odd">
<td>22</td>
<td>0C80 - 0CFF</td>
<td>Kannada</td>
</tr>
<tr class="even">
<td>23</td>
<td>0D00 - 0D7F</td>
<td>Malayalam</td>
</tr>
<tr class="odd">
<td>24</td>
<td>0E00 - 0E7F</td>
<td>Thai</td>
</tr>
<tr class="even">
<td>25</td>
<td>0E80 - 0EFF</td>
<td>Lao</td>
</tr>
<tr class="odd">
<td rowspan="2">26${REMOVE}$<br />
</td>
<td>10A0 - 10FF</td>
<td>Georgiano</td>
</tr>
<tr class="even">
<td>2D00 - 2D2F</td>
<td>Supplemento in stile alfabeto alfabeto</td>

</tr>
<tr class="odd">
<td>27</td>
<td>1B00 - 1B7F</td>
<td>Balinese</td>
</tr>
<tr class="even">
<td>28</td>
<td>1100 - 11FF</td>
<td>Hangul Jamo</td>
</tr>
<tr class="odd">
<td rowspan="3">29${REMOVE}$<br />
</td>
<td>1E00 - 1EFF</td>
<td>Latin Extended Additional</td>
</tr>
<tr class="even">
<td>2C60 - 2C7F</td>
<td>Alfabeto latino esteso-C</td>

</tr>
<tr class="odd">
<td>A720 - A7FF</td>
<td>Latino esteso-D</td>

</tr>
<tr class="even">
<td>30</td>
<td>1F00 - 1FFF</td>
<td>Greco esteso</td>
</tr>
<tr class="odd">
<td rowspan="2">31${REMOVE}$<br />
</td>
<td>2000 - 206F</td>
<td>Punteggiatura generale</td>
</tr>
<tr class="even">
<td>2E00 - 2E7F</td>
<td>Punteggiatura supplementare</td>

</tr>
<tr class="odd">
<td>32</td>
<td>2070 - 209F</td>
<td>Apici e pedice</td>
</tr>
<tr class="even">
<td>33</td>
<td>20A0 - 20CF</td>
<td>Simboli di valuta</td>
</tr>
<tr class="odd">
<td>34</td>
<td>20D0 - 20FF</td>
<td>Combinazione di segni diacritici per i simboli</td>
</tr>
<tr class="even">
<td>35</td>
<td>2100 - 214F</td>
<td>Simboli simili a lettere</td>
</tr>
<tr class="odd">
<td>36</td>
<td>2150 - 218F</td>
<td>Moduli numerici</td>
</tr>
<tr class="even">
<td rowspan="4">37${REMOVE}$<br />
</td>
<td>2190 - 21FF</td>
<td>Frecce</td>
</tr>
<tr class="odd">
<td>27F0 - 27FF</td>
<td>Frecce supplementari-A</td>

</tr>
<tr class="even">
<td>2900 - 297F</td>
<td>Frecce supplementari-B</td>

</tr>
<tr class="odd">
<td>2B00 - 2BFF</td>
<td>Simboli e frecce vari</td>

</tr>
<tr class="even">
<td rowspan="4">38${REMOVE}$<br />
</td>
<td>2200 - 22FF</td>
<td>Operatori matematici</td>
</tr>
<tr class="odd">
<td>27C0 - 27EF</td>
<td>Simboli matematici vari-A</td>

</tr>
<tr class="even">
<td>2980 - 29FF</td>
<td>Simboli matematici vari-B</td>

</tr>
<tr class="odd">
<td>2A00 - 2AFF</td>
<td>Operatori matematici supplementari</td>

</tr>
<tr class="even">
<td>39</td>
<td>2300 - 23FF</td>
<td>Varie tecniche</td>
</tr>
<tr class="odd">
<td>40</td>
<td>2400 - 243F</td>
<td>Controllare le immagini</td>
</tr>
<tr class="even">
<td>41</td>
<td>2440 - 245F</td>
<td>Riconoscimento ottico dei caratteri</td>
</tr>
<tr class="odd">
<td>42</td>
<td>2460 - 24FF</td>
<td>Caratteri alfanumerici racchiusi</td>
</tr>
<tr class="even">
<td>43</td>
<td>2500 - 257F</td>
<td>Disegno a casella</td>
</tr>
<tr class="odd">
<td>44</td>
<td>2580 - 259F</td>
<td>Elementi block</td>
</tr>
<tr class="even">
<td>45</td>
<td>25A0 - 25FF</td>
<td>Forme geometriche</td>
</tr>
<tr class="odd">
<td>46</td>
<td>2600 - 26FF</td>
<td>Simboli vari</td>
</tr>
<tr class="even">
<td>47</td>
<td>2700 - 27BF</td>
<td>Dingbats</td>
</tr>
<tr class="odd">
<td>48</td>
<td>3000 - 303F</td>
<td>Simboli E punteggiatura CJK</td>
</tr>
<tr class="even">
<td>49</td>
<td>3040 - 309F</td>
<td>Hiragana</td>
</tr>
<tr class="odd">
<td rowspan="2">50${REMOVE}$<br />
</td>
<td>30A0 - 30FF</td>
<td>Katakana</td>
</tr>
<tr class="even">
<td>31F0 - 31FF</td>
<td>Estensioni fonetiche Katakana</td>

</tr>
<tr class="odd">
<td rowspan="2">51${REMOVE}$<br />
</td>
<td>3100 - 312F</td>
<td>Bopomofo</td>
</tr>
<tr class="even">
<td>31A0 - 31BF</td>
<td>Bopomofo Esteso</td>

</tr>
<tr class="odd">
<td>52</td>
<td>3130 - 318F</td>
<td>Jamo di compatibilità Hangul</td>
</tr>
<tr class="even">
<td>53</td>
<td>A840 - A87F</td>
<td>Phags-pa</td>
</tr>
<tr class="odd">
<td>54</td>
<td>3200 - 32FF</td>
<td>Lettere e mesi CJK racchiusi</td>
</tr>
<tr class="even">
<td>55</td>
<td>3300 - 33FF</td>
<td>Compatibilità con CJK</td>
</tr>
<tr class="odd">
<td>56</td>
<td>AC00 - D7AF</td>
<td>Sillabe Hangul</td>
</tr>
<tr class="even">
<td>57</td>
<td>D800 - DFFF</td>
<td>Non piano 0. Si noti che l'impostazione di questo bit implica che esiste almeno un punto di codice supplementare oltre il piano BMP (Basic Multilingual Plane) supportato da questo tipo di carattere. Vedere <a href="surrogates-and-supplementary-characters.md">Surrogati e caratteri supplementari.</a></td>
</tr>
<tr class="odd">
<td>58</td>
<td>10900 - 1091F</td>
<td>Fenicia</td>
</tr>
<tr class="even">
<td rowspan="7">59${REMOVE}$<br />
</td>
<td>2E80 - 2EFF</td>
<td>Supplemento per CJK Radicals</td>
</tr>
<tr class="odd">
<td>2F00 - 2FDF</td>
<td>Kangxi Radicals</td>

</tr>
<tr class="even">
<td>2FF0 - 2FFF</td>
<td>Caratteri di descrizione ideografica</td>

</tr>
<tr class="odd">
<td>3190 - 319F</td>
<td>Kanbun</td>

</tr>
<tr class="even">
<td>3400 - 4DBF</td>
<td>Estensione ideografi unificati CJK A</td>

</tr>
<tr class="odd">
<td>4E00 - 9FFF</td>
<td>Ideografi unificati CJK</td>

</tr>
<tr class="even">
<td>20000 - 2A6DF</td>
<td>Estensione CJK Unified Ideographs B</td>

</tr>
<tr class="odd">
<td>60</td>
<td>E000 - F8FF</td>
<td>Area di utilizzo privato</td>
</tr>
<tr class="even">
<td rowspan="3">61${REMOVE}$<br />
</td>
<td>31C0 - 31EF</td>
<td>Tratti CJK</td>
</tr>
<tr class="odd">
<td>F900 - FAFF</td>
<td>Ideografi di compatibilità CJK</td>

</tr>
<tr class="even">
<td>2F800 - 2FA1F</td>
<td>Supplemento ideografi per la compatibilità CJK</td>

</tr>
<tr class="odd">
<td>62</td>
<td>FB00 - FB4F</td>
<td>Moduli di presentazione alfabetici</td>
</tr>
<tr class="even">
<td>63</td>
<td>FB50 - FDFF</td>
<td>Moduli di presentazione arabo-A</td>
</tr>
<tr class="odd">
<td>64</td>
<td>FE20 - FE2F</td>
<td>Combinazione di mezzi contrassegni</td>
</tr>
<tr class="even">
<td rowspan="2">65${REMOVE}$<br />
</td>
<td>FE10 - FE1F</td>
<td>Moduli verticali</td>
</tr>
<tr class="odd">
<td>FE30 - FE4F</td>
<td>Moduli di compatibilità CJK</td>

</tr>
<tr class="even">
<td>66</td>
<td>FE50 - FE6F</td>
<td>Varianti di forma di piccole dimensioni</td>
</tr>
<tr class="odd">
<td>67</td>
<td>FE70 - FEFF</td>
<td>Moduli di presentazione arabo-B</td>
</tr>
<tr class="even">
<td>68</td>
<td>FF00 - FFEF</td>
<td>Forme halfwidth e fullwidth</td>
</tr>
<tr class="odd">
<td>69</td>
<td>FFF0 - FFFF</td>
<td>Speciali</td>
</tr>
<tr class="even">
<td>70</td>
<td>0F00 - 0FFF</td>
<td>Tibetano</td>
</tr>
<tr class="odd">
<td>71</td>
<td>0700 - 074F</td>
<td>Siriaco</td>
</tr>
<tr class="even">
<td>72</td>
<td>0780 - 07BF</td>
<td>Thaana</td>
</tr>
<tr class="odd">
<td>73</td>
<td>0D80 - 0DFF</td>
<td>Singalese</td>
</tr>
<tr class="even">
<td>74</td>
<td>1000 - 109F</td>
<td>Myanmar</td>
</tr>
<tr class="odd">
<td rowspan="3">75${REMOVE}$<br />
</td>
<td>1200 - 137F</td>
<td>Etiope</td>
</tr>
<tr class="even">
<td>1380 - 139F</td>
<td>Supplemento etiopic</td>

</tr>
<tr class="odd">
<td>2D80 - 2DDF</td>
<td>Ethiopic Extended</td>

</tr>
<tr class="even">
<td>76</td>
<td>13A0 - 13FF</td>
<td>Cherokee</td>
</tr>
<tr class="odd">
<td>77</td>
<td>1400 - 167F</td>
<td>Sillabico aborigeno canadese unificato</td>
</tr>
<tr class="even">
<td>78</td>
<td>1680 - 169F</td>
<td>Ogham</td>
</tr>
<tr class="odd">
<td>79</td>
<td>16A0 - 16FF</td>
<td>Runic</td>
</tr>
<tr class="even">
<td rowspan="2">80${REMOVE}$<br />
</td>
<td>1780 - 17FF</td>
<td>Khmer</td>
</tr>
<tr class="odd">
<td>19E0 - 19FF</td>
<td>Simboli Khmer</td>

</tr>
<tr class="even">
<td>81</td>
<td>1800 - 18AF</td>
<td>Mongolo</td>
</tr>
<tr class="odd">
<td>82</td>
<td>2800 - 28FF</td>
<td>Modelli braille</td>
</tr>
<tr class="even">
<td rowspan="2">83${REMOVE}$<br />
</td>
<td>A000 - A48F</td>
<td>Sillabe Yi</td>
</tr>
<tr class="odd">
<td>A490 - A4CF</td>
<td>Yi Radicals</td>

</tr>
<tr class="even">
<td rowspan="4">84${REMOVE}$<br />
</td>
<td>1700 - 171F</td>
<td>Tagalog</td>
</tr>
<tr class="odd">
<td>1720 - 173F</td>
<td>Hanunoo</td>

</tr>
<tr class="even">
<td>1740 - 175F</td>
<td>Buhid:</td>

</tr>
<tr class="odd">
<td>1760 - 177F</td>
<td>Tagbanwa</td>

</tr>
<tr class="even">
<td>85</td>
<td>10300 - 1032F</td>
<td>Corsivo precedente</td>
</tr>
<tr class="odd">
<td>86</td>
<td>10330 - 1034F</td>
<td>Gotico</td>
</tr>
<tr class="even">
<td>87</td>
<td>10400 - 1044F</td>
<td>Deseret</td>
</tr>
<tr class="odd">
<td rowspan="3">88${REMOVE}$<br />
</td>
<td>1D000 - 1D0FF</td>
<td>Simboli musicali bizantini</td>
</tr>
<tr class="even">
<td>1D100 - 1D1FF</td>
<td>Simboli musicali</td>

</tr>
<tr class="odd">
<td>1D200 - 1D24F</td>
<td>Notazione musicale greco</td>

</tr>
<tr class="even">
<td>89</td>
<td>1D400 - 1D7FF</td>
<td>Simboli alfanumerici matematici</td>
</tr>
<tr class="odd">
<td rowspan="2">90${REMOVE}$<br />
</td>
<td>FF000 - FFFFD</td>
<td>Uso privato (piano 15)</td>
</tr>
<tr class="even">
<td>100000 - 10FFFD</td>
<td>Uso privato (piano 16)</td>

</tr>
<tr class="odd">
<td rowspan="2">91${REMOVE}$<br />
</td>
<td>FE00 - FE0F</td>
<td>Selettori di variazione</td>
</tr>
<tr class="even">
<td>E0100 - E01EF</td>
<td>Supplemento ai selettori di variazione</td>

</tr>
<tr class="odd">
<td>92</td>
<td>E0000 - E007F</td>
<td>Tag</td>
</tr>
<tr class="even">
<td>93</td>
<td>1900 - 194F</td>
<td>Limbu</td>
</tr>
<tr class="odd">
<td>94</td>
<td>1950 - 197F</td>
<td>Tai Le</td>
</tr>
<tr class="even">
<td>95</td>
<td>1980 - 19DF</td>
<td>Nuovo Tai Lue</td>
</tr>
<tr class="odd">
<td>96</td>
<td>1A00 - 1A1F</td>
<td>Buginese</td>
</tr>
<tr class="even">
<td>97</td>
<td>2C00 - 2C5F</td>
<td>Glagolitico</td>
</tr>
<tr class="odd">
<td>98</td>
<td>2D30 - 2D7F</td>
<td>Tifinagh</td>
</tr>
<tr class="even">
<td>99</td>
<td>4DC0 - 4DFF</td>
<td>Simboli hexagram di Yijing</td>
</tr>
<tr class="odd">
<td>100</td>
<td>A800 - A82F</td>
<td>Syloti Nagri</td>
</tr>
<tr class="even">
<td rowspan="3">101${REMOVE}$<br />
</td>
<td>10000 - 1007F</td>
<td>Linear B Syllabary</td>
</tr>
<tr class="odd">
<td>10080 - 100FF</td>
<td>Ideogrammi lineari B</td>

</tr>
<tr class="even">
<td>10100 - 1013F</td>
<td>Numeri egei</td>

</tr>
<tr class="odd">
<td>102</td>
<td>10140 - 1018F</td>
<td>Numeri greco greco</td>
</tr>
<tr class="even">
<td>103</td>
<td>10380 - 1039F</td>
<td>Ugaritico</td>
</tr>
<tr class="odd">
<td>104</td>
<td>103A0 - 103DF</td>
<td>Old Persian</td>
</tr>
<tr class="even">
<td>105</td>
<td>10450 - 1047F</td>
<td>Sha shae</td>
</tr>
<tr class="odd">
<td>106</td>
<td>10480 - 104AF</td>
<td>Osmascher</td>
</tr>
<tr class="even">
<td>107</td>
<td>10800 - 1083F</td>
<td>Sillabara cipriota</td>
</tr>
<tr class="odd">
<td>108</td>
<td>10A00 - 10A5F</td>
<td>Gharoshthi</td>
</tr>
<tr class="even">
<td>109</td>
<td>1D300 - 1D35F</td>
<td>Simboli Tai Xuan Jing</td>
</tr>
<tr class="odd">
<td rowspan="2">110${REMOVE}$<br />
</td>
<td>12000 - 123FF</td>
<td>Cuneiforme</td>
</tr>
<tr class="even">
<td>12400 - 1247F</td>
<td>Numeri cuneiformi e punteggiatura</td>

</tr>
<tr class="odd">
<td>111</td>
<td>1D360 - 1D37F</td>
<td>Conteggio dei numeri dell'asta</td>
</tr>
<tr class="even">
<td>112</td>
<td>1B80 - 1BBF</td>
<td>Sundanese</td>
</tr>
<tr class="odd">
<td>113</td>
<td>1C00 - 1C4F</td>
<td>Lepcha</td>
</tr>
<tr class="even">
<td>114</td>
<td>1C50 - 1C7F</td>
<td>Ol Chiki</td>
</tr>
<tr class="odd">
<td>115</td>
<td>A880 - A8DF</td>
<td>Saurashtra</td>
</tr>
<tr class="even">
<td>116</td>
<td>A900 - A92F</td>
<td>Kayah Li</td>
</tr>
<tr class="odd">
<td>117</td>
<td>A930 - A95F</td>
<td>Rejang</td>
</tr>
<tr class="even">
<td>118</td>
<td>AA00 - AA5F</td>
<td>Cham</td>
</tr>
<tr class="odd">
<td>119</td>
<td>10190 - 101CF</td>
<td>Simboli di simboli di simboli</td>
</tr>
<tr class="even">
<td>120</td>
<td>101D0 - 101FF</td>
<td>Disco Phaistos</td>
</tr>
<tr class="odd">
<td rowspan="3">121${REMOVE}$<br />
</td>
<td>10280 - 1029F</td>
<td>Lycian</td>
</tr>
<tr class="even">
<td>102A0 - 102DF</td>
<td>Caria</td>

</tr>
<tr class="odd">
<td>10920 - 1093F</td>
<td>Lydian</td>

</tr>
<tr class="even">
<td rowspan="2">122${REMOVE}$<br />
</td>
<td>1F000 - 1F02F</td>
<td>Riquadri Mahjong</td>
</tr>
<tr class="odd">
<td>1F030 - 1F09F</td>
<td>Tessere Domino</td>

</tr>
<tr class="even">
<td>123</td>

<td><strong>Windows 2000 e versioni successive:</strong> Stato del layout, orizzontale da destra a sinistra</td>
</tr>
<tr class="odd">
<td>124</td>

<td><strong>Windows 2000 e versioni successive:</strong> Avanzamento del layout, verticale prima dell'orizzontale</td>
</tr>
<tr class="even">
<td>125</td>

<td><strong>Windows 2000 e versioni successive:</strong> Stato del layout, verticale dal basso verso l'alto</td>
</tr>
<tr class="odd">
<td>126-127</td>

<td>Riservato per l'utilizzo interno del processo</td>
</tr>
</tbody>
</table>



 

 

 



