---
description: Nell'esempio Advanced Recognition sono illustrate le funzionalità avanzate del Application Programming Interface di automazione dei Tablet PC Microsoft (API) utilizzato per il riconoscimento della grafia.
ms.assetid: 4c9b9f31-c317-43fd-8404-35295b41d093
title: Esempio di riconoscimento avanzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e23a078ded9c6967f8e45780f8cb3a739b246f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749119"
---
# <a name="advanced-recognition-sample"></a>Esempio di riconoscimento avanzato

Nell'esempio Advanced Recognition sono illustrate le funzionalità avanzate del Application Programming Interface di automazione dei Tablet PC Microsoft (API) utilizzato per il riconoscimento della grafia.

Esso comprende le seguenti funzionalità:

-   Enumerazione del riconoscimento installato
-   Creazione di un contesto di riconoscimento con una lingua specifica
-   Utilizzo dell'oggetto Recognizer
-   Impostazione del controllo di riconoscimento e degli elenchi di parole
-   Uso delle guide per migliorare la qualità del riconoscimento
-   Riconoscimento in background dinamico
-   Riconoscimento movimenti

Le interfacce utilizzate sono: [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer), **IInkRecoContext**, [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult), **IInkRecognitionGuide**, **IInkWordList**, [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture), **IInkCollector**, **IInkDisp**, **IInkRenderer**, **IInkDrawingAttributes**, **IInkStrokes** e **IInkStroke**.

## <a name="ink-and-project-headers"></a>Intestazioni input penna e progetto

