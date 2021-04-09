---
description: In questo argomento vengono descritte le differenze tra le funzioni di stringa utilizzate per la gestione delle informazioni sui set di caratteri e Unicode Queste funzioni dispongono sia di implementazioni di tabella codici Unicode che di Windows per supportare i parametri Unicode e della tabella codici di Windows.
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: Differenze tra le funzioni di stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c940aa8be1603f7958fb1993cc521ca7b1ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967104"
---
# <a name="string-function-differences"></a>Differenze tra le funzioni di stringa

In questo argomento vengono descritte le differenze tra le funzioni di stringa utilizzate per la gestione delle informazioni sui set di caratteri e Unicode Queste funzioni dispongono sia di implementazioni di [tabella codici](code-pages.md) [Unicode](unicode.md) che di Windows per supportare i parametri Unicode e della tabella codici di Windows.

Le funzioni stringa seguenti non richiedono un commento speciale. Le rispettive implementazioni di tabelle codici Unicode e Windows funzionano in modo identico.

-   [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta)
-   [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva)
-   [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [ **StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)
-   [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [ **StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)
-   [**StrCbLength**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha), [ **StrCchLength**](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)

Il valore di lunghezza recuperato da una delle funzioni di lunghezza stringa è sempre basato sulla larghezza del carattere normale: 8 bit per le tabelle codici di Windows, 16 bit per Unicode. Questo valore viene spesso definito "numero di caratteri". Questo termine è rigorosamente corretto perché le tabelle codici di Windows che utilizzano [set di caratteri a doppio byte](double-byte-character-sets.md) (DBCS) presentano caratteri a larghezza intera che sono effettivamente rappresentati da due byte consecutivi. Una situazione simile si verifica per i [surrogati](surrogates-and-supplementary-characters.md) in Unicode.

Le funzioni stringa seguenti sono sensibili alle impostazioni locali del thread corrente, derivate dalla lingua selezionata dall'utente nel pannello di controllo. Le funzioni [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) e [**due**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) non eseguono confronti di byte come gli omonimi ANSI, ad esempio [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp). Al contrario, confrontano le stringhe in base alle regole delle impostazioni locali.

-   [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
-   [**CharLowerBuff**](/windows/win32/api/winuser/nf-winuser-charlowerbuffa)
-   [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)
-   [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
-   [**LSTRCMP**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)
-   [**due**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

Le funzioni seguenti consentono di eseguire la conversione tra il set di caratteri OEM e la tabella codici di Windows corrente o Unicode, a seconda della versione usata:

-   [**CharToOem**](/windows/win32/api/winuser/nf-winuser-chartooema)
-   [**CharToOemBuff**](/windows/win32/api/winuser/nf-winuser-chartooembuffa)
-   [**OemToCharBuff**](/windows/win32/api/winuser/nf-winuser-oemtocharbuffa)

Le funzioni di stampa, ad esempio [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), supportano Unicode fornendo i seguenti tipi di dati nuovi e modificati nelle specifiche di formato. Queste specifiche di formato influiscono sul modo in cui le funzioni interpretano il parametro di input corrispondente.



| Specifica del formato | Tipo di dati per la versione della tabella codici di Windows | Tipo di dati per la versione Unicode |
|----------------------|-----------------------------------------|-------------------------------|
| c                    | CHAR                                    | WCHAR                         |
| C                    | WCHAR                                   | CHAR                          |
| HC, hC               | CHAR                                    | CHAR                          |
| HS, hS               | LPSTR                                   | LPSTR                         |
| LC, lC               | WCHAR                                   | WCHAR                         |
| LS, lS               | LPWSTR                                  | LPWSTR                        |
| s                    | LPSTR                                   | LPWSTR                        |
| S                    | LPWSTR                                  | LPSTR                         |



 

Il tipo di dati per il testo di output dipende sempre dalla versione della funzione. Quando il tipo di dati del parametro di input e il tipo di dati del testo di output non sono conformi, la funzione di stampa esegue una conversione da Unicode alla tabella codici di Windows corrente, o viceversa, in base alle esigenze.

Per la versione Unicode delle funzioni di stampa, la stringa di formato è Unicode, così come il testo di output.

> [!Caution]  
> Una gestione dei buffer insufficiente è coinvolta in molti problemi di sicurezza che coinvolgono sovraccarichi del buffer. Vedere le informazioni di [riferimento su strsafe. h](../menurc/strsafe-ovw.md). Le funzioni definite in strsafe. h forniscono un'elaborazione aggiuntiva per la gestione appropriata del buffer nel codice. Per questo motivo, hanno lo scopo di sostituire le controparti C/C++ predefinite, nonché le implementazioni specifiche di Microsoft Windows. Per ulteriori informazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
