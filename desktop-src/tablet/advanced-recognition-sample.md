---
description: L'esempio di riconoscimento avanzato illustra le funzionalità avanzate dell'API (Application Programming Interface) di Automazione di Microsoft Tablet PC usata per il riconoscimento della grafia.
ms.assetid: 4c9b9f31-c317-43fd-8404-35295b41d093
title: Esempio di riconoscimento avanzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7c56a76e66870fdd881ff1d51c4b54acb929765fb21d45857d67c252b01628
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675629"
---
# <a name="advanced-recognition-sample"></a>Esempio di riconoscimento avanzato

L'esempio di riconoscimento avanzato illustra le funzionalità avanzate dell'API (Application Programming Interface) di Automazione di Microsoft Tablet PC usata per il riconoscimento della grafia.

Esso comprende le seguenti funzionalità:

-   Enumerazione del sistema di riconoscimento installato
-   Creazione di un contesto di riconoscimento con un linguaggio specifico
-   Uso dell'oggetto riconoscitore
-   Impostazione del factoid di riconoscimento e degli elenchi di parole
-   Uso di guide per migliorare la qualità del riconoscimento
-   Riconoscimento dinamico dello sfondo
-   Riconoscimento dei movimenti

Le interfacce usate sono: [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer), **IInkRecoContext**, [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult), **IInkRecognitionGuide**, **IInkWordList**, [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture), **IInkCollector**, **IInkDisp**, **IInkRenderer**, **IInkDrawingAttributes**, **IInkStrokes** e **IInkStroke**.

## <a name="ink-and-project-headers"></a>Intestazioni input penna Project input penna

