---
description: Per supportare l'input penna nelle applicazioni, esistono due oggetti, che possono essere incorporati e supportati da qualsiasi contenitore OLE.
ms.assetid: fbd7bdf0-63b4-48d1-be91-eabbbb3f1618
title: Oggetti sInk e tInk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef7ed1c06d256fe8eda9fad4bf15afa19fcb833
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319146"
---
# <a name="sink-and-tink-objects"></a>Oggetti sInk e tInk

Per supportare l'input penna nelle applicazioni, esistono due oggetti, che possono essere incorporati e supportati da qualsiasi contenitore OLE. Vengono generati chiamando il metodo **Ink. ClipboardCopy (Rectangle, InkClipboardFormats, InkClipboardModes)** o il metodo **Ink. ClipboardCopy (Strokes, InkClipboardFormats, InkClipboardModes)** e sono:

-   Oggetto input penna del testo (tInk). Si tratta di un oggetto OLE che rappresenta l'input penna che dovrebbe formare parole. Un oggetto tInk consente la conversione dell'input penna manoscritto in testo, come il testo restituito da un riconoscimento o la scelta effettuata da un elenco di alternative di riconoscimento. Il colore e le dimensioni dell'input penna possono essere impostati a livello di codice e possono essere basati sugli attributi del testo intorno all'oggetto. L'oggetto tInk è destinato a contenere una singola parola. L'oggetto tInk è un piccolo oggetto leggero che può eseguire semplici operazioni come il rendering (dato un handle a un contesto di dispositivo (HDC) e un RECT) e la persistenza (dato un flusso). L'uso di un oggetto tInk consente un'esperienza utente trasparente quando si lavora in un'applicazione che usa l'input della grafia e del testo.
-   Oggetto sketch Ink (sInk). Si tratta di un oggetto OLE che rappresenta l'input penna che non si prevede di creare parole. Un oggetto sInk viene interpretato come un disegno. Un oggetto sInk è utile anche per rappresentare più parole.

Questi oggetti possono essere utilizzati per l'interoperabilità tra le applicazioni, inserendoli nello slot oggetto OLE negli Appunti o incorporando tali oggetti in formato RTF (Rich Text Format).

È possibile usare gli oggetti tInk e sInk nei modi seguenti:

-   Entrambi gli oggetti tInk e sInk sono supportati in Microsoft Word 2002. Gli utenti possono inserire input penna in un documento di Word usando i pannelli di input di testo di scrittura e disegno forniti in Word 2002. Questo input penna viene incorporato nel file di Word come oggetto OLE con il CLSID dell'oggetto sInk o tInk.
-   Il controllo [InkEdit](/previous-versions/ms552265(v=vs.100)) di Tablet PC usa l'oggetto Tink. Il controllo InkEdit è una sottoclasse del controllo [RichTextBox](/dotnet/api/system.windows.forms.richtextbox?view=netcore-3.1) standard. L'input penna viene inserito nel flusso RTF del controllo InkEdit come oggetto tInk.
-   Quando un'applicazione sposta un oggetto [input penna](/previous-versions/aa515768(v=msdn.10)) selezionato negli Appunti, lo slot degli appunti degli oggetti OLE contiene un oggetto OLE TInk o sink.

Ad esempio, l'applicazione può riconoscere la grafia e contrassegnare un oggetto [input penna](/previous-versions/aa515768(v=msdn.10)) come oggetto Tink. Quindi, se si seleziona una parola in input penna e la si copia e incolla in Word, le alternative per tale parola vengono visualizzate in Word 2002.

> [!Note]  
> Il supporto per gli Appunti della piattaforma Tablet PC seleziona automaticamente il flag EMF (Enhanced Metafile) quando si inserisce un oggetto sInk o tInk negli Appunti come oggetto OLE. L'oggetto stesso viene archiviato negli Appunti negli slot di incorporamento dell'origine e del descrittore dell'oggetto.

 

Come altro esempio, usando l'oggetto sInk, è possibile disegnare uno schizzo di input penna in un'applicazione, copiare e incollare lo sketch in Word 2002, quindi modificare il disegno usando il pannello di input di Tablet PC in Word.

Per contenere correttamente gli oggetti tInk, un'applicazione deve implementare il supporto del contenitore OLE per gli oggetti incorporati. Quindi, per fare in modo che il contenitore supporti completamente tInk, è necessario istituire:

-   Modifiche al codice per trova e Sostituisci. Anziché ignorare gli oggetti incorporati nella ricerca, è necessario interrogare questi oggetti per il tipo. Se sono un oggetto tInk, è necessario crearne un'istanza ed eseguire una query per ottenere il testo corrispondente.
-   Modifiche al comportamento di selezione. La selezione degli oggetti tInk non dovrebbe mai essere visualizzata con handle di ridimensionamento. Devono essere selezionati nello stesso modo in cui il testo è selezionato nel documento. Il codice di selezione per gli oggetti deve rilevare se il tipo è tInk e visualizzare la selezione in modo appropriato.
-   Uso delle proprietà di ambiente. Le proprietà di ambiente, ad esempio la dimensione del carattere, il colore e la formattazione in grassetto, devono essere trasmesse all'oggetto tInk. L'applicazione di queste proprietà modifica la larghezza dell'input penna a mano, quindi è necessario un aggiornamento delle dimensioni chiamando il [**Metodo GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) o il metodo [IOleObject:: GetExtent](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) .
-   Eseguire l'override dell'elaborazione del metodo [IOleObject::D overb](/windows/win32/api/oleidl/nf-oleidl-ioleobject-doverb) predefinito. Questo consente la conversione in testo per passare un batch di oggetti tInk al riconoscimento, che può quindi suddividere le parole in segmenti di riconoscimento.

Per altre informazioni su come suddividere le parole in segmenti di riconoscimento, vedere [segmenti di riconoscimento](recognition-segments.md).

 

 
