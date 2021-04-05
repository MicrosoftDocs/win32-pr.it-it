---
title: Stringhe
description: In questa sezione vengono illustrate le funzioni di stringa.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- risorse, stringhe
- stringhe
- funzioni per i valori stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3231006de2dfe6ed611b58e5b511819a40c21e8b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732098"
---
# <a name="strings"></a>Stringhe

Questa sezione descrive le funzioni di stringa e spiega come usarle nelle applicazioni.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                     | Descrizione                                             |
|------------------------------------------|---------------------------------------------------------|
| [Informazioni sulle stringhe](about-strings.md)       | Vengono illustrate le funzioni di stringa.<br/>              |
| [Informazioni su strsafe. h](strsafe-ovw.md)       | Vengono illustrate le funzioni di stringa in strsafe. h.<br/> |
| [Riferimento alla stringa](string-reference.md) | Contiene il riferimento all'API.<br/>                  |



 

### <a name="string-functions"></a>Funzioni di stringa



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></td>
<td>Converte una stringa di caratteri o un singolo carattere in lettere minuscole. Se l'operando è una stringa di caratteri, la funzione converte i caratteri sul posto. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></td>
<td>Converte i caratteri maiuscoli in un buffer in caratteri minuscoli. La funzione converte i caratteri sul posto. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></td>
<td>Recupera un puntatore al carattere successivo in una stringa. Questa funzione può gestire le stringhe costituite da caratteri a byte singolo o multibyte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></td>
<td>Recupera il puntatore al carattere successivo in una stringa. Questa funzione può gestire le stringhe costituite da caratteri a byte singolo o multibyte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></td>
<td>Recupera un puntatore al carattere precedente in una stringa. Questa funzione può gestire le stringhe costituite da caratteri a byte singolo o multibyte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></td>
<td>Recupera il puntatore al carattere precedente in una stringa. Questa funzione può gestire le stringhe costituite da caratteri a byte singolo o multibyte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></td>
<td>Converte una stringa nel set di caratteri definito dall'OEM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></td>
<td>Converte un numero specificato di caratteri in una stringa nel set di caratteri definito dall'OEM.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></td>
<td>Converte una stringa di caratteri o un singolo carattere in maiuscolo. Se l'operando è una stringa di caratteri, la funzione converte i caratteri sul posto. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></td>
<td>Converte i caratteri minuscoli di un buffer in caratteri maiuscoli. La funzione converte i caratteri sul posto. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></td>
<td>Confronta due stringhe di caratteri, usando le impostazioni locali specificate.
<blockquote>
[!Note]<br />
Per compatibilità con Unicode, usare <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> o la versione Unicode di <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></td>
<td>Confronta due stringhe Unicode (caratteri wide), usando le impostazioni locali specificate.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>Della funzione FoldString</strong></a></td>
<td>Esegue il mapping di una stringa a un'altra, eseguendo un'opzione di trasformazione specificata. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></td>
<td>Recupera le informazioni sul tipo di carattere per i caratteri nella stringa di origine specificata. Per ogni carattere nella stringa, la funzione imposta uno o più bit nell'elemento a 16 bit corrispondente della matrice di output. Ogni bit identifica un tipo di carattere specificato, ad esempio se il carattere è una lettera, una cifra o nessuno dei due.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></td>
<td>Recupera le informazioni sul tipo di carattere per i caratteri nella stringa di origine specificata. Per ogni carattere nella stringa, la funzione imposta uno o più bit nell'elemento a 16 bit corrispondente della matrice di output. Ogni bit identifica un tipo di carattere specificato, ad esempio se il carattere è una lettera, una cifra o nessuno dei due. <br/> A differenza dei parenti di chiusura <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> e <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> presenta il comportamento standard tramite l'uso dell'opzione <strong> # define Unicode</strong> . Si tratta della funzione consigliata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></td>
<td>Recupera le informazioni sul tipo di carattere per i caratteri nella stringa di origine specificata. Per ogni carattere nella stringa, la funzione imposta uno o più bit nell'elemento a 16 bit corrispondente della matrice di output. Ogni bit identifica un tipo di carattere specificato, ad esempio se il carattere è una lettera, una cifra o nessuno dei due.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></td>
<td>Determina se un carattere è un carattere alfabetico. Questa determinazione è basata sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite il pannello di controllo. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></td>
<td>Determina se un carattere è un carattere alfabetico o numerico. Questa determinazione è basata sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite il pannello di controllo. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></td>
<td>Determina se un carattere è minuscolo. Questa determinazione è basata sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite il pannello di controllo. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></td>
<td>Determina se un carattere è in maiuscolo. Questa determinazione è basata sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite il pannello di controllo. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></td>
<td>Carica una risorsa di tipo stringa dal file eseguibile associato a un modulo specificato, copia la stringa in un buffer e aggiunge un carattere di terminazione NULL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></td>
<td>Accoda una stringa a un'altra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>LSTRCMP</strong></a></td>
<td>Confronta due stringhe di caratteri. Il confronto fa distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>due</strong></a></td>
<td>Confronta due stringhe di caratteri. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></td>
<td>Copia una stringa in un buffer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></td>
<td>Copia un numero specificato di caratteri da una stringa di origine in un buffer. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></td>
<td>Determina la lunghezza della stringa specificata (escluso il carattere null di terminazione).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></td>
<td>Converte una stringa dal set di caratteri definito dall'OEM in una stringa ANSI o a caratteri wide.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></td>
<td>Converte un numero specificato di caratteri in una stringa dal set di caratteri definito dall'OEM in una stringa ANSI o di caratteri wide.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></td>
<td>Scrive i dati formattati nel buffer specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></td>
<td>Scrive i dati formattati nel buffer specificato utilizzando un puntatore a un elenco di argomenti.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="strsafe-functions"></a>Funzioni strsafe