Includere innanzitutto le intestazioni per le interfacce di automazione dei Tablet PC. Queste vengono installate con Tablet PC Platform SDK. Il file TpcError. h contiene le definizioni dei codici di errore dell'API Tablet PC.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
#include <TpcError.h>
```



Il file EventSinks. h definisce le interfacce **IInkEventsImpl** e **IInkRecognitionEventsImpl** e imposta gli eventi [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md), [**Stroke**](inkcollector-stroke.md)e [**gesture**](inkcollector-gesture.md) .


```C++
#include "EventSinks.h"
```



Il file ChildWnds. h contiene le definizioni delle classi **CInkInputWnd** e **CRecoOutputWnd**, derivate dal CWindowImpl di ATL e utilizzate per la creazione delle finestre figlio dell'esempio.


```C++
#include "ChildWnds.h"
```



Il file AdvReco. h dichiara la classe **CAdvRecoApp** , che è la classe della finestra dell'applicazione per questo esempio.


```C++
#include "AdvReco.h"
```



## <a name="initializing-the-application-window"></a>Inizializzazione della finestra dell'applicazione

Tramite il metodo della finestra viene `Run` impostato l'oggetto **CAdvRecoApp** , vengono caricati il menu e l'icona per la finestra, viene creato un oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) per il riconoscimento predefinito e viene avviato il ciclo di messaggi della finestra.

Il metodo **OnCreate** della finestra gestisce l'evento di **\_ creazione WM** e crea le finestre figlio. Un oggetto [**InkCollector**](inkcollector-class.md) si connette all'origine eventi dell'agente di raccolta input penna e Abilita input penna nella finestra di input. Viene quindi creato un oggetto [**InkRecognizerGuide**](inkrecognizerguide-class.md) e viene utilizzata la proprietà [**renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer) dell'agente di raccolta input penna per convertire i rettangoli della casella della Guida di riconoscimento nello spazio di input penna. Infine, il metodo **OnCreate** crea un oggetto [**InkWord**](inkwordlist-class.md) .

## <a name="handling-ink-collector-events"></a>Gestione degli eventi dell'agente di raccolta input penna

Il metodo **OnStroke** della finestra gestisce l'evento [**Stroke**](inkcollector-stroke.md) dell'agente di raccolta input penna. Il nuovo oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) viene aggiunto al [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) della proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) dell'agente di raccolta input penna.

Il metodo **Ongesto** della finestra gestisce l'evento del [**movimento**](inkcollector-gesture.md) dell'agente di raccolta input penna. Il metodo **OnGesture** identifica il movimento, usando prima il movimento di confidenza più elevato e controlla se la finestra supporta questo particolare movimento. Se il movimento è supportato, il rettangolo di delimitazione del movimento viene invalidato, perché il movimento viene rimosso dalla raccolta Strokes. Se il movimento non è supportato, l'evento di **movimento** viene annullato, causando la generazione di un evento [**Stroke**](inkcollector-stroke.md) da parte dell'agente di raccolta input penna. Infine, la finestra risultati viene aggiornata.

## <a name="handling-recognizer-context-events"></a>Gestione degli eventi di contesto del riconoscimento

Il metodo **OnRecognitionWithAlternates** della finestra gestisce l'evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) del contesto del riconoscitore. Il metodo **OnRecognitionWithAlternates** Visualizza i risultati del riconoscimento nella finestra risultati.

## <a name="handling-menu-commands"></a>Gestione dei comandi di menu

Il metodo **Onrecognizer** della finestra gestisce i comandi nel menu Recognizer. Se è stato selezionato il comando **predefinito** , per recuperare il riconoscimento predefinito viene usato il metodo [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) di [dagli oggetti InkRecognizer](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) . in caso contrario, viene recuperato il riconoscimento selezionato. Viene quindi creato e utilizzato un contesto di riconoscimento e vengono aggiornati i menu e la barra di stato.

Il metodo **OnFactoidWordlist** della finestra gestisce il comando **use WordList** **nel menu del controllo dell'oggetto** . La proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contesto di riconoscimento è impostata su **null** per reimpostare il contesto del riconoscimento. Se l'opzione **use WordList** è disattivata, la proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del contesto del riconoscitore viene impostata su **null**. in caso contrario, la proprietà **WordList** del contesto del riconoscitore viene impostata sull'oggetto [**InkWord**](inkwordlist-class.md) creato nel metodo **OnCreate** . Infine, il [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dell'agente di raccolta input penna viene ricollegato al contesto del riconoscimento, viene chiamato il metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contesto di riconoscimento e il menu viene aggiornato.

Il metodo **OnFactoid** della finestra gestisce i comandi del controllo dell'oggetto **nel menu del controllo dell'oggetto** . Prima imposta la proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contesto del riconoscitore su **null**, imposta [**la proprietà del**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) controllo del contesto del riconoscitore sul controllo del controllo selezionato e riassegna il [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dell'agente di raccolta input penna al contesto del riconoscimento. Se l' [oggetto del controllo del controllo](factoid-constants.md) è supportato dal contesto del riconoscimento, viene chiamato il metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contesto del riconoscitore; in caso contrario, viene visualizzato un messaggio di errore. Infine, il menu e la barra di stato vengono aggiornati.

Il metodo **OnGuide** della finestra gestisce i comandi nel menu della **Guida** . Se il contesto di riconoscimento supporta le opzioni della guida, il metodo **OnGuide** imposta la proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contesto del riconoscitore su **null**, imposta la proprietà [**guide**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) del contesto di riconoscimento sull'impostazione della guida selezionata, riassegna [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dell'agente di raccolta input penna al contesto del riconoscimento e chiama il metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contesto di riconoscimento. In caso contrario, viene visualizzato un messaggio di errore. Infine, la finestra di input, il menu e la barra di stato vengono aggiornati.

Il metodo **Onmode** della finestra gestisce i comandi nel menu **modalità** . Viene disabilitato l'agente di raccolta input penna, viene aggiornata la proprietà [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) dell'agente di raccolta input penna, viene aggiornato il menu e vengono visualizzati o nascosti gli elenchi di movimenti. Infine, l'agente di raccolta input penna è abilitato.

Il metodo **Onrecognize** della finestra gestisce il comando **Recognize** nel menu di input penna. Chiama il metodo [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) del contesto del riconoscitore per evitare che l'input penna venga aggiunto al contesto del riconoscimento. Questo è talvolta necessario, in quanto non tutti i riconoscitori supportano il riconoscimento parziale. Chiama quindi il metodo [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) del contesto di riconoscimento e passa i risultati al metodo **OnRecognitionWithAlternates** della finestra. Infine, il [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dell'agente di raccolta input penna viene riassegnato al contesto del riconoscimento.

Il metodo **OnClear** della finestra gestisce il comando **Clear** nel menu di **input penna** . Elimina i tratti dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) dell'agente di raccolta input penna, rilascia l'insieme di tratti obsoleti e ne crea uno nuovo per la proprietà **Ink** dell'agente di raccolta input penna e collega la nuova raccolta Strokes al contesto del riconoscimento.

Il metodo **OnExit** della finestra gestisce il comando **Exit** nel menu **Ink** e genera l' \_ evento di chiusura WM.

## <a name="helper-methods"></a>Metodi helper

Il metodo **LoadMenu** della finestra viene chiamato dal metodo **Run** della finestra e aggiunge l'elenco dei riconoscitori supportati e l'elenco di factoids supportati nel menu. Viene innanzitutto recuperato il [dagli oggetti InkRecognizer](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)). Scorre quindi i riconoscitori disponibili e seleziona solo quelli che dispongono di un elenco di lingue nella proprietà **Languages** , che aggiunge al menu **Recognizer** . Infine, **il menu del controllo dell'oggetto** viene popolato con l'elenco di factoids definito come costante globale.

Il metodo **UseRecognizer** della finestra viene chiamato dal metodo **onrecognizer** della finestra quando l'utente seleziona un nuovo riconoscimento. Viene creato un contesto di riconoscimento, viene scollegato il contesto precedente dal sink di evento Recognizer, viene cancellato e rilasciato il contesto precedente e il nuovo contesto viene collegato al sink di evento Recognizer.

Quindi, il metodo **UseRecognizer** controlla la proprietà [**capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) del riconoscitore, che restituisce un valore [**InkRecognizerCapabilities**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities) . Se il riconoscimento supporta l'input rigato, il comando **linee** nel menu **Guida** è abilitato. Se il riconoscimento supporta l'input boxed, il comando **Boxes** è abilitato. Se il riconoscimento non supporta l'input libero, il comando **None** è disabilitato. Se la selezione della Guida corrente non è supportata, viene aggiornata sia la proprietà [**guide**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) del contesto di riconoscimento che il menu.

Quindi, il metodo **UseRecognizer** tenta di impostare [**le proprietà dell'**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) oggetto [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) e del controllo del contesto del contesto del riconoscimento. Se una delle due impostazioni non è supportata dal riconoscimento, viene usato il valore predefinito e il menu viene aggiornato.

Infine, il metodo **UseRecognizer** connette la proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) dell'oggetto [**InkDisp**](inkdisp-class.md) dell'agente di raccolta input penna al contesto del riconoscimento, imposta il tipo di carattere della finestra di output su uno supportato dalla lingua del riconoscimento, Reimposta la finestra di output e aggiorna i risultati del riconoscimento chiamando il metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contesto del riconoscitore.

Il metodo **Getgesturename** della finestra viene chiamato dal metodo **ongesto** della finestra. Viene eseguita la ricerca del movimento e viene restituito un indice al nome del movimento, che viene archiviato in una tabella di stringhe nel file AdvReco. RC.

 

 
