---
title: Architettura e componenti
description: Questo argomento descrive i componenti che costituiscono Microsoft DirectComposition.
ms.assetid: 7C79B330-41EA-4BA0-9103-BB5A0C3D4CE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2de495aa170560b1e7082cacf1893a8c94905a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047178"
---
# <a name="architecture-and-components"></a>Architettura e componenti

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Questo argomento descrive i componenti che costituiscono Microsoft DirectComposition. È costituito dalle seguenti sezioni.

-   [Componenti software](#software-components)
-   [Libreria di applicazioni](#application-library)
-   [Motore di composizione](#composition-engine)
-   [Argomenti correlati](#related-topics)

## <a name="software-components"></a>Componenti software

DirectComposition è costituito dai componenti software principali seguenti.

-   Una libreria di applicazioni in modalità utente (dcomp.dll) che implementa l'API pubblica basata su Component Object Model (COM).
-   Un motore di composizione in modalità utente (dwmcore.dll) ospitato nel processo di Gestione finestre desktop (DWM) (dwm.exe) ed esegue l'effettiva composizione desktop.
-   Un database di oggetti in modalità kernel (parte di win32k.sys) che esegue il marshalling dei comandi dall'applicazione al motore di composizione.

Una singola istanza del motore di composizione gestisce gli alberi della composizione DirectComposition per tutte le applicazioni e l'albero di composizione DWM, che rappresenta l'intero desktop. Viene creata un'istanza del database di oggetti in modalità kernel e del motore di composizione in modalità utente una volta per sessione, pertanto un computer Terminal Server con più utenti ha più istanze di entrambi i componenti.

Il diagramma seguente illustra i componenti principali di DirectComposition e il modo in cui sono correlati tra loro.

![architettura di primo livello di DirectComposition](images/directcomposition-top-level-architecture.png)

## <a name="application-library"></a>Libreria di applicazioni

La libreria di applicazioni DirectComposition è un'API pubblica basata su COM con un singolo punto di ingresso flat che viene esportato da dcomp.dll e restituisce un puntatore a interfaccia a un oggetto dispositivo. L'oggetto dispositivo, a sua volta, dispone di metodi per la creazione di tutti gli altri oggetti, ognuno dei quali è rappresentato da un puntatore a interfaccia. Tutte le interfacce DirectComposition ereditano da e implementano completamente l'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . Tutti i metodi che accettano le interfacce DirectComposition controllano se l'interfaccia è implementata all'interno di dcomp.dll o se è implementata da un altro componente. Poiché DirectComposition non è estensibile, i metodi che accettano le interfacce come parametri restituiscono E \_ INVALIDARG se le interfacce non sono implementate in dcomp.dll. L'API non richiede privilegi speciali. può essere chiamato da processi in esecuzione al livello di accesso più basso. Tuttavia, poiché l'API non funziona nella sessione 0, non è adatta per i servizi. In questi aspetti, l'API DirectComposition è simile ad altre API Microsoft DirectX, in particolare Direct2D, Microsoft Direct3D e Microsoft DirectWrite.

Poiché il motore di composizione è progettato esclusivamente per l'esecuzione asincrona, le proprietà dell'oggetto nell'API DirectComposition sono di sola scrittura. Tutte le proprietà hanno metodi setter, ma non metodi Get. La lettura delle proprietà non solo comporta un utilizzo intensivo delle risorse, ma può anche essere imprecisa perché qualsiasi valore restituito dal motore di composizione può diventare immediatamente non valido. Questo problema può verificarsi se, ad esempio, un'animazione indipendente viene associata alla proprietà che viene letta.

L'API è thread-safe. Un'applicazione può chiamare qualsiasi metodo da qualsiasi thread in qualsiasi momento. Tuttavia, poiché molti metodi API devono essere chiamati in una determinata sequenza, senza alcuna sincronizzazione, un'applicazione può riscontrare un comportamento imprevedibile a seconda della modalità di interfoliazione dei thread. Se, ad esempio, due thread modificano contemporaneamente la stessa proprietà dello stesso oggetto con valori diversi, l'applicazione non è in grado di stimare quale dei due valori sarà il valore finale della proprietà. Analogamente, se due thread chiamano [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) sullo stesso dispositivo, nessuno dei due thread ottiene un comportamento transazionale perché una chiamata al **commit** in un thread invierà il batch di tutti i comandi emessi da entrambi i thread, non solo quello che ha chiamato **commit**.

Il sistema gestisce tutto lo stato interno per ogni oggetto dispositivo. Se un'applicazione crea due o più oggetti dispositivo DirectComposition, l'applicazione può mantenere batch indipendenti e altro stato tra i due.

Tutti gli oggetti DirectComposition hanno affinità oggetto dispositivo; gli oggetti creati da un particolare oggetto dispositivo possono essere usati solo con tale oggetto dispositivo e possono essere associati solo ad altri oggetti creati dallo stesso oggetto dispositivo. In altre parole, ogni oggetto dispositivo è un'isola disgiunta separata di funzionalità. L'unica eccezione è rappresentata dalla classe visiva, che consente la compilazione di alberi visivi in cui un oggetto visivo può appartenere a un oggetto dispositivo diverso rispetto al relativo elemento padre. Questo consente scenari in cui un'applicazione e un controllo possono gestire un singolo albero di composizione senza che sia necessario condividere un singolo oggetto dispositivo DirectComposition.

## <a name="composition-engine"></a>Motore di composizione

Il motore di composizione DirectComposition viene eseguito su un processo dedicato, separato da qualsiasi processo dell'applicazione. Un singolo processo di composizione, dwm.exe, supporta tutte le applicazioni in una sessione. Ogni applicazione può creare due alberi visivi per ogni finestra di cui è proprietario. Tutti gli alberi vengono effettivamente implementati come sottoalberi di una struttura ad albero visuale più ampia che include anche le strutture di composizione di DWM. DWM crea una struttura ad albero visuale di grandi dimensioni per ogni desktop in una sessione. Ecco i vantaggi principali di questa architettura:

-   Il motore di composizione ha accesso a tutte le bitmap dell'applicazione e ad alberi visivi, che consente l'interoperabilità e la composizione della finestra tra processi.
-   Il motore di composizione viene eseguito in un processo di sistema attendibile separato da qualsiasi processo dell'applicazione, consentendo alle applicazioni con diritti di accesso limitati di comporre in modo sicuro il contenuto protetto.
-   Il motore di composizione può rilevare quando una particolare finestra è completamente nascosto ed evitare di sprecare risorse della CPU e della GPU (Graphics Processing Unit) che compongono la finestra.
-   Il motore di composizione può comporre direttamente sul buffer indietro, evitando la necessità di una copia aggiuntiva necessaria per i motori di composizione per processo.
-   Tutte le applicazioni condividono un singolo dispositivo Direct3D per la composizione, che offre un notevole risparmio di memoria

La struttura ad albero visuale è una struttura mantenuta. L'API DirectComposition espone metodi per modificare la struttura in batch di modifiche elaborate atomicamente. L'oggetto radice nell'API DirectComposition è l'oggetto dispositivo, che funge da Factory per tutti gli altri oggetti DirectComposition e contiene un metodo denominato [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). Il motore di composizione non riflette le modifiche apportate dall'applicazione alla struttura ad albero visuale fino a quando l'applicazione chiama **commit**. a questo punto tutte le modifiche apportate dall'ultimo **commit** vengono elaborate come una singola transazione.

Il requisito per chiamare [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) è simile al concetto di "frame", ad eccezione del fatto che, poiché il motore di composizione viene eseguito in modo asincrono, può presentare più frame diversi tra le chiamate al **commit**. In DirectComposition, un *frame* è una singola iterazione del motore di composizione e l'intervallo impiegato da un'applicazione tra due chiamate al **commit** viene chiamato *batch*.

DirectComposition esegue il batch di tutte le chiamate dell'applicazione all'API DirectComposition. Il database dell'oggetto kernel, implementato nel driver della sessione di win32k.sys, archivia tutte le informazioni sullo stato associate alle chiamate API.

Il motore di composizione produce un frame per ogni vuoto verticale nella visualizzazione. Il frame viene avviato in uno spazio vuoto verticale e viene indirizzato al successivo vuoto verticale. All'avvio del frame, il motore di composizione preleva tutti i batch in sospeso e include i comandi in tale frame. I batch vengono inseriti in una coda in sospeso quando l'applicazione chiama [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)e la coda in sospeso viene scaricata in modo atomico all'inizio del frame. Pertanto, è presente un singolo momento che contrassegna l'inizio di un frame. Tutti i batch inviati prima di questo punto vengono inclusi nel frame, mentre tutti i batch inviati dopo devono attendere fino all'elaborazione del frame successivo. Il ciclo di composizione completo è il seguente:

1.  Stimare l'ora del successivo vuoto verticale.
2.  Recuperare tutti i batch in sospeso.
3.  Elaborare i batch recuperati.
4.  Aggiornare tutte le animazioni usando il tempo stimato nel passaggio 1.
5.  Determinare le aree della schermata che devono essere ricomposte.
6.  Comporre di nuovo le aree dirty.
7.  Presentare il frame capovolgendo i buffer indietro e anteriore per ogni schermata.
8.  Se non è stata eseguita alcuna operazione di composizione e presentazione nei passaggi 6 e 7, attendere il commit di un batch.
9.  Attendere il successivo vuoto verticale.

Se sono presenti più monitoraggi collegati a una singola scheda video, il motore di composizione utilizza lo spazio vuoto verticale del monitor primario per guidare il ciclo di composizione e impostare i tempi di campionamento dell'animazione. Ogni monitoraggio è rappresentato da una catena di Flip a schermo intero separata; il motore di composizione ripete i passaggi 6 e 7 per ogni monitoraggio, in modo Round Robin, usando un singolo dispositivo Direct3D. Se sono presenti anche più schede video, il motore di composizione usa un dispositivo Direct3D separato per ogni scheda video nei passaggi 6 e 7.

I frame di composizione sono pianificati per iniziare sempre in uno spazio vuoto verticale, come illustrato nella figura seguente.

![pianificazione del frame di composizione](images/composition-frame-scheduling.png)

Se il motore di composizione non ha alcuna operazione da eseguire perché l'albero della composizione non è stato modificato, il thread di composizione rimane in attesa di un nuovo batch. Quando viene inviato un nuovo batch, il thread di composizione viene riattivato, ma viene immediatamente riavviato per la sospensione fino al successivo vuoto verticale. Questo comportamento garantisce l'ora di inizio e di fine del frame prevedibile per le applicazioni e per il motore di composizione.

Il motore di composizione pubblica i tempi di presentazione del frame e la frequenza dei fotogrammi corrente. La pubblicazione di queste informazioni consente alle applicazioni di stimare il tempo di presentazione per i propri batch, che a sua volta consente la sincronizzazione delle animazioni. In particolare, un'applicazione può usare una combinazione di statistiche di frame dal motore di composizione e un modello cronologico del tempo impiegato dal thread dell'interfaccia utente per generare un batch, per determinare il tempo di campionamento per le proprie animazioni.

Ad esempio, all'inizio del batch di applicazioni illustrato nella figura precedente, l'applicazione può eseguire una query sul motore di composizione per determinare l'ora di presentazione esatta del frame successivo. L'applicazione può quindi usare l'ora corrente, insieme alle informazioni sui batch precedenti che ha prodotto, per determinare se l'applicazione può completare il batch corrente prima del successivo vuoto verticale. Pertanto, l'applicazione utilizza l'ora di presentazione del frame come tempo di campionamento per le proprie animazioni. Se l'applicazione determina che è improbabile che il suo lavoro venga completato nello spazio vuoto verticale corrente, l'applicazione può usare l'ora del frame successiva come tempo di campionamento, usando le informazioni sulla frequenza dei fotogrammi restituite dal motore di composizione per calcolare tale tempo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 