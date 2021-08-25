---
title: Informazioni su Strsafe.h
description: Una gestione del buffer insufficiente è implicata in molti problemi di sicurezza che comportano sovraccarichi del buffer.
ms.assetid: a104a260-1edb-441a-acf8-e2bd3a7d8235
keywords:
- funzioni per i valori stringa
- Strsafe.h
- Funzioni Strsafe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5d50a6921e2775c64fd4db53393332c667aba975ffa366fb2eb49881b6beaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720591"
---
# <a name="about-strsafeh"></a>Informazioni su Strsafe.h

Una gestione del buffer insufficiente è implicata in molti problemi di sicurezza che comportano sovraccarichi del buffer. Le funzioni definite in Strsafe.h forniscono un'ulteriore elaborazione per una corretta gestione del buffer nel codice. Per questo motivo, sono destinate a sostituire le controparti C/C++ incorporate e implementazioni Windows specifiche. Strsafe.h è disponibile in Windows SDK a partire da Windows XP con Service Pack 2 (SP2).

I vantaggi delle funzioni Strsafe includono:

-   Le dimensioni del buffer di destinazione vengono sempre fornite alla funzione per garantire che la funzione non scrivo oltre la fine del buffer.

-   È garantito che i buffer siano con terminazione Null, anche se l'operazione tronca il risultato previsto.

-   Tutte le funzioni restituiscono **un valore HRESULT,** con un solo possibile codice di esito positivo (**S \_ OK**).

-   Ogni funzione è disponibile in una versione corrispondente del conteggio dei caratteri ("cch") o del numero di byte ("cb").

-   La maggior parte delle funzioni ha una versione estesa ("Ex") disponibile per funzionalità avanzate.

Per altre informazioni, vedere le sezioni seguenti.

-   [Funzioni di conteggio caratteri](#character-count-functions)
-   [Funzioni per il conteggio dei byte](#byte-count-functions)
-   [Uso di Strsafe.h](#using-strsafeh)
-   [Argomenti correlati](#related-topics)

## <a name="character-count-functions"></a>Funzioni di conteggio caratteri

Le funzioni seguenti usano un numero di caratteri anziché un numero di byte.



| Funzione                                                                                                                                                                                                                      | Sostituisce                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt> [ **StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**StrCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**StrCatBuff**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                             |
| <dl> <dt>[**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)</dt> <dt> [ **StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **StrNCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                   |
| <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt> [ **StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**StrCpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                    |
| <dl> <dt>[**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)</dt> <dt> [ **StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ tcsncpy](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>[**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)</dt> <dt> [ **StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)</dt> </dl>             | <dl> <dt>[gets, \_ getws, \_ getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt> [ **StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ stprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>          |
| <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt> [ **StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**wvnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl>, |
| <dl> <dt>[**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> </dl>                                                                                                         | <dl> <dt>[strlen, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="byte-count-functions"></a>Funzioni per il conteggio dei byte

Le funzioni seguenti usano un numero di byte anziché un numero di caratteri.



| Funzione                                                                                                                                                                                                                  | Sostituisce                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt> [ **StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**StrCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**StrCatBuff**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                            |
| <dl> <dt>[**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)</dt> <dt> [ **StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **StrNCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                  |
| <dl> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt> [ **StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**StrCpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                   |
| <dl> <dt>[**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)</dt> <dt> [ **StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ tcsncpy](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>[**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)</dt> <dt> [ **StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)</dt> </dl>             | <dl> <dt>[gets, \_ getws, \_ getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt> [ **StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ stprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>         |
| <dl> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt> [ **StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**wvnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl> |
| <dl> <dt>[**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                       | <dl> <dt>[strlen, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="using-strsafeh"></a>Uso di Strsafe.h

-   Per usare le funzioni Strsafe inline, includere il file di intestazione come illustrato di seguito, seguendo le **\# istruzioni include** per tutti gli altri file di intestazione.

    `#include <strsafe.h>`

-   Per usare le funzioni in formato libreria, includere l'istruzione seguente prima di includere Strsafe.h. È tuttavia consigliabile usare le funzioni inline.

    `#define STRSAFE_LIB`

    > [!Note]  
    > : le funzioni seguenti devono essere usate come funzioni inline: [**StringCbGets,**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa) [**StringCbGetsEx,**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa) [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)e [**StringCchGetsEx.**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)

     

-   Quando si include Strsafe.h nel file, le funzioni precedenti sostituite dalle funzioni Strsafe.h verranno deprecate. I tentativi di usare queste funzioni precedenti comporteranno un errore del compilatore che indica di usare le funzioni più recenti. Se si vuole eseguire l'override di questo comportamento, includere l'istruzione seguente prima di includere Strsafe.h.

    `#define STRSAFE_NO_DEPRECATE`

-   Per consentire solo le funzioni di conteggio dei caratteri, includere l'istruzione seguente prima di includere Strsafe.h.

    `#define STRSAFE_NO_CB_FUNCTIONS`

-   Per consentire solo funzioni di conteggio dei byte, includere l'istruzione seguente prima di includere Strsafe.h.

    `#define STRSAFE_NO_CCH_FUNCTIONS`

    > [!Note]  
    > È possibile definire **STRSAFE \_ NO \_ CB \_ FUNCTIONS** o **STRSAFE \_ NO \_ CCH \_ FUNCTIONS**, ma non entrambi.

     

-   Alcune funzioni Strsafe hanno versioni con supporto delle impostazioni locali. Per impostazione predefinita, l'intestazione non dichiara queste funzioni. Per abilitare queste dichiarazioni, includere l'istruzione macro seguente prima di includere Strsafe.h.

    `#define STRSAFE_LOCALE_FUNCTIONS`

-   La lunghezza massima supportata per la stringa è di 2.147.483.647 (**STRSAFE \_ MAX \_ CCH),** ansi o Unicode.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni Strsafe](string-overviews.md)
</dt> </dl>

 

 