Includere prima di tutto le intestazioni per le interfacce di automazione di Tablet PC. Vengono installati con Tablet PC Platform SDK. Il file TpcError.h contiene le definizioni del codice di errore dell'API Tablet PC.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
#include <TpcError.h>
```



Il file EventSinks.h definisce le interfacce **IInkEventsImpl** e **IInkRecognitionEventsImpl** e configura gli eventi [**RecognitionWithAlternates,**](inkrecognizercontext-recognitionwithalternates.md) [**Stroke**](inkcollector-stroke.md)e [**Gesture.**](inkcollector-gesture.md)


```C++
#include "EventSinks.h"
```



Il file ChildWnds.h contiene le definizioni delle classi **CInkInputWnd** e **CRecoOutputWnd**, derivate da CWindowImpl di ATL e usate per creare le finestre figlio dell'esempio.


```C++
#include "ChildWnds.h"
```



Il file AdvReco.h dichiara la **classe CAdvRecoApp,** che è la classe della finestra dell'applicazione per questo esempio.


```C++
#include "AdvReco.h"
```



## <a name="initializing-the-application-window"></a>Inizializzazione della finestra dell'applicazione

Il metodo della finestra configura l'oggetto `Run` **CAdvRecoApp,** carica il menu e l'icona per la finestra, crea un oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) per il riconoscitore predefinito e avvia il ciclo di messaggi della finestra.

Il metodo **OnCreate della finestra** gestisce l'evento **WM \_ CREATE** e crea le finestre figlio. Un [**oggetto InkCollector**](inkcollector-class.md) si connette all'origine evento dell'agente di raccolta input penna e abilita l'input penna nella finestra di input penna. Crea quindi un oggetto [**InkRecognizerGuide**](inkrecognizerguide-class.md) e usa la proprietà [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer) dell'agente di raccolta input penna per convertire i rettangoli della casella della guida di riconoscimento nello spazio input penna. Infine, il **metodo OnCreate** crea un [**oggetto InkWordList.**](inkwordlist-class.md)

## <a name="handling-ink-collector-events"></a>Gestione degli eventi dell'agente di raccolta input penna

Il metodo **OnStroke** della finestra gestisce l'evento Stroke dell'agente [**di**](inkcollector-stroke.md) raccolta input penna. Il nuovo [**oggetto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) viene aggiunto a [InkStrokes della](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) dell'agente di raccolta input penna.

Il metodo **OnGesture** della finestra gestisce l'evento Gesture dell'agente [**di**](inkcollector-gesture.md) raccolta input penna. Il **metodo OnGesture** identifica il movimento, usando prima il movimento di attendibilità più alto, e controlla se la finestra supporta questo particolare movimento. Se il movimento è supportato, il rettangolo di selezione del movimento viene invalidato, poiché il movimento viene rimosso dalla raccolta di tratti. Se il movimento non è supportato, **l'evento Gesture** viene annullato e l'agente di raccolta input penna genera un [**evento Stroke.**](inkcollector-stroke.md) Infine, la finestra dei risultati viene aggiornata.

## <a name="handling-recognizer-context-events"></a>Gestione degli eventi di contesto del riconoscitore

Il metodo **OnRecognitionWithAlternates** della finestra gestisce l'evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) del contesto del riconoscimento. Il **metodo OnRecognitionWithAlternates** visualizza i risultati del riconoscimento nella finestra dei risultati.

## <a name="handling-menu-commands"></a>Gestione dei comandi di menu

Il metodo **OnRecognizer della finestra** gestisce i comandi del menu Recognizer. Se è **stato** selezionato il comando Default, per recuperare il riconoscimento predefinito viene usato il metodo [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) [di InkRecognizers.](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) In caso contrario, viene recuperato il riconoscitore selezionato. Viene quindi creato e usato un contesto di riconoscimento e i menu e la barra di stato vengono aggiornati.

Il metodo **OnFactoidWordlist della** finestra gestisce **il comando Usa Wordlist** del menu **Factoid.** La proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contesto di riconoscimento è impostata su **NULL per** reimpostare il contesto del riconoscimento. Se **l'opzione Usa Wordlist** è disattivata, la proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del contesto del riconoscimento è impostata su **NULL.** In caso contrario, la proprietà **WordList** del contesto del riconoscimento viene impostata [**sull'oggetto InkWordList**](inkwordlist-class.md) creato nel **metodo OnCreate.** Infine, [inkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dell'agente di raccolta input penna viene ricollegare al contesto del riconoscimento, viene chiamato il metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contesto di riconoscimento e il menu viene aggiornato.

Il metodo **OnFactoid della** finestra gestisce i comandi factoid nel menu **Factoid.** Imposta prima di tutto la proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contesto del riconoscimento su **NULL,** imposta la proprietà Factoid del contesto del riconoscimento sul [**factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) selezionato e riassegna [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dell'agente di raccolta input penna al contesto del riconoscimento. Se [l'oggetto Factoid](factoid-constants.md) è supportato dal contesto del riconoscimento, viene chiamato il metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contesto del riconoscimento; In caso contrario, viene visualizzato un messaggio di errore. Infine, il menu e la barra di stato vengono aggiornati.

Il metodo **OnGuide della** finestra gestisce i comandi **del** menu Guida. Se il contesto del riconoscimento supporta le opzioni della guida, il metodo **OnGuide** imposta la proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contesto del riconoscimento su **NULL,** imposta la proprietà [**Guide**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) del contesto di riconoscimento sull'impostazione della guida selezionata, riassegna [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dell'agente di raccolta input penna al contesto del riconoscimento e chiama il metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contesto del riconoscimento. In caso contrario, viene visualizzato un messaggio di errore. Infine, la finestra di input, il menu e la barra di stato vengono aggiornati.

Il metodo **OnMode della** finestra gestisce i comandi **nel** menu Modalità. Disabilita l'agente di raccolta input penna, aggiorna la proprietà [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) dell'agente di raccolta input penna, aggiorna il menu e mostra o nasconde gli elenchi di movimenti. Infine, l'agente di raccolta input penna è abilitato.

Il metodo **OnRecognize della finestra** gestisce il **comando Recognize** nel menu Input penna. Chiama il metodo [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) del contesto di riconoscimento per evitare che l'input penna venga aggiunto al contesto di riconoscimento. Questo è talvolta necessario, perché non tutti i riconoscitori supportano il riconoscimento parziale. Chiama quindi il metodo [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) del contesto del riconoscimento e passa i risultati al metodo **OnRecognitionWithAlternates della** finestra. Infine, [inkStrokes dell'agente](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) di raccolta input penna viene riassegnato al contesto del riconoscimento.

Il metodo **OnClear della** finestra gestisce il **comando Cancella** nel menu **Input** penna. Elimina i tratti dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) dell'agente di raccolta input penna, rilascia la raccolta di tratti precedenti e ne crea uno nuovo per la proprietà **Ink** dell'agente di raccolta input penna e associa la nuova raccolta di tratti al contesto del riconoscitore.

Il metodo **OnExit della** finestra gestisce il **comando Exit** nel menu **Input** penna e genera l'evento WM \_ CLOSE.

## <a name="helper-methods"></a>Metodi helper

Il metodo **LoadMenu della** finestra viene chiamato dal metodo **Run** della finestra e aggiunge l'elenco dei riconoscitori supportati e l'elenco dei factoid supportati al menu. In primo luogo, recupera [InkRecognizers.](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) Scorre quindi i riconoscitori disponibili e seleziona solo quelli che hanno un elenco di lingue nella proprietà **Lingue,** che viene aggiunta al menu **Riconoscimento.** Infine, popola il menu **Factoid** con l'elenco di factoid definiti come costante globale.

Il metodo **UseRecognizer** della finestra viene chiamato dal metodo **OnRecognizer** della finestra quando l'utente seleziona un nuovo riconoscitore. Crea un contesto di riconoscimento, scollega il contesto precedente dal sink di evento del riconoscitore, cancella e rilascia il contesto precedente e associa il nuovo contesto al sink di evento del riconoscitore.

Il metodo **UseRecognizer** controlla quindi la proprietà [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) del riconoscitore, che restituisce un [**valore InkRecognizerCapabilities.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities) Se il sistema di riconoscimento supporta l'input a linee, il **comando Righe** **nel** menu Guida è abilitato. Se il riconoscimento supporta l'input boxed, il **comando Caselle** è abilitato. Se il sistema di riconoscimento non supporta l'input libero, **il comando Nessuno** è disabilitato. Se la selezione della guida corrente non è supportata, vengono aggiornate sia la proprietà [**Guide**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) del contesto del riconoscitore che il menu.

Il metodo **UseRecognizer tenta** quindi di impostare le [**proprietà WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) e [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del contesto del riconoscitore. Se una delle due impostazioni non è supportata dal riconoscimento, viene usato il valore predefinito e il menu viene aggiornato.

Infine, il metodo **UseRecognizer** associa la proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) dell'oggetto [**InkDisp**](inkdisp-class.md) dell'agente di raccolta input penna al contesto del riconoscitore, imposta il tipo di carattere della finestra di output su uno supportato dalla lingua del sistema di riconoscimento, reimposta la finestra di output e aggiorna i risultati del riconoscimento chiamando il metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contesto del riconoscimento.

Il metodo **GetGestureName della** finestra viene chiamato dal metodo **OnGesture della** finestra. Cerca il movimento e restituisce un indice al nome del movimento, archiviato in una tabella di stringhe nel file AdvReco.rc.

 

 
