---
title: Operazioni sugli Appunti
description: Una finestra deve usare gli Appunti per tagliare, copiare o incollare i dati. Una finestra inserisce i dati negli Appunti per le operazioni taglia e copia e recupera i dati dagli Appunti per le operazioni Incolla.
ms.assetid: 27f9142c-3154-4de5-aea6-3c53f7e940ec
keywords:
- Windows Interfaccia utente,Appunti
- Appunti, finestre
- Appunti, taglio dei dati
- Appunti, copia di dati
- Appunti, incolla dei dati
- Appunti, finestra proprietario
- Appunti, rendering ritardato
- Appunti, memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a0dfe82f6130f0435521ac4e17cf8e8b7162115074f7b3ff716187730f8bb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545435"
---
# <a name="clipboard-operations"></a>Operazioni sugli Appunti

Una finestra deve usare gli Appunti per tagliare, copiare o incollare i dati. Una finestra inserisce i dati negli Appunti per le operazioni taglia e copia e recupera i dati dagli Appunti per le operazioni Incolla. Le sezioni seguenti descrivono queste operazioni e i problemi correlati.

Per inserire o recuperare dati dagli Appunti, una finestra deve prima aprire gli Appunti usando la [**funzione OpenClipboard.**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) Gli Appunti possono essere aperti in una sola finestra alla volta. Per individuare la finestra in cui sono aperti gli Appunti, chiamare la [**funzione GetOpenClipboardWindow.**](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow) Al termine, la finestra deve chiudere gli Appunti chiamando la [**funzione CloseClipboard.**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard)

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Operazioni taglia e copia](#cut-and-copy-operations)
-   [Operazioni Incolla](#paste-operations)
-   [Proprietà degli Appunti](#clipboard-ownership)
-   [Rendering ritardato](#delayed-rendering)
-   [Memoria e Appunti](#memory-and-the-clipboard)

## <a name="cut-and-copy-operations"></a>Operazioni taglia e copia

Per inserire informazioni negli Appunti, una finestra cancella prima di tutto il contenuto degli Appunti precedente usando la [**funzione EmptyClipboard.**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) Questa funzione invia il messaggio [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) al proprietario degli Appunti precedente, libera le risorse associate ai dati negli Appunti e assegna la proprietà degli Appunti alla finestra in cui sono aperti gli Appunti. Per scoprire quale finestra è proprietaria degli Appunti, chiama la [**funzione GetClipboardOwner.**](/windows/win32/api/winuser/nf-winuser-getclipboardowner)

Dopo aver svuotato gli Appunti, la finestra inserisce i dati negli Appunti nel maggior numero possibile di formati degli Appunti, ordinati dal formato degli Appunti più descrittivo al meno descrittivo. Per ogni formato, la finestra chiama la [**funzione SetClipboardData,**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) specificando l'identificatore di formato e un handle di memoria globale. L'handle di memoria può essere NULL, a indicare che la finestra esegue il rendering dei dati su richiesta. Per altre informazioni, vedere [Rendering ritardato.](#delayed-rendering)

## <a name="paste-operations"></a>Operazioni Incolla

Per recuperare le informazioni incollate dagli Appunti, una finestra determina innanzitutto il formato degli Appunti da recuperare. In genere, una finestra enumera i formati degli Appunti disponibili usando la [**funzione EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) e usa il primo formato riconosciuto. Questo metodo seleziona il formato migliore disponibile in base alla priorità impostata quando i dati sono stati inseriti negli Appunti.

In alternativa, una finestra può usare [**la funzione GetPriorityClipboardFormat.**](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat) Questa funzione identifica il formato degli Appunti migliore disponibile in base a una priorità specificata. Una finestra che riconosce un solo formato degli Appunti può semplicemente determinare se tale formato è disponibile usando la [**funzione IsClipboardFormatAvailable.**](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable)

Dopo aver determinato il formato degli Appunti da usare, una finestra chiama la [**funzione GetClipboardData.**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) Questa funzione restituisce l'handle a un oggetto memoria globale contenente dati nel formato specificato. Una finestra può bloccare brevemente l'oggetto memoria per esaminare o copiare i dati. Tuttavia, una finestra non deve liberare l'oggetto o lasciarlo bloccato per un lungo periodo di tempo.

## <a name="clipboard-ownership"></a>Proprietà degli Appunti

Il *proprietario degli* Appunti è la finestra associata alle informazioni negli Appunti. Una finestra diventa il proprietario degli Appunti quando inserisce i dati negli Appunti, in particolare quando chiama la [**funzione EmptyClipboard.**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) La finestra rimane il proprietario degli Appunti fino a quando non viene chiusa o un'altra finestra svuota gli Appunti.

Quando gli Appunti vengono svuotati, il proprietario degli Appunti riceve un [**messaggio WM \_ DESTROYCLIPBOARD.**](wm-destroyclipboard.md) Di seguito sono riportati alcuni motivi per cui una finestra potrebbe elaborare questo messaggio:

-   Rendering ritardato della finestra di uno o più formati degli Appunti. In risposta al messaggio [**WM \_ DESTROYCLIPBOARD,**](wm-destroyclipboard.md) la finestra potrebbe liberare le risorse allocate per eseguire il rendering dei dati su richiesta. Per altre informazioni sul rendering dei dati, vedere [Rendering ritardato.](#delayed-rendering)
-   La finestra ha inserito i dati negli Appunti in un formato degli Appunti privato. I dati per i formati degli Appunti privati non vengono liberati dal sistema quando gli Appunti vengono svuotati. Pertanto, il proprietario degli Appunti deve liberare i dati alla ricezione del [**messaggio WM \_ DESTROYCLIPBOARD.**](wm-destroyclipboard.md) Per altre informazioni sui formati degli Appunti privati, vedere [Formati degli Appunti.](clipboard-formats.md)
-   La finestra ha inserito i dati negli Appunti usando il formato degli Appunti **CF \_ OWNERDISPLAY.** In risposta al messaggio [**WM \_ DESTROYCLIPBOARD,**](wm-destroyclipboard.md) la finestra potrebbe liberare le risorse usate per visualizzare le informazioni nella finestra del visualizzatore Appunti. Per altre informazioni su questo formato alternativo, vedere [Formato di visualizzazione proprietario.](about-the-clipboard.md)

## <a name="delayed-rendering"></a>Rendering ritardato

Quando si inserisce un formato degli Appunti negli Appunti, una finestra può ritardare il rendering dei dati in tale formato fino a quando non sono necessari. A tale scopo, un'applicazione può **specificare NULL** per *il parametro hData* della funzione [**SetClipboardData.**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) Ciò è utile se l'applicazione supporta diversi formati degli Appunti, alcuni o tutti richiedono molto tempo per il rendering. Passando un handle **NULL,** una finestra esegue il rendering di formati di Appunti complessi solo quando e se sono necessari.

Se una finestra ritarda il rendering di un formato degli Appunti, deve essere preparata per il rendering del formato su richiesta, purché sia il proprietario degli Appunti. Il sistema invia al proprietario degli Appunti un [**messaggio \_ RENDERFORMAT WM**](wm-renderformat.md) quando viene ricevuta una richiesta per un formato specifico di cui non è stato eseguito il rendering. Alla ricezione di questo messaggio, la finestra deve chiamare la [**funzione SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) per inserire un handle di memoria globale negli Appunti nel formato richiesto.

Un'applicazione non deve aprire gli Appunti prima di [**chiamare SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) in risposta al [**messaggio \_ RENDERFORMAT WM.**](wm-renderformat.md) L'apertura degli Appunti non è necessaria e qualsiasi tentativo avrà esito negativo perché gli Appunti sono attualmente mantenuti aperti dall'applicazione che ha richiesto il rendering del formato.

Se il proprietario degli Appunti sta per essere eliminato e ha ritardato il rendering di alcuni o tutti i formati degli Appunti, riceve il messaggio [**\_ WM RENDERALLFORMATS.**](wm-renderallformats.md) Alla ricezione di questo messaggio, la finestra dovrebbe aprire gli Appunti, verificare che sia ancora il proprietario degli Appunti con la [**funzione GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) e quindi inserire handle di memoria validi negli Appunti per tutti i formati degli Appunti forniti. In questo modo si garantisce che questi formati rimangano disponibili dopo l'eliminazione del proprietario degli Appunti.

A differenza di [**WM \_ RENDERFORMAT,**](wm-renderformat.md)un'applicazione che risponde a [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) deve aprire gli Appunti prima di chiamare [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) per inserire eventuali handle di memoria globali negli Appunti.

Tutti i formati degli Appunti di cui non viene eseguito il rendering in risposta al messaggio [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) non sono più disponibili per altre applicazioni e non vengono più enumerati dalle funzioni degli Appunti.

## <a name="memory-and-the-clipboard"></a>Memoria e Appunti

Un oggetto memoria da inserire negli Appunti deve essere allocato usando la [**funzione GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) con il flag **GMEM \_ MOVEABLE.**

Dopo che un oggetto memoria è stato inserito negli Appunti, la proprietà di tale handle di memoria viene trasferita al sistema. Quando gli Appunti vengono svuotati e l'oggetto memoria ha uno dei formati di Appunti seguenti, il sistema libera l'oggetto memoria chiamando la funzione specificata:



| Funzione per liberare un oggetto                             | Formato degli Appunti                                                                                                                                               |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile)<br/> | **CF \_ DSPENHMETAFILE**<br/> **CF \_ DSPMETAFILEPICT**<br/> **CF \_ ENHMETAFILE**<br/> **CF \_ METAFILEPICT**<br/>                            |
| [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)<br/>     | **CF \_ BITMAP**<br/> **CF \_ DSPBITMAP**<br/> **TAVOLOZZA \_ CF**<br/>                                                                              |
| [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree)<br/>        | **CF \_ DIB**<br/> **CF \_ DIBV5**<br/> **CF \_ DSPTEXT**<br/> **CF \_ OEMTEXT**<br/> **TESTO \_ CF**<br/> **CF \_ UNICODETEXT**<br/>   |
| Nessuno<br/>                                     | **CF \_ OWNERDISPLAY**<br/> Quando gli Appunti vengono svuotati da un oggetto **CF \_ OWNERDISPLAY,** l'applicazione stessa deve liberare l'oggetto memoria.<br/> |



 

 

