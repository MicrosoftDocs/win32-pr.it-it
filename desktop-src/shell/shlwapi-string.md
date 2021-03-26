---
description: In questa sezione vengono descritte le funzioni di gestione delle stringhe della shell di Windows. Gli elementi di programmazione descritti in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi. h e Shlwapi. lib.
title: Funzioni di gestione delle stringhe della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c2e47785db10ba7dc4bbe54e78e3a06be1b152a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968336"
---
# <a name="shell-string-handling-functions"></a>Funzioni di gestione delle stringhe della shell

In questa sezione vengono descritte le funzioni di gestione delle stringhe della shell di Windows. Gli elementi di programmazione descritti in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi. h e Shlwapi. lib.

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a><br/></td>
<td>Esegue un confronto tra due caratteri. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a><br/></td>
<td>Recupera una stringa utilizzata con i siti Web quando si specificano le preferenze della lingua.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a><br/></td>
<td>Esegue un confronto con distinzione tra maiuscole e minuscole di un numero specificato di caratteri dall'inizio di due stringhe localizzate.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a><br/></td>
<td>Esegue un confronto senza distinzione tra maiuscole e minuscole di un numero specificato di caratteri dall'inizio di due stringhe localizzate.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a><br/></td>
<td>Confronta un numero specificato di caratteri dall'inizio di due stringhe localizzate.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a><br/></td>
<td>Determina se un carattere rappresenta uno spazio.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a><br/></td>
<td>Estrae una risorsa di testo specificata quando la risorsa viene specificata sotto forma di stringa indiretta (una stringa che inizia con il simbolo ' @').<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a><br/></td>
<td>Crea una copia di una stringa nella memoria appena allocata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a><br/></td>
<td>Accoda una stringa a un'altra. <br/>
<blockquote>
[!Note]<br />
Non usare. Vedere la sezione Osservazioni per le funzioni alternative.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a><br/></td>
<td>Copia e aggiunge caratteri da una stringa alla fine di un altro. <br/>
<blockquote>
[!Note]<br />
Non usare. Vedere la sezione Osservazioni per le funzioni alternative.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a><br/></td>
<td>Concatena due stringhe Unicode. Utilizzato quando sono necessarie concatenazioni ripetute allo stesso buffer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a><br/></td>
<td>Cerca in una stringa la prima occorrenza di un carattere che corrisponde al carattere specificato. Il confronto fa distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a><br/></td>
<td>Cerca in una stringa la prima occorrenza di un carattere che corrisponde al carattere specificato. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a><br/></td>
<td>Cerca in una stringa la prima occorrenza di un carattere specificato. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a><br/></td>
<td>Cerca in una stringa la prima occorrenza di un carattere specificato. Il confronto fa distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a><br/></td>
<td>Confronta due stringhe per determinare se sono uguali. Il confronto fa distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a><br/></td>
<td>Confronta le stringhe utilizzando le regole di confronto della fase di esecuzione del linguaggio C (ASCII). Il confronto fa distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a><br/></td>
<td>Confronta due stringhe per determinare se sono uguali. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a><br/></td>
<td>Confronta due stringhe utilizzando le regole di confronto della fase di esecuzione del linguaggio C (ASCII). Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a><br/></td>
<td>Confronta due stringhe Unicode. Le cifre nelle stringhe vengono considerate come contenuti numerici anziché come testo. Questo test non fa distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a><br/></td>
<td>Confronta un numero specificato di caratteri dall'inizio di due stringhe per determinare se sono uguali. Il confronto fa distinzione tra maiuscole e minuscole. La macro <strong>StrNCmp</strong> è diversa da questa funzione solo nel nome.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a><br/></td>
<td>Confronta un numero specificato di caratteri dall'inizio di due stringhe utilizzando le regole di confronto della fase di esecuzione del linguaggio C (ASCII). Il confronto fa distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a><br/></td>
<td>Confronta un numero specificato di caratteri dall'inizio di due stringhe per determinare se sono uguali. Nel confronto non viene fatta distinzione tra maiuscole e minuscole. La macro <strong>StrNCmpI</strong> è diversa da questa funzione solo nel nome.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a><br/></td>
<td>Confronta un numero specificato di caratteri dall'inizio di due stringhe utilizzando le regole di confronto della fase di esecuzione del linguaggio C (ASCII). Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a><br/></td>
<td>Copia una stringa in un'altra. <br/>
<blockquote>
[!Note]<br />
Non usare. Vedere la sezione Osservazioni per le funzioni alternative.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a><br/></td>
<td>Copia un numero specificato di caratteri dall'inizio di una stringa a un'altra.<br/>
<blockquote>
[!Note]<br />
Non usare questa funzione o la macro <strong>StrNCpy</strong> . Vedere la sezione Osservazioni per le funzioni alternative.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a><br/></td>
<td>Cerca in una stringa la prima occorrenza di un gruppo di caratteri. Il metodo di ricerca fa distinzione tra maiuscole e minuscole e il carattere <strong>null</strong> di terminazione è incluso nella corrispondenza dei criteri di ricerca.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a><br/></td>
<td>Cerca in una stringa la prima occorrenza di un gruppo di caratteri. Il metodo di ricerca non fa distinzione tra maiuscole e minuscole e il carattere di terminazione <strong>null</strong> è incluso nella corrispondenza dei criteri di ricerca.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a><br/></td>
<td>Duplica una stringa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a><br/></td>
<td>Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a><br/></td>
<td>Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni. Differisce da <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> in un tipo di parametro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a><br/></td>
<td>Converte un valore numerico in una stringa che rappresenta il numero in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni. Estende <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> offrendo l'opzione per arrotondare alla cifra visualizzata più vicina o per eliminare le cifre non visualizzate.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a><br/></td>
<td>Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni. Differisce da <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> in un tipo di parametro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a><br/></td>
<td>Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in kilobyte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a><br/></td>
<td>Converte un intervallo di tempo, in millisecondi, in una stringa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a><br/></td>
<td>Confronta un numero specificato di caratteri dall'inizio di due stringhe per determinare se sono uguali.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a><br/></td>
<td>Accoda un numero specificato di caratteri dall'inizio di una stringa alla fine di un altro. <br/>
<blockquote>
[!Note]<br />
Non usare questa funzione o la macro <strong>StrCatN</strong> . Vedere la sezione Osservazioni per le funzioni alternative.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a><br/></td>
<td>Cerca in una stringa la prima occorrenza di un carattere contenuto in un buffer specificato. Questa ricerca non include il carattere null di terminazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a><br/></td>
<td>Cerca in una stringa l'ultima occorrenza di un carattere specificato. Il confronto fa distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a><br/></td>
<td>Cerca in una stringa l'ultima occorrenza di un carattere specificato. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a><br/></td>
<td>Accetta una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> che contiene o punta a una stringa e restituisce tale stringa come <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a><br/></td>
<td>Converte una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> in una stringa e inserisce il risultato in un buffer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a><br/></td>
<td>Accetta una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> e restituisce un puntatore a una stringa allocata contenente il nome visualizzato.<br/></td>
</tr>
<tr class="even">
<td><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a><br/></td>
<td>Accetta una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a>, la converte in una stringa e inserisce il risultato in un buffer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a><br/></td>
<td>Consente di cercare l'ultima occorrenza di una sottostringa specificata all'interno di una stringa. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a><br/></td>
<td>Ottiene la lunghezza di una sottostringa all'interno di una stringa costituita interamente da caratteri contenuti in un buffer specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a><br/></td>
<td>Trova la prima occorrenza di una sottostringa all'interno di una stringa. Il confronto fa distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a><br/></td>
<td>Trova la prima occorrenza di una sottostringa all'interno di una stringa. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a><br/></td>
<td>Converte una stringa che rappresenta un valore decimale in un intero. La macro <strong>StrToLong</strong> è identica a questa funzione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a><br/></td>
<td>Converte una stringa che rappresenta un valore decimale o esadecimale in un intero a 64 bit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a><br/></td>
<td>Converte una stringa che rappresenta un numero decimale o esadecimale in un valore integer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a><br/></td>
<td>Rimuove i caratteri iniziali e finali specificati da una stringa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a><br/></td>
<td>Accetta un elenco di argomenti a lunghezza variabile e restituisce i valori degli argomenti come stringa formattata in stile <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br/>
<blockquote>
[!Note]<br />
Non usare questa funzione. Vedere la sezione Osservazioni per le funzioni alternative.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a><br/></td>
<td>Accetta un elenco di argomenti e restituisce i valori degli argomenti come stringa formattata in stile <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br/>
<blockquote>
[!Note]<br />
Non usare questa funzione. Vedere la sezione Osservazioni per le funzioni alternative.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
