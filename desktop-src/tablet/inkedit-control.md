---
description: Il controllo InkEdit offre un modo semplice per acquisire, riconoscere e visualizzare l'input penna.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: Controllo InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa64c4452ba5d7f66cdc03a1148c02a12f3945f876d68ac240ff4473e8d50bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451322"
---
# <a name="inkedit-control"></a>Controllo InkEdit

Il [controllo InkEdit](inkedit-control-reference.md) offre un modo semplice per acquisire, riconoscere e visualizzare l'input penna.

Questa implementazione del [controllo InkEdit](inkedit-control-reference.md) è basata [**sul controllo RichEdit.**](/windows/desktop/api/richole/nn-richole-iricheditole) L'implementazione gestita (.NET Framework) [di InkEdit](/previous-versions/ms835842(v=msdn.10)) si basa sul [**controllo RichTextBox.**](/previous-versions/windows/)

Lo scopo principale del controllo [InkEdit](inkedit-control-reference.md) è raccogliere l'input penna, riconoscerlo e visualizzarlo in formato testo. Supporta inoltre la visualizzazione dell'input penna come oggetto incorporato con funzionalità di formattazione del testo, ad esempio grassetto e sottolineatura.

## <a name="gestures-and-correction"></a>Movimenti e correzione

[InkEdit](inkedit-control-reference.md) supporta i movimenti seguenti.



| Movimento                                                                    | Nome movimento              | Azione               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![movimento verso il basso a sinistra](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | In basso a sinistra<br/>      | Immettere<br/>     |
| ![movimento lungo verso il basso a sinistra](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | Lungo-sinistra verso il basso<br/> | Immettere<br/>     |
| ![movimento verso l'alto a destra](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | In alto a destra<br/>       | Scheda<br/>       |
| ![movimento verso l'alto verso destra e lungo.](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | Verso l'alto a destra e lungo<br/>  | Scheda<br/>       |
| ![movimento a destra](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | Destra<br/>          | Space<br/>     |
| ![movimento a sinistra](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | Sinistra<br/>           | Backspace<br/> |



 

Gli eventi di movimento che puoi gestire contengono informazioni su movimento, tratto e cursore che puoi usare per inviare testo [a InkEdit](inkedit-control-reference.md) o inserire dati negli Appunti.

[InkEdit](inkedit-control-reference.md) offre anche un'interfaccia utente di correzione che consente agli utenti di visualizzare e selezionare tra alternative, usare la tastiera su schermo e i riconoscitori di caratteri/lettere/blocchi.

## <a name="other-details"></a>Altri dettagli

[InkEdit è](inkedit-control-reference.md) progettato per funzionare bene in uno scenario di modulo per l'immissione e la modifica di testo su più righe. L'uso principale previsto per InkEdit è ottenere l'input di testo da un utente sotto forma di grafia. Per impostazione predefinita, l'input penna viene riconosciuto e al suo posto viene inserito testo. L'interfaccia utente predefinita per InkEdit è simile a quella del [**controllo RichTextBox,**](/previous-versions/windows/) tranne quando l'utente sta distogliendo l'input penna. È possibile visualizzare l'input penna originale anziché il testo. Tuttavia, l'input penna viene ridimensionato in base alle dimensioni correnti del carattere di input del controllo InkEdit e viene visualizzato inline con altro testo.

> [!Note]  
> Per motivi di sicurezza, è necessario utilizzare procedure standard per aprire o chiudere un file, trasmettere l'input/output e impostare la [**proprietà RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) [**o**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) Text.

 

Il [controllo InkEdit](inkedit-control-reference.md) è impostato per riconoscere l'input penna come testo per impostazione predefinita. Per consentire agli utenti di aggiungere input penna come input penna, impostare la [**proprietà InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) **su InsertAsInk.**

Per informazioni di riferimento dettagliate sul [controllo InkEdit,](inkedit-control-reference.md) vedere InkEdit.

> [!Note]  
> Se si usa il controllo [InkEdit](inkedit-control-reference.md) Win32 e lo si posiziona all'interno di una casella di gruppo, assicurarsi che la casella abbia uno stile trasparente. In caso contrario, InkEdit non è in grado di raccogliere input penna.

 

> [!Note]  
> Per assicurarsi che l'input penna venga visualizzato correttamente, chiamare il metodo [**Refresh**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) del controllo [InkEdit](inkedit-control-reference.md) quando riceve un [**evento HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) [**o VScroll.**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1)

 

Le sezioni seguenti illustrano in dettaglio l'uso [del controllo InkEdit:](inkedit-control-reference.md)

-   [Creazione di un'istanza di InkEdit](instantiating-inkedit.md)
-   [Confronto tra riconoscimento di parole e caratteri](word-vs--character-recognition.md)
-   [Visualizzazione dell'input penna come input penna](displaying-ink-as-ink.md)
-   [Uso di InkEdit nelle versioni precedenti di Windows](using-inkedit-on-earlier-versions-of-windows.md)
-   [Uso di un dizionario applicazioni con InkEdit](using-an-application-dictionary-with-inkedit.md)

 

