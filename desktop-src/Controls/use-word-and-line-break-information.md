---
title: Come usare le informazioni sulle parole e sulle interruzioni di riga
description: Un controllo Rich Edit chiama una funzione denominata routine di interruzione di parola per trovare le interruzioni tra le parole e per determinare dove può interrompere le righe.
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178770ce4a7206c18f6fbbc197d92e23ff0139ae637bd5f7ceb4159aee3270ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059691"
---
# <a name="how-to-use-word-and-line-break-information"></a>Come usare le informazioni sulle parole e sulle interruzioni di riga

Un controllo Rich Edit chiama una funzione denominata routine di interruzione di parola per trovare le interruzioni tra le parole e per determinare dove può interrompere le righe. Il controllo usa queste informazioni quando si eseguono operazioni di ritorno a capo automatico e durante l'elaborazione di combinazioni di tasti CTRL+FRECCIA SINISTRA e CTRL+FRECCIA DESTRA. Un'applicazione può inviare messaggi a un controllo Rich Edit per sostituire la routine di interruzione di parola predefinita, recuperare le informazioni sull'interruzione di parola e determinare la riga su cui si trova un determinato carattere.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="use-word-and-line-break-information"></a>Usare le informazioni sulle interruzioni di riga e di parola

Le procedure di interruzione di parola per i controlli Rich Edit sono simili a quelle per i controlli di modifica, ma hanno funzionalità aggiuntive: le procedure di interruzione di parola per entrambi i tipi di controlli possono determinare se un carattere è un delimitatore e possono trovare l'interruzione di parola più vicina prima o dopo la posizione specificata. Un delimitatore è un carattere che contrassegna la fine di una parola, ad esempio uno spazio. In genere, in un controllo di modifica, un'interruzione di parola si verifica solo dopo i delimitatori. Tuttavia, regole diverse si applicano alla maggior parte delle lingue asiatiche.

Le procedure di interruzione di parola per i controlli Rich Edit raggruppano anche i caratteri in classi di caratteri, ognuna identificata da un valore nell'intervallo compreso tra 0x00 e 0x0F. Le interruzioni si verificano dopo i delimitatori o tra caratteri di classi diverse. Una routine di interruzione di parola con classi diverse per caratteri alfanumerici e di punteggiatura troverà quindi due interruzioni di parola nella stringa "Win.doc" (prima e dopo il punto).

La classe di un carattere può essere combinata con zero o più flag di interruzione di parola per formare un valore a 8 bit. Quando si eseguono operazioni di ritorno a capo automatico, un controllo Rich Edit usa i flag di interruzione delle parole per determinare dove può interrompere le righe. Rich Edit usa i flag di word break seguenti.



| Flag            | Descrizione                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| WBF \_ BREAKAFTER | Le righe possono essere interrotte dopo il carattere.                                                                                          |
| WBF \_ BREAKLINE  | Il carattere è un delimitatore. I delimitatori contrassegnano le estremità delle parole. Le righe possono essere interrotte dopo i delimitatori.                            |
| WBF \_ ISWHITE    | Il carattere è uno spazio vuoto. Gli spazi vuoti finali non sono inclusi nella lunghezza di una riga durante il ritorno a capo. |



 

Il valore WBF BREAKAFTER viene usato per consentire il ritorno a capo dopo un carattere che non contrassegna la fine di una parola, ad esempio \_ un trattino.

È possibile sostituire la routine di interruzione di parola predefinita per un controllo Rich Edit con una procedura personale usando il messaggio [**EM \_ SETWORDBREAKPROC.**](em-setwordbreakproc.md) Per altre informazioni sulle procedure di word break, vedere la descrizione della [*funzione EditWordBreakProc.*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)

> [!Note]  
> Questa sostituzione non è consigliata per Microsoft Rich Edit 2.0 e versioni successive, a causa della complessità dell'interruzione delle parole multilingue.

 

Per Microsoft Rich Edit 1.0, è possibile usare il messaggio [**EM \_ SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) per sostituire la routine di word break estesa predefinita con una [*funzione EditWordBreakProcEx.*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) Questa funzione fornisce informazioni aggiuntive sul testo, ad esempio il set di caratteri. È possibile usare il [**messaggio EM \_ GETWORDBREAKPROCEX**](em-getwordbreakprocex.md) per recuperare l'indirizzo della routine di word break estesa corrente. Si noti che Microsoft Rich Edit 2.0 e versioni successive non *supportaNo EditWordBreakProcEx,* **EM \_ GETWORDBREAKPROCEX** e **EM \_ SETWORDBREAKPROCEX**.

È possibile usare il [**messaggio EM \_ FINDWORDBREAK**](em-findwordbreak.md) per trovare le interruzioni di parola o per determinare la classe di un carattere e i flag di interruzione di parola. A sua volta, il controllo chiama la routine di word break per ottenere le informazioni richieste.

Per determinare su quale riga cade un determinato carattere, è possibile usare il [**messaggio EM \_ EXLINEFROMCHAR.**](em-exlinefromchar.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 