---
title: Architettura e componenti
description: Questo argomento descrive i componenti che costituiscono Microsoft DirectComposition.
ms.assetid: 7C79B330-41EA-4BA0-9103-BB5A0C3D4CE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125a640f902bc64d55af8cdcdbf816c788e0507a48034dfb52c972fa3f068d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985463"
---
# <a name="architecture-and-components"></a>Architettura e componenti

> [!NOTE]
> Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition. Per altre informazioni, vedere [Modernizzare l'app desktop usando il livello Visivo.](/windows/uwp/composition/visual-layer-in-desktop-apps)

Questo argomento descrive i componenti che costituiscono Microsoft DirectComposition. È costituito dalle sezioni seguenti.

-   [Componenti software](#software-components)
-   [Libreria di applicazioni](#application-library)
-   [Motore di composizione](#composition-engine)
-   [Argomenti correlati](#related-topics)

## <a name="software-components"></a>Componenti software

DirectComposition è costituito dai componenti software principali seguenti.

-   Libreria di applicazioni in modalità utente (dcomp.dll) che implementa l'API pubblica basata su Component Object Model (COM).
-   Un motore di composizione in modalità utente (dwmcore.dll) ospitato nel processo Gestione finestre desktop (dwm.exe) ed esegue la composizione desktop effettiva.
-   Un database di oggetti in modalità kernel (parte win32k.sys) che effettua il marshalling dei comandi dall'applicazione al motore di composizione.

Una singola istanza del motore di composizione gestisce gli alberi della composizione DirectComposition per tutte le applicazioni e l'albero della composizione DWM, che rappresenta l'intero desktop. Sia il database degli oggetti in modalità kernel che il motore di composizione in modalità utente vengono istanziati una volta per sessione, quindi un computer Terminal Server con più utenti ha più istanze di entrambi i componenti.

Il diagramma seguente illustra i componenti DirectComposition principali e il modo in cui sono correlati tra loro.

![Architettura di primo livello directcomposition](images/directcomposition-top-level-architecture.png)

## <a name="application-library"></a>Libreria di applicazioni

La libreria di applicazioni DirectComposition è un'API pubblica basata su COM con un singolo punto di ingresso flat esportato da dcomp.dll e restituisce un puntatore a interfaccia a un oggetto dispositivo. L'oggetto dispositivo, a sua volta, dispone di metodi per la creazione di tutti gli altri oggetti, ognuno dei quali è rappresentato da un puntatore a interfaccia. Tutte le interfacce DirectComposition ereditano da e implementano completamente [**l'interfaccia IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) Tutti i metodi che accettano le interfacce DirectComposition controllano se l'interfaccia viene implementata all'interno di dcomp.dll o se viene implementata da un altro componente. Poiché DirectComposition non è estendibile, i metodi che accettano interfacce come parametri restituiscono E INVALIDARG se le interfacce non vengono implementate \_ in dcomp.dll. L'API non richiede privilegi speciali. può essere chiamato dai processi in esecuzione al livello di accesso più basso. Tuttavia, poiché l'API non funziona nella sessione 0, non è adatta per i servizi. A questo proposito, l'API DirectComposition è simile ad altre API Microsoft DirectX, in particolare Direct2D, Microsoft Direct3D e Microsoft DirectWrite.

Poiché il motore di composizione è progettato esclusivamente per l'esecuzione asincrona, le proprietà dell'oggetto nell'API DirectComposition sono di sola scrittura. Tutte le proprietà hanno metodi setter, ma non metodi getter. La lettura delle proprietà non è solo a elevato utilizzo di risorse, ma può anche essere imprecisa perché qualsiasi valore restituito dal motore di composizione può diventare immediatamente non valido. Ciò può verificarsi se, ad esempio, un'animazione indipendente è associata alla proprietà in fase di lettura.

L'API è thread-safe. Un'applicazione può chiamare qualsiasi metodo da qualsiasi thread in qualsiasi momento. Tuttavia, poiché molti metodi API devono essere chiamati in una sequenza specifica, senza alcuna sincronizzazione un'applicazione può avere un comportamento imprevedibile a seconda dell'interfoliazione dei thread. Ad esempio, se due thread modificano contemporaneamente la stessa proprietà dello stesso oggetto in valori diversi, l'applicazione non può stimare quale dei due valori sarà il valore finale della proprietà. Analogamente, se due thread chiamano [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) sullo stesso dispositivo, nessuno dei due thread ottiene effettivamente un comportamento transazionale perché una chiamata a **Commit** in un thread invierà il batch di tutti i comandi emessi da entrambi i thread, non solo quello che ha chiamato **Commit**.

Il sistema mantiene tutti gli stati interni per ogni oggetto dispositivo. Se un'applicazione crea due o più oggetti dispositivo DirectComposition, l'applicazione può mantenere batch indipendenti e altri stati tra i due.

Tutti gli oggetti DirectComposition hanno affinità di oggetto dispositivo. Gli oggetti creati da un particolare oggetto dispositivo possono essere usati solo con tale oggetto dispositivo e possono essere associati solo ad altri oggetti creati dallo stesso oggetto dispositivo. In altre parole, ogni oggetto dispositivo è un'isola separata di funzionalità non contigue. L'unica eccezione è la classe visiva, che consente la creazione di alberi visivi in cui un oggetto visivo può appartenere a un oggetto dispositivo diverso da quello padre. Ciò consente scenari in cui un'applicazione e un controllo possono gestire un singolo albero della composizione senza dover condividere un singolo oggetto dispositivo DirectComposition.

## <a name="composition-engine"></a>Motore di composizione

Il motore di composizione DirectComposition viene eseguito in un processo dedicato, separato da qualsiasi processo dell'applicazione. Un singolo processo di composizione, dwm.exe, supporta ogni applicazione in una sessione. Ogni applicazione può creare due alberi visivi per ogni finestra di cui è proprietaria. Tutti gli alberi vengono effettivamente implementati come sottoalberi di una struttura ad albero visuale più grande che comprende anche le strutture di composizione di DWM. Il modello DWM costruisce una struttura ad albero visuale di grandi dimensioni per ogni desktop in una sessione. Ecco i vantaggi principali di questa architettura:

-   Il motore di composizione ha accesso a tutte le bitmap dell'applicazione e agli alberi visivi, che consentono l'interoperabilità e la composizione delle finestre tra processi.
-   Il motore di composizione viene eseguito in un processo di sistema attendibile separato da qualsiasi processo dell'applicazione, consentendo alle applicazioni con diritti di accesso limitati di comporre in modo sicuro contenuto protetto.
-   Il motore di composizione può rilevare quando una determinata finestra è completamente occlusa ed evitare di sprecare risorse GPU (Cpu and Graphics Processing Unit) per la finestra.
-   Il motore di composizione può comporre direttamente nel buffer nascosto dello schermo, evitando la necessità di una copia aggiuntiva necessaria per i motori di composizione per processo.
-   Tutte le applicazioni condividono un singolo dispositivo Direct3D per la composizione, con un notevole risparmio di memoria

La struttura ad albero visuale è una struttura mantenuta. L'API DirectComposition espone metodi per modificare la struttura in batch di modifiche elaborate in modo atomico. L'oggetto radice nell'API DirectComposition è l'oggetto dispositivo, che funge da factory per tutti gli altri oggetti DirectComposition e contiene un metodo denominato [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). Il motore di composizione non riflette le modifiche apportate dall'applicazione alla struttura ad albero visuale fino a quando l'applicazione non chiama **Commit**, a questo punto tutte le modifiche dall'ultimo **commit** vengono elaborate come una singola transazione.

Il requisito di chiamare [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) è simile al concetto di "frame", ad eccezione del fatto che, poiché il motore di composizione viene eseguito in modo asincrono, può presentare diversi fotogrammi tra le chiamate a **Commit**. In DirectComposition un *frame* è una singola iterazione del motore di composizione e l'intervallo trascorso da un'applicazione tra due chiamate a **Commit** è denominato *batch*.

DirectComposition in batch tutte le chiamate dell'applicazione all'API DirectComposition. Il database di oggetti del kernel, implementato nel driver di sessione win32k.sys, archivia tutte le informazioni sullo stato associate alle chiamate API.

Il motore di composizione produce un frame per ogni spazio vuoto verticale nello schermo. Il frame viene avviato in corrispondenza di uno spazio vuoto verticale e punta al successivo spazio vuoto verticale. All'avvio del frame, il motore di composizione seleziona tutti i batch in sospeso e include i relativi comandi in tale frame. I batch vengono inseriti in una coda in sospeso quando l'applicazione chiama [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)e la coda in sospeso viene scaricata atomicamente all'inizio del frame. Di conseguenza, esiste un singolo punto nel tempo che contrassegna l'inizio di un frame. Tutti i batch inviati prima di questo punto vengono inclusi nel frame, mentre i batch inviati dopo devono attendere l'elaborazione del frame successivo. Il ciclo di composizione completo è il seguente:

1.  Stimare l'ora del successivo vuoto verticale.
2.  Recuperare tutti i batch in sospeso.
3.  Elaborare i batch recuperati.
4.  Aggiornare tutte le animazioni usando il tempo stimato nel passaggio 1.
5.  Determinare le aree dello schermo che devono essere ri composte.
6.  Ricomposire le aree dirty.
7.  Presentare il frame capovolgendo i buffer indietro e frontale per ogni schermata.
8.  Se non è stato composto e presentato alcun elemento nei passaggi 6 e 7, attendere il commit di un batch.
9.  Attendere il successivo spazio vuoto verticale.

Se sono presenti più monitor collegati a una singola scheda video, il motore di composizione usa lo spazio vuoto verticale del monitor primario per guidare il ciclo di composizione e impostare i tempi di campionamento dell'animazione. Ogni monitoraggio è rappresentato da una catena di flip a schermo intero separata. il motore di composizione ripete i passaggi 6 e 7 per ogni monitoraggio, in modalità round robin, usando un singolo dispositivo Direct3D. Se sono presenti anche più schede video, il motore di composizione usa un dispositivo Direct3D separato per ogni scheda video nei passaggi 6 e 7.

I fotogrammi di composizione vengono pianificati per iniziare sempre in corrispondenza di uno spazio vuoto verticale, come illustrato nella figura seguente.

![pianificazione dei frame di composizione](images/composition-frame-scheduling.png)

Se il motore di composizione non ha alcuna operazione da eseguire perché l'albero della composizione non è stato modificato, il thread di composizione viene in sospensione durante l'attesa di un nuovo batch. Quando viene inviato un nuovo batch, il thread di composizione si riattiva ma torna immediatamente in sospensione fino al successivo vuoto verticale. Questo comportamento garantisce tempi di inizio e fine prevedibili per le applicazioni e per il motore di composizione.

Il motore di composizione pubblica i tempi di presentazione dei fotogrammi e la frequenza fotogrammi corrente. La pubblicazione di queste informazioni consente alle applicazioni di stimare il tempo di presentazione per i propri batch, che a sua volta consente la sincronizzazione delle animazioni. In particolare, un'applicazione può usare una combinazione di statistiche dei fotogrammi del motore di composizione e un modello cronologico del tempo necessario al thread dell'interfaccia utente per produrre un batch, per determinare il tempo di campionamento per le proprie animazioni.

Ad esempio, all'inizio del batch dell'applicazione illustrato nella figura precedente, l'applicazione può eseguire una query sul motore di composizione per determinare l'ora di presentazione esatta del frame successivo. L'applicazione può quindi usare l'ora corrente, insieme alle informazioni sui batch precedenti prodotti, per determinare se l'applicazione può completare il batch corrente prima del successivo vuoto verticale. Pertanto, l'applicazione usa il tempo di presentazione dei fotogrammi come tempo di campionamento per le proprie animazioni. Se l'applicazione determina che è improbabile completare il lavoro nello spazio vuoto verticale corrente, l'applicazione può usare il tempo di campionamento successivo come tempo di campionamento, usando le informazioni sulla frequenza dei fotogrammi restituite dal motore di composizione per calcolare tale tempo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi a DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 