---
description: In questa sezione vengono descritte le Windows di gestione delle stringhe della shell. Gli elementi di programmazione illustrati in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi.h e Shlwapi.lib.
title: Funzioni di gestione delle stringhe della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d11ad956b6eab11212243232dfaf8ef341d05544
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473317"
---
# <a name="shell-string-handling-functions"></a>Funzioni di gestione delle stringhe della shell

In questa sezione vengono descritte le Windows di gestione delle stringhe della shell. Gli elementi di programmazione illustrati in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi.h e Shlwapi.lib.

## <a name="in-this-section"></a>Contenuto della sezione




| Argomento | Descrizione | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a><br /> | Esegue un confronto tra due caratteri. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a><br /> | Recupera una stringa utilizzata con i siti Web quando si specificano le preferenze di lingua.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a><br /> | Esegue un confronto con distinzione tra maiuscole e minuscole di un numero specificato di caratteri dall'inizio di due stringhe localizzate.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a><br /> | Esegue un confronto senza distinzione tra maiuscole e minuscole di un numero specificato di caratteri dall'inizio di due stringhe localizzate.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a><br /> | Confronta un numero specificato di caratteri dall'inizio di due stringhe localizzate.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a><br /> | Determina se un carattere rappresenta uno spazio.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a><br /> | Estrae una risorsa di testo specificata quando viene specificata tale risorsa sotto forma di stringa indiretta (stringa che inizia con il simbolo '@').<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a><br /> | Crea una copia di una stringa nella memoria appena allocata.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a><br /> | Aggiunge una stringa a un'altra. <br /><blockquote>[!Note]<br />Non usare. Vedere Osservazioni per le funzioni alternative.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a><br /> | Copia e aggiunge caratteri da una stringa alla fine di un'altra. <br /><blockquote>[!Note]<br />Non usare. Vedere Osservazioni per le funzioni alternative.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a><br /> | Concatena due stringhe Unicode. Utilizzato quando sono necessarie concatenazioni ripetute allo stesso buffer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a><br /> | Cerca in una stringa la prima occorrenza di un carattere che corrisponde al carattere specificato. Il confronto fa distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a><br /> | Cerca in una stringa la prima occorrenza di un carattere che corrisponde al carattere specificato. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a><br /> | Cerca in una stringa la prima occorrenza di un carattere specificato. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a><br /> | Cerca in una stringa la prima occorrenza di un carattere specificato. Il confronto fa distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>Strcmp</strong></a><br /> | Confronta due stringhe per determinare se sono uguali. Il confronto fa distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a><br /> | Confronta le stringhe usando regole di confronto C in fase di esecuzione (ASCII). Il confronto fa distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a><br /> | Confronta due stringhe per determinare se sono uguali. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a><br /> | Confronta due stringhe usando regole di confronto C in fase di esecuzione (ASCII). Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a><br /> | Confronta due stringhe Unicode. Le cifre nelle stringhe vengono considerate come contenuto numerico anziché come testo. Questo test non fa distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a><br /> | Confronta un numero specificato di caratteri dall'inizio di due stringhe per determinare se sono uguali. Il confronto fa distinzione tra maiuscole e minuscole. La macro <strong>StrNCmp</strong> differisce da questa funzione solo nel nome.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a><br /> | Confronta un numero specificato di caratteri dall'inizio di due stringhe usando regole di confronto C in fase di esecuzione (ASCII). Il confronto fa distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a><br /> | Confronta un numero specificato di caratteri dall'inizio di due stringhe per determinare se sono uguali. Nel confronto non viene fatta distinzione tra maiuscole e minuscole. La macro <strong>StrNCmpI</strong> differisce da questa funzione solo nel nome.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a><br /> | Confronta un numero specificato di caratteri dall'inizio di due stringhe usando regole di confronto C in fase di esecuzione (ASCII). Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>Strcpy</strong></a><br /> | Copia una stringa in un'altra. <br /><blockquote>[!Note]<br />Non usare. Vedere Osservazioni per le funzioni alternative.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a><br /> | Copia un numero specificato di caratteri dall'inizio di una stringa a un'altra.<br /><blockquote>[!Note]<br />Non usare questa funzione o la macro <strong>StrNCpy.</strong> Vedere Osservazioni per le funzioni alternative.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a><br /> | Cerca in una stringa la prima occorrenza di un gruppo di caratteri. Il metodo di ricerca fa distinzione tra maiuscole e minuscole e il carattere <strong>NULL</strong> di terminazione è incluso nella corrispondenza del criterio di ricerca.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a><br /> | Cerca in una stringa la prima occorrenza di un gruppo di caratteri. Il metodo di ricerca non fa distinzione tra maiuscole e minuscole e il carattere <strong>NULL</strong> di terminazione è incluso nella corrispondenza del criterio di ricerca.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a><br /> | Duplica una stringa.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a><br /> | Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a><br /> | Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni. Differisce da <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> in un tipo di parametro.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a><br /> | Converte un valore numerico in una stringa che rappresenta il numero in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni. Estende <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> offrendo la possibilità di arrotondare alla cifra visualizzata più vicina o di eliminare le cifre non visualizzate.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a><br /> | Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni. Differisce da <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> in un tipo di parametro.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a><br /> | Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in kilobyte.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a><br /> | Converte un intervallo di tempo, specificato in millisecondi, in una stringa.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a><br /> | Confronta un numero specificato di caratteri dall'inizio di due stringhe per determinare se sono uguali.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a><br /> | Aggiunge un numero specificato di caratteri dall'inizio di una stringa alla fine di un'altra. <br /><blockquote>[!Note]<br />Non usare questa funzione o la macro <strong>StrCatN.</strong> Per le funzioni alternative, vedere La sezione Osservazioni.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a><br /> | Cerca in una stringa la prima occorrenza di un carattere contenuto in un buffer specificato. Questa ricerca non include il carattere null di terminazione.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a><br /> | Cerca in una stringa l'ultima occorrenza di un carattere specificato. Il confronto fa distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a><br /> | Cerca in una stringa l'ultima occorrenza di un carattere specificato. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a><br /> | Accetta una <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>struttura STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> che contiene o punta a una stringa e restituisce tale stringa <a href="/previous-versions/windows/desktop/automat/bstr"><strong>come BSTR.</strong></a><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a><br /> | Converte una <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>struttura STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> in una stringa e inserisce il risultato in un buffer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a><br /> | Accetta una <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>struttura STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> e restituisce un puntatore a una stringa allocata contenente il nome visualizzato.<br /> | 
| <a href="strrettostrn.md"><strong>StrRetToStrN</strong></a><br /> | Accetta una <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>struttura STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf,</strong></a>la converte in una stringa e inserisce il risultato in un buffer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a><br /> | Cerca l'ultima occorrenza di una sottostringa specificata all'interno di una stringa. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a><br /> | Ottiene la lunghezza di una sottostringa all'interno di una stringa costituita interamente da caratteri contenuti in un buffer specificato.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a><br /> | Trova la prima occorrenza di una sottostringa all'interno di una stringa. Il confronto fa distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a><br /> | Trova la prima occorrenza di una sottostringa all'interno di una stringa. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a><br /> | Converte una stringa che rappresenta un valore decimale in un intero. La macro <strong>StrToLong</strong> è identica a questa funzione.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a><br /> | Converte una stringa che rappresenta un valore decimale o esadecimale in un intero a 64 bit.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a><br /> | Converte una stringa che rappresenta un numero decimale o esadecimale in un numero intero.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a><br /> | Rimuove i caratteri iniziali e finali specificati da una stringa.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a><br /> | Accetta un elenco di argomenti a lunghezza variabile e restituisce i valori degli argomenti come stringa formattata di tipo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf.</strong></a> <br /><blockquote>[!Note]<br />Non usare questa funzione. Per le funzioni alternative, vedere La sezione Osservazioni.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a><br /> | Accetta un elenco di argomenti e restituisce i valori degli argomenti come stringa formattata di tipo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf.</strong></a> <br /><blockquote>[!Note]<br />Non usare questa funzione. Per le funzioni alternative, vedere La sezione Osservazioni.</blockquote><br /> | 




 

 

 