| Nome                                             | Descrizione                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | Concatena una stringa a un'altra stringa.<br/>                                            |
| [**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | Concatena una stringa a un'altra stringa.<br/>                                            |
| [**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | Concatena il numero specificato di byte da una stringa a un'altra stringa.<br/>         |
| [**StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | Concatena il numero specificato di byte da una stringa a un'altra stringa.<br/>         |
| [**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | Copia una stringa in un'altra.<br/>                                                         |
| [**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | Copia una stringa in un'altra.<br/>                                                         |
| [**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | Copia il numero specificato di byte da una stringa a un'altra.<br/>                      |
| [**StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | Copia il numero specificato di byte da una stringa a un'altra.<br/>                      |
| [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | Ottiene una riga di testo da stdin, fino a includere il carattere di nuova riga (' \\ n').<br/>  |
| [**StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | Ottiene una riga di testo da stdin, fino a includere il carattere di nuova riga (' \\ n').<br/>  |
| [**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | Determina se una stringa supera la lunghezza specificata, in byte.<br/>                   |
| [**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | Scrive i dati formattati nella stringa specificata.<br/>                                        |
| [**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | Scrive i dati formattati nella stringa specificata.<br/>                                        |
| [**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | Scrive i dati formattati nella stringa specificata utilizzando un puntatore a un elenco di argomenti.<br/> |
| [**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | Scrive i dati formattati nella stringa specificata utilizzando un puntatore a un elenco di argomenti.<br/> |
| [**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | Concatena una stringa a un'altra stringa.<br/>                                            |
| [**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | Concatena una stringa a un'altra stringa.<br/>                                            |
| [**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | Concatena il numero specificato di caratteri da una stringa a un'altra stringa.<br/>    |
| [**StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | Concatena il numero specificato di caratteri da una stringa a un'altra stringa.<br/>    |
| [**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | Copia una stringa in un'altra.<br/>                                                         |
| [**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | Copia una stringa in un'altra.<br/>                                                         |
| [**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | Copia il numero specificato di caratteri da una stringa a un'altra.<br/>                 |
| [**StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | Copia il numero specificato di caratteri da una stringa a un'altra.<br/>                 |
| [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | Ottiene una riga di testo da stdin, fino a includere il carattere di nuova riga (' \\ n').<br/>  |
| [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | Ottiene una riga di testo da stdin, fino a includere il carattere di nuova riga (' \\ n').<br/>  |
| [**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | Determina se una stringa supera la lunghezza specificata, in caratteri.<br/>              |
| [**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | Scrive i dati formattati nella stringa specificata.<br/>                                        |
| [**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | Scrive i dati formattati nella stringa specificata.<br/>                                        |
| [**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | Scrive i dati formattati nella stringa specificata utilizzando un puntatore a un elenco di argomenti.<br/> |
| [**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | Scrive i dati formattati nella stringa specificata utilizzando un puntatore a un elenco di argomenti.<br/> |



 

 

