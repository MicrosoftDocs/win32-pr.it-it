---
title: Cenni preliminari sull'animazione Windows
description: Questa panoramica fornisce un'introduzione a gestione animazioni Windows e si concentra sui componenti e i concetti chiave.
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Animazione Windows Animation Windows, panoramica
- Animazione Windows oggetti Animation Manager, descritti
- Animazione Windows per variabili di animazione, descrizione
- animazione Windows oggetti timer animazione, descritti
- Animazione di Windows di sistema di temporizzazione
- Animazione Windows Duration sensibile al contesto
- Animazione Windows corrispondente alla velocità
- Animazione di Windows per la gestione dei conflitti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a60b02b29d8d434cc93420f36c3cdca4428f94c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046843"
---
# <a name="windows-animation-overview"></a>Cenni preliminari sull'animazione Windows

Questa panoramica fornisce un'introduzione a gestione animazioni Windows e si concentra sui componenti e i concetti chiave. Per ulteriori informazioni sugli storyboard e le transizioni, vedere [Cenni preliminari sugli storyboard](storyboard-construction.md).

In questo argomento sono incluse le sezioni seguenti:

-   [Concetti di base](#basic-concepts)
-   [Componenti dell'animazione Windows](#components-of-windows-animation)
-   [API di animazione Windows](#the-windows-animation-api)
-   [Configurazioni](#configurations)
    -   [Animazione basata su applicazioni](#application-driven-animation)
    -   [Animazione basata su timer](#timer-driven-animation)
-   [Funzionalità avanzate](#advanced-features)
    -   [Gestione dei conflitti](#contention-management)
-   [Argomenti correlati](#related-topics)

## <a name="basic-concepts"></a>Concetti di base

L' *animazione* è una sequenza di immagini ancora successive che produce un illusione di spostamento quando viene riprodotto. L'uso di animazioni interattive nella sua interfaccia utente può fornire a un'applicazione una personalità univoca, oltre a migliorare l'esperienza utente. L'animazione consente di comunicare le principali modifiche di stato nell'interfaccia utente e di gestire la complessità dell'interfaccia utente. L'animazione può anche aggiungere alla percezione dell'utente della qualità di un'applicazione.

Come esempio, l'animazione Windows viene utilizzata nella barra delle applicazioni per semplificare la gestione e l'accesso ai file e ai programmi, oltre a una lente di ingrandimento per le diverse parti dello schermo per facilitarne la visualizzazione.

Le unità di base di un'animazione sono la caratteristica di un elemento visivo da animare e la descrizione del modo in cui tale caratteristica cambia nel tempo. Un'applicazione può animare un'ampia gamma di caratteristiche, ad esempio la posizione, il colore, la dimensione, la rotazione, il contrasto e l'opacità.

Nell'animazione Windows una *variabile di animazione* rappresenta la caratteristica da animare. Una *transizione* descrive il modo in cui il valore di tale variabile di animazione cambia quando si verifica l'animazione. Ad esempio, un elemento visivo potrebbe avere una variabile di animazione che specifica l'opacità e un'azione dell'utente potrebbe generare una transizione che accetta tale opacità da un valore 50 a 100, che rappresenta un'animazione da semi trasparente a completamente opaca.

Uno *storyboard* è un set di transizioni applicato a una o più variabili di animazione nel tempo. Un'applicazione consente di visualizzare le animazioni creando e riproducendo gli storyboard e quindi creando sequenze di fotogrammi discreti quando i valori delle variabili di animazione cambiano nel tempo.

## <a name="components-of-windows-animation"></a>Componenti dell'animazione Windows

L'animazione Windows è costituita dai componenti seguenti:

<dl> <dt>

<span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>Gestione animazioni
</dt> <dd>

Le applicazioni utilizzano un oggetto Gestione animazioni per creare variabili di animazione e storyboard, animazioni di pianificazione e controllo e aggiornare le informazioni sullo stato prima che l'applicazione disegni ogni frame. Un singolo oggetto di gestione animazioni gestisce in genere tutte le animazioni in un'applicazione e pertanto dispone di un controllo globale su tutti gli storyboard pianificati.

</dd> <dt>

<span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>variabili di animazione
</dt> <dd>

Prima di avviare qualsiasi animazione, un'applicazione deve creare oggetti variabile di animazione. Una variabile di animazione rappresenta un aspetto di un elemento visivo da animare. La variabile è un valore a virgola mobile scalare, anche se il valore può essere arrotondato a un valore integer.

Una variabile di animazione ha in genere la stessa durata dell'elemento visivo a cui aggiungere un'animazione. Il valore iniziale di una variabile di animazione viene specificato al momento della creazione della variabile. Successivamente, il suo valore non può essere modificato direttamente. deve essere aggiornato tramite Gestione animazioni.

Una variabile di animazione può essere identificata da un *tag*, ovvero un abbinamento di un identificatore di tipo integer con un puntatore a un oggetto com. Un tag non deve essere univoco, a meno che non venga usato dall'applicazione per cercare una variabile. Per impostazione predefinita, una variabile di animazione non dispone di un tag e tutti i tentativi di lettura del tag avranno esito negativo fino a quando non ne viene impostata una.

</dd> <dt>

<span id="timing_system"></span><span id="TIMING_SYSTEM"></span>sistema di temporizzazione
</dt> <dd>

L'animazione Windows include un sistema di temporizzazione che consente di garantire il rendering delle animazioni a una frequenza dei fotogrammi uniforme e coerente, riducendo al tempo stesso l'utilizzo delle risorse di sistema per il rendering quando il sistema è occupato. Un *timer* consente di gestire il rendering dell'animazione indicando automaticamente il passaggio di una piccola unità di tempo, denominata *segno* di indicizzazione. Il sistema di temporizzazione monitora le prestazioni complessive di rendering del *sistema e limita* le animazioni aumentando o diminuendo in modo dinamico la frequenza dei cicli. Le applicazioni possono consentire a un timer di guidare gestione animazioni ed è possibile registrare un gestore per ricevere una notifica prima e dopo l'aggiornamento del Manager per ogni ciclo. Le applicazioni possono specificare la frequenza minima dei fotogrammi di animazione accettabile per un timer e ricevere una notifica se la frequenza dei fotogrammi effettiva di un'animazione scende al di sotto di questa frequenza.

Per conservare le risorse di sistema, è possibile configurare un timer per disabilitarsi quando non viene eseguita alcuna animazione.

</dd> </dl>

## <a name="the-windows-animation-api"></a>API di animazione Windows

L'API di animazione di Windows è un'API basata su COM a thread singolo che fornisce le funzionalità seguenti per gli sviluppatori:

-   Oggetto Gestione animazioni, [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)), per la creazione di oggetti animazione e il controllo delle animazioni
-   Variabili di animazione e storyboard
-   Una libreria di base, [**UIAnimationTransitionLibrary**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85)), di transizioni pronte per l'uso
-   Oggetto timer, [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)), per determinare l'ora corrente e, facoltativamente, per la guida dell'animazione
-   Hook di eventi per il monitoraggio dello stato e dello stato di avanzamento dell'animazione

Per informazioni di riferimento complete sulle API, vedere informazioni di [riferimento sull'animazione di Windows](windows-animation-reference.md). Per un esempio di codice, vedere [attività di animazione Windows](using-windows-animation.md) e [esempi di animazioni di Windows](windows-animation-samples.md).

## <a name="configurations"></a>Configurazioni

Le applicazioni devono ottenere l'ora corrente prima di pianificare una nuova animazione. Di seguito sono riportati i meccanismi di temporizzazione supportati dall'animazione Windows:

-   [Animazione basata su applicazioni](#application-driven-animation)
-   [Animazione basata su timer](#timer-driven-animation)

### <a name="application-driven-animation"></a>Animazione Application-Driven

Le applicazioni che usano un'API grafica con accelerazione hardware possono essere sincronizzate con la frequenza di aggiornamento del monitor per eseguire il rendering di animazioni Smooth. In alternativa, un'applicazione può utilizzare un meccanismo di temporizzazione autonomo per determinare quando creare ogni frame di un'animazione. In entrambi i casi, l'applicazione indica al gestore dell'animazione quando aggiornare il proprio stato. Un timer di animazione può comunque essere utilizzato per determinare l'ora corrente con precisione elevata, nelle unità richieste da Gestione animazioni.

Nel diagramma seguente vengono illustrate le interazioni tra un'applicazione e i componenti di animazione di Windows quando l'applicazione conduce direttamente gli aggiornamenti dell'animazione.

![diagramma che mostra le interazioni tra un'applicazione e i componenti di animazione di Windows quando l'applicazione conduce direttamente gli aggiornamenti dell'animazione.](images/animationupdates.png)

Nella configurazione più semplice, un'applicazione ridisegnirà tutti gli elementi ogni volta che lo schermo viene aggiornato, anche quando nessuna animazione viene riprodotta. Per evitare il lavoro sprecato, un'applicazione può registrare un gestore eventi di gestione per ricevere una notifica in caso di animazioni pianificate e può rilevare quando la pianificazione è vuota, in modo che possa arrestare il ridisegno.

### <a name="timer-driven-animation"></a>Animazione Timer-Driven

Anziché aggiornare direttamente gestione animazioni, le applicazioni possono consentire al timer di animazione di indicare al gestore delle animazioni quando aggiornare il proprio stato e ricevere una notifica solo quando si è verificato ogni aggiornamento. Questo approccio è consigliato per le API grafiche precedenti. In generale, se è possibile eseguire la sincronizzazione con la frequenza di aggiornamento del monitoraggio, è preferibile usare un'animazione basata sull'applicazione.

Nel diagramma seguente vengono illustrate le interazioni tra un'applicazione e i componenti di animazione Windows quando il timer di animazione sta guidando gli aggiornamenti dell'animazione.

![diagramma che mostra le interazioni tra un'applicazione e i componenti di animazione Windows quando il timer di animazione sta guidando gli aggiornamenti dell'animazione.](images/animationtimerupdates.png)

Il timer può essere configurato per l'esecuzione solo quando le animazioni sono pianificate; in questo modo è semplice passare un determinato parametro quando il timer e il gestore animazione sono connessi.

## <a name="advanced-features"></a>Funzionalità avanzate

Oltre a una base di base per supportare l'animazione, l'animazione Windows include il supporto per diverse tecniche di animazione avanzate, tra cui:

<dl> <dt>

<span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*durata sensibile al contesto*
</dt> <dd>

Non è necessario correggere la durata di una transizione. può essere determinato in base al valore e alla velocità della variabile animata all'inizio della transizione.

</dd> <dt>

<span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*corrispondenza velocità*
</dt> <dd>

Lo spostamento è in genere più gradevole se la posizione e la velocità di un oggetto in movimento non passano immediatamente tra i valori. Quando un nuovo storyboard ne interrompe uno attualmente in riproduzione, la corrispondenza della velocità consente al nuovo storyboard di prelevare senza problemi la posizione in cui è terminata la prima.

</dd> <dt>

<span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*gestione dei conflitti*
</dt> <dd>

Se due storyboard devono aggiornare contemporaneamente la stessa variabile di animazione, si verificherà un conflitto di pianificazione. Anziché richiedere una specifica priorità numerica per ogni Storyboard, l'animazione Windows consente all'applicazione di determinare le priorità relative di due storyboard.

</dd> </dl>

### <a name="contention-management"></a>Gestione dei conflitti

Gli sviluppatori possono implementare un callback di *confronto prioritario* per confrontare la priorità dello storyboard di pianificato e lo storyboard già presente nella pianificazione. Un'applicazione che implementa un confronto di priorità può usare qualsiasi logica preferita per determinare quando uno storyboard previene un altro. Per risolvere il conflitto di pianificazione, l'animazione Windows chiede all'applicazione quali di queste azioni possono essere eseguite nell'ordine seguente:

-   **Annulla lo storyboard pianificato.** Se lo storyboard pianificato non è ancora stato avviato, è possibile che venga annullato e immediatamente rimosso dalla pianificazione.
-   **Tagliare lo storyboard pianificato.** Quando un nuovo storyboard taglia uno storyboard pianificato, lo storyboard pianificato smette di influenzare la variabile non appena il nuovo storyboard inizia ad animarlo. Viene stabilita una corrispondenza tra le velocità, consentendo al nuovo storyboard di selezionare senza problemi la posizione precedente.
-   **Concludere lo storyboard pianificato.** È possibile concludere uno storyboard solo se contiene un ciclo che si ripete per un periodo illimitato. Se lo storyboard si trova in un ciclo di questo tipo quando viene terminato, la ripetizione corrente viene completata e il resto dello storyboard viene quindi riprodotto. Se il ciclo non è ancora iniziato quando si conclude uno storyboard, il ciclo viene ignorato completamente.
-   **Comprime lo storyboard pianificato.** Se l'operazione di taglio o annullamento dello storyboard pianificato non è un'opzione, è consentita l'esecuzione dello storyboard. L'animazione Windows introduce la possibilità di comprimere il tempo disponibile per lo storyboard pianificato (e gli eventuali storyboard pianificati prima), in modo che le variabili raggiungano lo stato finale più rapidamente. Quando viene applicata la compressione, l'ora è temporaneamente accelerata per gli storyboard interessati, quindi la riproduzione viene eseguita più velocemente.

Se nessuna delle azioni precedenti è consentita dagli oggetti di confronto di priorità registrati, il tentativo di pianificare il nuovo storyboard ha esito negativo. Per impostazione predefinita, tutti gli storyboard possono essere tagliati, conclusi o compressi per evitare errori, ma nessuno può essere annullato.

Il diagramma seguente mostra il ciclo di vita di uno storyboard, usando gli stati definiti dall' [**enumerazione \_ \_ \_ dello stato dello storyboard dell'animazione dell'interfaccia utente**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) . Le applicazioni utilizzano l'API di animazione Windows per creare uno storyboard e inviarlo per la pianificazione. Gestione animazioni pianifica lo storyboard e gestisce l'animazione.

![diagramma che illustra in che modo Gestione animazioni pianifica lo storyboard e gestisce l'animazione.](images/statediagram.png)

Per ulteriori informazioni sulla pianificazione e sulla gestione degli storyboard, vedere [Cenni preliminari sugli storyboard](storyboard-construction.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sull'animazione Windows](windows-animation-reference.md)
</dt> <dt>

[Esempi di animazioni Windows](windows-animation-samples.md)
</dt> <dt>

[Attività di animazione Windows](using-windows-animation.md)
</dt> </dl>

 

 