---
title: Operazioni degli Appunti
description: Una finestra deve usare gli Appunti per tagliare, copiare o incollare i dati. Una finestra inserisce i dati negli Appunti per le operazioni Taglia e copia e recupera i dati dagli Appunti per le operazioni Incolla.
ms.assetid: 27f9142c-3154-4de5-aea6-3c53f7e940ec
keywords:
- Interfaccia utente di Windows, appunti
- Appunti, Windows
- Appunti, taglio di dati
- Appunti, copia di dati
- Appunti, incolla di dati
- Appunti, finestra proprietaria
- Appunti, rendering ritardato
- Appunti, memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cb2c3451cf562b35b976e137a974e19892acbb3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338911"
---
# <a name="clipboard-operations"></a>Operazioni degli Appunti

Una finestra deve usare gli Appunti per tagliare, copiare o incollare i dati. Una finestra inserisce i dati negli Appunti per le operazioni Taglia e copia e recupera i dati dagli Appunti per le operazioni Incolla. Le sezioni seguenti descrivono le operazioni e i problemi correlati.

Per inserire dati o recuperare dati dagli Appunti, una finestra deve prima aprire gli Appunti utilizzando la funzione [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) . Gli Appunti possono essere aperti in una sola finestra alla volta. Per individuare la finestra con gli Appunti aperti, chiamare la funzione [**GetOpenClipboardWindow**](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow) . Al termine, la finestra deve chiudere gli Appunti chiamando la funzione [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

In questa sezione vengono descritti gli argomenti seguenti.

-   [Operazioni Taglia e copia](#cut-and-copy-operations)
-   [Operazioni Incolla](#paste-operations)
-   [Proprietà degli Appunti](#clipboard-ownership)
-   [Rendering ritardato](#delayed-rendering)
-   [Memoria e appunti](#memory-and-the-clipboard)

## <a name="cut-and-copy-operations"></a>Operazioni Taglia e copia

Per inserire informazioni negli Appunti, una finestra Cancella prima di tutto il contenuto degli appunti precedente tramite la funzione [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) . Questa funzione Invia il messaggio [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) al proprietario degli appunti precedente, libera le risorse associate ai dati negli Appunti e assegna la proprietà degli Appunti alla finestra con gli Appunti aperti. Per individuare la finestra proprietaria degli Appunti, chiamare la funzione [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) .

Dopo aver svuotato gli appunti, la finestra inserisce i dati negli Appunti nel maggior numero possibile di formati degli Appunti, ordinati dal formato degli appunti più descrittivo al meno descrittivo. Per ogni formato, la finestra chiama la funzione [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) , specificando l'identificatore di formato e un handle di memoria globale. L'handle di memoria può essere NULL, a indicare che la finestra esegue il rendering dei dati su richiesta. Per ulteriori informazioni, vedere [rendering ritardato](#delayed-rendering).

## <a name="paste-operations"></a>Operazioni Incolla

Per recuperare le informazioni di Incolla dagli Appunti, una finestra determina innanzitutto il formato degli Appunti da recuperare. In genere, una finestra enumera i formati degli appunti disponibili usando la funzione [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) e usa il primo formato riconosciuto. Questo metodo seleziona il formato migliore disponibile in base al set di priorità quando i dati sono stati inseriti negli Appunti.

In alternativa, una finestra può utilizzare la funzione [**GetPriorityClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat) . Questa funzione identifica il migliore formato degli appunti disponibili in base a una priorità specificata. Una finestra che riconosce solo un formato degli Appunti può semplicemente determinare se tale formato è disponibile tramite la funzione [**IsClipboardFormatAvailable**](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable) .

Dopo aver determinato il formato degli Appunti da usare, una finestra chiama la funzione [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) . Questa funzione restituisce l'handle a un oggetto memoria globale contenente i dati nel formato specificato. Una finestra può bloccare brevemente l'oggetto memoria per esaminare o copiare i dati. Tuttavia, una finestra non deve liberare l'oggetto o lasciarla bloccata per un lungo periodo di tempo.

## <a name="clipboard-ownership"></a>Proprietà degli Appunti

Il *proprietario degli Appunti* è la finestra associata alle informazioni negli Appunti. Una finestra diventa il proprietario degli Appunti quando inserisce i dati negli Appunti, in particolare quando chiama la funzione [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) . La finestra rimane il proprietario degli Appunti fino a quando non viene chiusa o un'altra finestra svuota gli Appunti.

Quando gli Appunti vengono svuotati, il proprietario degli Appunti riceve un messaggio [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) . Di seguito sono riportati alcuni dei motivi per cui una finestra potrebbe elaborare questo messaggio:

-   Il rendering ritardato della finestra di uno o più formati degli Appunti. In risposta al messaggio [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) , la finestra potrebbe liberare le risorse allocate per eseguire il rendering dei dati su richiesta. Per ulteriori informazioni sul rendering dei dati, vedere [rendering ritardato](#delayed-rendering).
-   La finestra posiziona i dati negli Appunti nel formato degli Appunti privati. I dati per i formati degli Appunti privati non vengono liberati dal sistema quando gli Appunti vengono svuotati. Il proprietario degli Appunti deve pertanto liberare i dati alla ricezione del messaggio [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) . Per ulteriori informazioni sui formati degli Appunti privati, vedere la pagina relativa ai [formati degli Appunti](clipboard-formats.md).
-   La finestra ha inserito i dati negli appunti usando il formato degli Appunti **\_ OWNERDISPLAY di CF** . In risposta al messaggio [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) , la finestra potrebbe liberare le risorse usate per visualizzare le informazioni nella finestra Visualizzatore Appunti. Per ulteriori informazioni su questo formato alternativo, vedere il [formato di visualizzazione del proprietario](about-the-clipboard.md).

## <a name="delayed-rendering"></a>Rendering ritardato

Quando si inserisce un formato degli Appunti negli Appunti, una finestra può ritardare il rendering dei dati in tale formato fino a quando non sono necessari i dati. A tale scopo, un'applicazione può specificare **null** per il parametro *HData* della funzione [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) . Questa operazione è utile se l'applicazione supporta diversi formati degli Appunti, alcuni o tutti i quali richiedono molto tempo per il rendering. Passando un handle **null** , una finestra esegue il rendering dei formati degli Appunti complessi solo quando e se sono necessari.

Se una finestra ritarda il rendering di un formato degli Appunti, deve essere preparato per eseguire il rendering del formato su richiesta per purché sia il proprietario degli Appunti. Il sistema invia al proprietario degli Appunti un messaggio [**WM \_ RENDERFORMAT**](wm-renderformat.md) quando viene ricevuta una richiesta per un formato specifico di cui non è stato eseguito il rendering. Alla ricezione di questo messaggio, la finestra deve chiamare la funzione [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) per inserire un handle di memoria globale negli Appunti nel formato richiesto.

Un'applicazione non deve aprire gli Appunti prima di chiamare [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) in risposta al messaggio [**WM \_ RENDERFORMAT**](wm-renderformat.md) . L'apertura degli Appunti non è necessaria e qualsiasi tentativo di eseguire questa operazione avrà esito negativo perché gli Appunti sono attualmente mantenuti aperti dall'applicazione che ha richiesto il rendering del formato.

Se il proprietario degli appunti sta per essere eliminato definitivamente e ha ritardato il rendering di alcuni o di tutti i formati degli Appunti, riceve il messaggio [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) . Al momento della ricezione di questo messaggio, la finestra deve aprire gli appunti, verificare che sia ancora il proprietario degli Appunti con la funzione [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) , quindi inserire gli handle di memoria validi negli Appunti per tutti i formati degli Appunti forniti. In questo modo si garantisce che questi formati rimangano disponibili dopo che il proprietario degli Appunti viene eliminato definitivamente.

A differenza di [**WM \_ RENDERFORMAT**](wm-renderformat.md), un'applicazione che risponde a [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) deve aprire gli Appunti prima di chiamare [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) per inserire tutti gli handle di memoria globale negli Appunti.

Tutti i formati degli Appunti di cui non viene eseguito il rendering in risposta al messaggio [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) non sono più disponibili per altre applicazioni e non vengono più enumerati dalle funzioni degli Appunti.

## <a name="memory-and-the-clipboard"></a>Memoria e appunti

Un oggetto memoria da inserire negli Appunti deve essere allocato usando la funzione [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) con il flag **GMEM \_ mobile** .

Dopo che un oggetto Memory è stato inserito negli Appunti, la proprietà dell'handle di memoria viene trasferita al sistema. Quando gli Appunti sono vuoti e l'oggetto Memory ha uno dei formati degli Appunti seguenti, il sistema libera l'oggetto memory chiamando la funzione specificata:



| Funzione per liberare oggetto                             | Formato degli Appunti                                                                                                                                               |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile)<br/> | **\_DSPENHMETAFILE CF**<br/> **\_DSPMETAFILEPICT CF**<br/> **\_ENHMETAFILE CF**<br/> **\_METAFILEPICT CF**<br/>                            |
| [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)<br/>     | **\_bitmap CF**<br/> **\_DSPBITMAP CF**<br/> **\_tavolozza CF**<br/>                                                                              |
| [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree)<br/>        | **\_DIB CF**<br/> **\_DIBV5 CF**<br/> **\_DSPTEXT CF**<br/> **\_OEMTEXT CF**<br/> **\_testo CF**<br/> **\_UNICODETEXT CF**<br/>   |
| Nessuno<br/>                                     | **\_OWNERDISPLAY CF**<br/> Quando gli Appunti vengono svuotati di un oggetto **CF \_ OWNERDISPLAY** , l'applicazione deve liberare l'oggetto Memory.<br/> |



 

 

