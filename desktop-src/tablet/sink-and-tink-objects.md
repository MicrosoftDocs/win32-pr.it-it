---
description: Per facilitare il supporto dell'input penna nelle applicazioni, sono disponibili due oggetti , entrambi incorporati e supportati da qualsiasi contenitore OLE.
ms.assetid: fbd7bdf0-63b4-48d1-be91-eabbbb3f1618
title: Oggetti sInk e tInk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e25e1f258ac789382475666878c986f5053323a1b19bf8f4b6110c096f2fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091306"
---
# <a name="sink-and-tink-objects"></a>Oggetti sInk e tInk

Per facilitare il supporto dell'input penna nelle applicazioni, sono disponibili due oggetti , entrambi incorporati e supportati da qualsiasi contenitore OLE. Vengono prodotti chiamando il metodo **Ink.ClipboardCopy (Rectangle, InkClipboardFormats, InkClipboardModes)** o il metodo **Ink.ClipboardCopy (Strokes, InkClipboardFormats, InkClipboardModes)** e sono:

-   Oggetto input penna di testo (tInk). Si tratta di un oggetto OLE che rappresenta l'input penna che deve formare parole. Un oggetto tInk consente di convertire l'input penna scritto a mano in testo, come testo restituito da un riconoscitore o come scelta scelta da un elenco di alternative di riconoscimento. Il colore e le dimensioni dell'input penna possono essere impostati a livello di codice e possono essere basati sugli attributi del testo intorno all'oggetto. L'oggetto tInk deve contenere una singola parola. L'oggetto tInk è un piccolo oggetto leggero che può eseguire operazioni semplici come il rendering (dato un handle a un contesto di dispositivo (HDC) e un RECT) e la persistenza (dato un flusso). L'uso di un oggetto tInk consente un'esperienza utente uniforme quando si lavora in un'applicazione che usa input sia di scrittura manuale che di testo.
-   Disegnare un oggetto input penna (sInk). Si tratta di un oggetto OLE che rappresenta l'input penna che non deve formare parole. Un oggetto sInk viene interpretato come un disegno. Un oggetto sInk è utile anche per rappresentare più parole.

Questi oggetti possono essere utilizzati per l'interoperabilità tra applicazioni, inserendoli nello slot di oggetti OLE negli Appunti o incorporandoli in formato RTF (Rich Text Format).

È possibile usare gli oggetti tInk e sInk nei modi seguenti:

-   Entrambi gli oggetti tInk e sInk sono supportati in Microsoft Word 2002. Gli utenti possono inserire input penna in un documento di Word usando i pannelli di input di testo di scrittura e disegno forniti in Word 2002. Questo input penna viene incorporato nel file di Word come oggetto OLE con il CLSID dell'oggetto sInk o tInk.
-   Il controllo [InkEdit di](/previous-versions/ms552265(v=vs.100)) Tablet PC usa l'oggetto tInk. Il controllo InkEdit è una sottoclasse del [controllo RichTextBox](/dotnet/api/system.windows.forms.richtextbox?view=netcore-3.1) standard. L'input penna viene inserito nel flusso RTF del controllo InkEdit come oggetto tInk.
-   Quando un'applicazione sposta un oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) selezionato negli Appunti, lo slot Degli Appunti dell'oggetto OLE contiene un oggetto OLE tInk o sInk.

Ad esempio, l'applicazione può riconoscere la grafia e contrassegnare [qualsiasi oggetto Ink](/previous-versions/aa515768(v=msdn.10)) come oggetto tInk. Quindi, se si seleziona una parola nell'input penna e la si copia e la si incolla in Word, le alternative per tale parola vengono visualizzate in Word 2002.

> [!Note]  
> Il supporto degli Appunti della piattaforma Tablet PC seleziona automaticamente il flag Enhanced Metafile (EMF) quando si posiziona un oggetto sInk o tInk negli Appunti come oggetto OLE. L'oggetto stesso viene archiviato negli Appunti negli slot di origine di incorporamento e descrittore di oggetti.

 

Come altro esempio, usando l'oggetto sInk, è possibile disegnare uno sketch input penna in un'applicazione, copiare e incollare lo sketch in Word 2002 e quindi modificare il disegno usando il pannello input penna di Tablet PC in Word.

Per contenere correttamente gli oggetti tInk, un'applicazione deve implementare il supporto del contenitore OLE per gli oggetti incorporati. Quindi, per fare in modo che il contenitore supporti completamente tInk, è necessario:

-   Modifiche al codice per Trova e Sostituisci. Anziché ignorare gli oggetti incorporati nella ricerca, è necessario interrogare questi oggetti per il tipo. Se si tratta di un oggetto tInk, è necessario crearne un'istanza ed eseguire query per trovare il testo corrispondente.
-   Modifiche al comportamento di selezione. La selezione di oggetti tInk non deve mai essere visualizzata con i quadratini di ridimensionamento. Devono essere selezionati nello stesso modo in cui viene selezionato il testo nel documento. Il codice di selezione per gli oggetti deve rilevare se il tipo è tInk e visualizzare la selezione in modo appropriato.
-   Uso delle proprietà di ambiente. Le proprietà di ambiente, ad esempio le dimensioni del carattere, il colore e la formattazione in grassetto, devono essere trasmesse all'oggetto tInk. L'applicazione di queste proprietà modifica la larghezza dell'input penna scritto a mano, quindi è necessario un aggiornamento delle dimensioni chiamando il metodo [**GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) o il metodo [IOleObject::GetExtent.](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent)
-   Eseguire l'override [dell'elaborazione predefinita del metodo IOleObject::D oVerb.](/windows/win32/api/oleidl/nf-oleidl-ioleobject-doverb) Ciò consente alla conversione in testo di passare un batch di oggetti tInk al riconoscitore, che può quindi suddividere le parole in segmenti di riconoscimento.

Per altre informazioni sull'interruzione delle parole in segmenti di riconoscimento, vedere [Segmenti di riconoscimento.](recognition-segments.md)

 

 
