---
description: In questo argomento vengono descritte le differenze tra le funzioni stringa utilizzate nella gestione delle informazioni unicode e dei set di caratteri. Queste funzioni hanno implementazioni sia Unicode che Windows di tabella codici per supportare i parametri unicode Windows tabella codici.
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: Differenze tra le funzioni stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60a6208e858eceac65ac8826ffbff6303b970969cae6f635d0bcc027dd6d9f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146994"
---
# <a name="string-function-differences"></a>Differenze tra le funzioni stringa

In questo argomento vengono descritte le differenze tra le funzioni stringa utilizzate nella gestione delle informazioni unicode e dei set di caratteri. Queste funzioni hanno implementazioni sia [Unicode](unicode.md) [che Windows di tabella](code-pages.md) codici per supportare i parametri unicode Windows tabella codici.

Le funzioni stringa seguenti non richiedono un commento speciale. Le implementazioni unicode e Windows della tabella codici funzionano in modo identico.

-   [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta)
-   [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva)
-   [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [ **StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)
-   [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [ **StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)
-   [**StrCbLength**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha), [ **StrCchLength**](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)

Il valore della lunghezza recuperato da una delle funzioni di lunghezza della stringa è sempre basato sulla larghezza normale dei caratteri: 8 bit per le Windows di codice, 16 bit per Unicode. Questo valore viene spesso definito "conteggio di caratteri". Questo termine è strettamente corretto perché Windows le [](double-byte-character-sets.md) pagine di codice che usano set di caratteri a byte doppio (DBCS) hanno alcuni caratteri a larghezza intera che sono effettivamente rappresentati da due byte consecutivi. Una situazione simile si verifica per [i surrogati](surrogates-and-supplementary-characters.md) in Unicode.

Le funzioni stringa seguenti sono sensibili alle impostazioni locali del thread corrente, derivate dalla lingua selezionata dall'utente nel Pannello di controllo. Le [**funzioni lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) [**e lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) non eseguono confronti di byte come i nomi ANSI, ad esempio [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp). Confrontano invece le stringhe in base alle regole delle impostazioni locali.

-   [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
-   [**CharLowerBuff**](/windows/win32/api/winuser/nf-winuser-charlowerbuffa)
-   [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)
-   [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
-   [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)
-   [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

Le funzioni seguenti e convertono tra il set di caratteri OEM e la tabella codici Windows corrente o Unicode, a seconda della versione usata:

-   [**CharToOem**](/windows/win32/api/winuser/nf-winuser-chartooema)
-   [**CharToOemBuff**](/windows/win32/api/winuser/nf-winuser-chartooembuffa)
-   [**OemToCharBuff**](/windows/win32/api/winuser/nf-winuser-oemtocharbuffa)

Le funzioni di stampa, ad esempio [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), supportano Unicode fornendo i tipi di dati nuovi e modificati seguenti nelle specifiche di formato. Queste specifiche di formato influiscono sul modo in cui le funzioni interpretano il parametro di input corrispondente.



| Specifica del formato | Tipo di dati per la Windows della tabella codici | Tipo di dati per la versione Unicode |
|----------------------|-----------------------------------------|-------------------------------|
| c                    | CHAR                                    | WCHAR                         |
| C                    | WCHAR                                   | CHAR                          |
| hc, hC               | CHAR                                    | CHAR                          |
| hs, hS               | LPSTR                                   | LPSTR                         |
| lc, lC               | WCHAR                                   | WCHAR                         |
| ls, lS               | LPWSTR                                  | LPWSTR                        |
| s                    | LPSTR                                   | LPWSTR                        |
| S                    | LPWSTR                                  | LPSTR                         |



 

Il tipo di dati per il testo di output dipende sempre dalla versione della funzione. Quando il tipo di dati del parametro di input e il tipo di dati del testo di output non sono concordi, la funzione print esegue una conversione da Unicode alla tabella codici Windows corrente o viceversa, in base alle esigenze.

Per la versione Unicode delle funzioni di stampa, la stringa di formato è Unicode, così come il testo di output.

> [!Caution]  
> Una gestione insufficiente del buffer è implicata in molti problemi di sicurezza che comportano sovraccarichi del buffer. Vedere [Strsafe.h Reference (Informazioni di riferimento su Strsafe.h).](../menurc/strsafe-ovw.md) Le funzioni definite in Strsafe.h forniscono un'elaborazione aggiuntiva per la corretta gestione del buffer nel codice. Per questo motivo, hanno lo scopo di sostituire le controparti C/C++ incorporate e specifiche implementazioni di Microsoft Windows. Per altre informazioni, vedere [Considerazioni sulla sicurezza: funzionalità internazionali.](security-considerations--international-features.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
