---
title: Come usare le informazioni relative a parole e interruzioni di riga
description: Un controllo Rich Edit chiama una funzione chiamata procedura di interruzione di parola per individuare le interruzioni tra le parole e per determinare la posizione in cui è possibile interrompere le righe.
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb90064e455bfeb8ee126e6107d75ef29b3a4f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300504"
---
# <a name="how-to-use-word-and-line-break-information"></a>Come usare le informazioni relative a parole e interruzioni di riga

Un controllo Rich Edit chiama una funzione chiamata procedura di interruzione di parola per individuare le interruzioni tra le parole e per determinare la posizione in cui è possibile interrompere le righe. Il controllo utilizza queste informazioni quando si eseguono operazioni di ritorno a capo automatico e quando si elaborano le combinazioni di tasti CTRL + freccia sinistra e CTRL + freccia destra. Un'applicazione può inviare messaggi a un controllo Rich Edit per sostituire la routine di Word break predefinita, per recuperare le informazioni sull'interruzioni di parola e per determinare la riga in cui si trova un determinato carattere.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-word-and-line-break-information"></a>Usare le informazioni relative a parole e interruzioni di riga

Le procedure di Word break per i controlli Rich Edit sono simili a quelle per i controlli di modifica, ma dispongono di funzionalità aggiuntive: le procedure di Word break per entrambi i tipi di controlli possono determinare se un carattere è un delimitatore ed è in grado di trovare la parola break più vicina prima o dopo la posizione specificata. Un delimitatore è un carattere che contrassegna la fine di una parola, ad esempio uno spazio. In genere, in un controllo di modifica, una parola break si verifica solo dopo i delimitatori. Tuttavia, le diverse regole si applicano alla maggior parte delle lingue asiatiche.

Anche le procedure di Word break per i controlli Rich Edit raggruppano i caratteri in classi di caratteri, ognuna identificata da un valore compreso nell'intervallo da 0x00 a 0x0F. Le interruzioni si verificano dopo i delimitatori o tra caratteri di classi diverse. Una procedura di interruzione di parola con classi diverse per i caratteri alfanumerici e di punteggiatura potrebbe quindi trovare due interruzioni di parola nella stringa "Win.doc" (prima e dopo il periodo).

La classe di un carattere può essere combinata con zero o più flag di interruzioni di parola per formare un valore a 8 bit. Quando si eseguono operazioni di ritorno a capo automatico, un controllo Rich Edit usa i flag di interruzioni di parola per determinare la posizione in cui è possibile interrompere le righe. Rich Edit usa i flag di Word breaker seguenti.



| Flag            | Descrizione                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| \_BREAKAFTER WBF | È possibile che le righe siano interrotte dopo il carattere.                                                                                          |
| \_discontinuità WBF  | Il carattere è un delimitatore. I delimitatori contrassegnano le estremità delle parole. È possibile che le righe siano interrotte dopo i delimitatori.                            |
| WBF \_ bianco    | Il carattere è un carattere di spazio vuoto. Gli spazi vuoti finali non sono inclusi nella lunghezza di una riga durante il wrapping. |



 

Il \_ valore BREAKAFTER di WBF viene usato per consentire il wrapping dopo un carattere che non contrassegna la fine di una parola, ad esempio un trattino.

È possibile sostituire la routine di Word break predefinita per un controllo Rich Edit con una procedura personalizzata usando il messaggio [**\_ SETWORDBREAKPROC em**](em-setwordbreakproc.md) . Per ulteriori informazioni sulle procedure per le interruzioni di parola, vedere la descrizione della funzione [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .

> [!Note]  
> Questa sostituzione non è consigliata per Microsoft Rich Edit 2,0 e versioni successive, a causa della complessità di Word revisioni multilingue.

 

Per Microsoft Rich Edit 1,0, è possibile usare il [**messaggio \_ SETWORDBREAKPROCEX em**](em-setwordbreakprocex.md) per sostituire la routine di Word Breaking estesa predefinita con una funzione [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) . Questa funzione fornisce informazioni aggiuntive sul testo, ad esempio il set di caratteri. È possibile usare il [**messaggio \_ GETWORDBREAKPROCEX em**](em-getwordbreakprocex.md) per recuperare l'indirizzo della procedura di Breaking di Word estesa corrente. Si noti che Microsoft Rich Edit 2,0 e versioni successive non supportano *EditWordBreakProcEx*, **em \_ GETWORDBREAKPROCEX** e **em \_ SETWORDBREAKPROCEX**.

È possibile usare il [**messaggio \_ FINDWORDBREAK em**](em-findwordbreak.md) per trovare le interruzioni di parola o per determinare i flag di classe e di interruzione di parola di un carattere. A sua volta, il controllo chiama la relativa procedura di Word break per ottenere le informazioni richieste.

Per determinare la riga in cui si trova un determinato carattere, è possibile usare il messaggio [**\_ EXLINEFROMCHAR em**](em-exlinefromchar.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 