---
description: Per supportare il supporto dell'input penna nelle applicazioni, sono disponibili due oggetti, entrambi incorporati e supportati da qualsiasi contenitore OLE, l'oggetto input penna di testo (tInk) e l'oggetto input penna di sketch (sInk).
ms.assetid: 0202e91c-c7a0-4e7b-a1c6-a2f58c11c0be
title: Utilizzo dell'oggetto Input penna di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938d7e68795147913b64cad399f70ac6c1d2fdb06edc19e6d0c0b6c64add6422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449264"
---
# <a name="working-with-the-text-ink-object"></a>Utilizzo dell'oggetto Input penna di testo

Per supportare il supporto dell'input penna nelle applicazioni, sono disponibili due oggetti, entrambi incorporati e supportati da qualsiasi contenitore OLE, l'oggetto input penna di testo (tInk) e l'oggetto input penna di sketch (sInk).

L'oggetto input penna di testo è un oggetto OLE che rappresenta l'input penna che deve formare parole. Un oggetto input penna di testo consente di convertire l'input penna scritto a mano in testo scegliendo da un elenco di alternative. Il colore e le dimensioni dell'oggetto input penna di testo possono essere impostati a livello di codice e possono essere basati sugli attributi del testo intorno all'oggetto. L'oggetto input penna di testo deve contenere una singola parola.

L'oggetto input penna di testo supporta il set standard di interfacce OLE necessarie per l'incorporamento e il supporto degli Appunti. [**L'interfaccia IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) legge e scrive in un flusso in formato ISF (Ink Serialized Format). L'oggetto input penna di testo fornisce [**l'interfaccia IInkLineInfo**](/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo) per accedere alle proprietà di visualizzazione e all'elenco dei risultati del riconoscimento.

L'oggetto input penna di testo può essere usato per l'interoperabilità tra le applicazioni inserendolo nello slot di oggetti OLE negli Appunti, incorporarlo in RTF o conservarlo in un flusso ISF.

Un oggetto input penna di testo può essere generato nei modi seguenti.

-   Il [controllo InkEdit](inkedit-control-reference.md) usa l'oggetto input penna di testo. La funzionalità del controllo InkEdit è un super-set della funzionalità standard del controllo RichEdit. L'input penna viene inserito nel flusso RTF del controllo InkEdit come oggetto input penna di testo.
-   Quando un'applicazione copia [un oggetto InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) o [InkEdit](inkedit-control-reference.md) negli Appunti e il formato di enumerazione [**InkClipboardFormats**](/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats) è impostato, lo slot Appunti dell'oggetto OLE contiene un oggetto OLE input penna di testo.
-   Pannello di input penna di Tablet PC può generare oggetti input penna di testo.

Ad esempio, l'applicazione può riconoscere la grafia e aggiungere il risultato del riconoscimento ai tratti. Quindi, se si copiano e incollano i tratti in Microsoft Word come oggetto input penna di testo, le alternative per tale parola sono disponibili in Word 2003 e versioni successive.

Per contenere correttamente gli oggetti input penna di testo, un'applicazione deve implementare il supporto del contenitore OLE per gli oggetti incorporati. Quindi, per fare in modo che il contenitore supporti completamente l'input penna, è necessario:

-   Modifiche all'applicazione per Trova e Sostituisci. Anziché ignorare gli oggetti incorporati nella ricerca, è necessario interrogare questi oggetti per il tipo. Se si tratta di un oggetto input penna di testo, è necessario crearne un'istanza ed eseguire query per il testo corrispondente.
-   Modifiche al comportamento di selezione. La selezione di oggetti input penna di testo non deve mai essere visualizzata con quadratini di ridimensionamento. Devono essere selezionati nello stesso modo in cui viene selezionato il testo nel documento. Il codice di selezione per gli oggetti deve rilevare se il tipo è input penna e visualizzare la selezione in modo appropriato.
-   Uso delle proprietà di ambiente. Le proprietà di ambiente, ad esempio le dimensioni del carattere, il colore e la formattazione in grassetto, devono essere trasmesse all'oggetto input penna di testo. L'applicazione di queste proprietà modifica la larghezza dell'input penna scritto a mano, quindi è necessario un aggiornamento delle dimensioni chiamando il metodo [**IInkLineInfo::GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) o [**IOleObject::GetExtent.**](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent)

## <a name="in-this-section"></a>Contenuto della sezione

-   [Conversione di un oggetto input penna di testo in input penna](converting-a-text-ink-object-to-ink.md)
-   [API Input penna di testo](text-ink-apis.md)
-   [Oggetti sInk e tInk](sink-and-tink-objects.md)

 

 
