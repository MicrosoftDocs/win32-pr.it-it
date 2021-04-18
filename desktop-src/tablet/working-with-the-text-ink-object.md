---
description: Per supportare l'input penna nelle applicazioni, esistono due oggetti, che possono essere incorporati e supportati da qualsiasi contenitore OLE, l'oggetto input penna (tInk) e l'oggetto sketch Ink (sInk).
ms.assetid: 0202e91c-c7a0-4e7b-a1c6-a2f58c11c0be
title: Utilizzo dell'oggetto Text Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082323f7e67e76f7ae39c6b592a86f2be0945a86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307948"
---
# <a name="working-with-the-text-ink-object"></a>Utilizzo dell'oggetto Text Ink

Per supportare l'input penna nelle applicazioni, esistono due oggetti, che possono essere incorporati e supportati da qualsiasi contenitore OLE, l'oggetto input penna (tInk) e l'oggetto sketch Ink (sInk).

L'oggetto Ink di testo è un oggetto OLE che rappresenta l'input penna che dovrebbe formare parole. Un oggetto input penna di testo consente di convertire l'input penna a mano in testo scegliendo da un elenco di alternative. Il colore e le dimensioni dell'oggetto input penna possono essere impostati a livello di codice e possono essere basati sugli attributi del testo intorno all'oggetto. L'oggetto input penna è destinato a contenere una singola parola.

L'oggetto input penna di testo supporta il set standard di interfacce OLE necessarie per l'incorporamento e il supporto degli Appunti. L'interfaccia [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) legge e scrive in un flusso in formato ISF (Ink Serialized Format). L'oggetto input penna testo fornisce l'interfaccia [**IInkLineInfo**](/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo) per accedere alle proprietà di visualizzazione e all'elenco dei risultati del riconoscimento.

È possibile utilizzare l'oggetto input penna per l'interoperabilità tra le applicazioni inserendolo nello slot oggetto OLE negli Appunti, incorporando il testo in formato RTF o rendendolo permanente in un flusso ISF.

Un oggetto input penna di testo può essere generato nei modi seguenti.

-   Il controllo [InkEdit](inkedit-control-reference.md) utilizza l'oggetto input penna di testo. La funzionalità del controllo InkEdit è un set avanzato di funzionalità di controllo RichEdit standard. L'input penna viene inserito nel flusso RTF del controllo InkEdit come oggetto Ink di testo.
-   Quando un'applicazione copia un [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) o un oggetto [InkEdit](inkedit-control-reference.md) negli Appunti e il formato di [**Enumerazione InkClipboardFormats**](/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats) è impostato, lo slot degli appunti degli oggetti OLE contiene un oggetto OLE input penna.
-   Il pannello input penna di Tablet PC può generare oggetti di testo.

Ad esempio, l'applicazione può riconoscere la grafia e aggiungere il risultato del riconoscimento ai tratti. Quindi, se si copiano e si incollano i tratti in Microsoft Word come oggetto input penna, le alternative per tale parola sono disponibili in Word 2003 e versioni successive.

Per contenere correttamente oggetti input penna, un'applicazione deve implementare il supporto del contenitore OLE per gli oggetti incorporati. Quindi, per fare in modo che il contenitore supporti completamente l'input penna del testo, è necessario istituire:

-   Modifiche all'applicazione per trova e Sostituisci. Anziché ignorare gli oggetti incorporati nella ricerca, è necessario interrogare questi oggetti per il tipo. Se si tratta di un oggetto input penna, è necessario crearne un'istanza e sottoporre a query il testo corrispondente.
-   Modifiche al comportamento di selezione. La selezione di oggetti input penna di testo non deve mai essere visualizzata con handle di ridimensionamento. Devono essere selezionati nello stesso modo in cui il testo è selezionato nel documento. Il codice di selezione per gli oggetti deve rilevare se il tipo è input penna e visualizzare la selezione in modo appropriato.
-   Uso delle proprietà di ambiente. Le proprietà di ambiente, ad esempio la dimensione del carattere, il colore e la formattazione in grassetto, devono essere trasmesse all'oggetto Ink di testo. L'applicazione di queste proprietà modifica la larghezza dell'input penna a mano, quindi è necessario un aggiornamento delle dimensioni chiamando il metodo [**IInkLineInfo:: GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) o [**IOleObject:: GetExtent**](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) .

## <a name="in-this-section"></a>Contenuto della sezione

-   [Conversione di un oggetto input penna in input penna](converting-a-text-ink-object-to-ink.md)
-   [API Text Ink](text-ink-apis.md)
-   [Oggetti sInk e tInk](sink-and-tink-objects.md)

 

 
