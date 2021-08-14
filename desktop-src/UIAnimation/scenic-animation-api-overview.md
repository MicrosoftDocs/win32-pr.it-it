---
title: Windows Panoramica dell'animazione
description: Questa panoramica offre un'introduzione a Gestione Windows animazione e si concentra sui componenti e sui concetti chiave.
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Windows Animazione Windows Animation , panoramica
- oggetti di gestione dell'animazione Windows animation , descritto
- variabili di animazione Windows Animation , descritto
- oggetti timer di animazione Windows Animation , descritto
- Animazione del sistema di Windows temporizzazione
- Durata sensibile al contesto Windows animazione
- velocità corrispondente all'Windows animazione
- Gestione dei Windows di contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc0892cffa3e79428e19cbe5b1a3c27d7abda62365c4ceb15731101aa857f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348009"
---
# <a name="windows-animation-overview"></a>Windows Panoramica dell'animazione

Questa panoramica offre un'introduzione a Gestione Windows animazione e si concentra sui componenti e sui concetti chiave. Per altre informazioni su storyboard e transizioni, vedere [Cenni preliminari sugli storyboard.](storyboard-construction.md)

In questo argomento sono incluse le sezioni seguenti:

-   [Concetti di base](#basic-concepts)
-   [Componenti dell'Windows animazione](#components-of-windows-animation)
-   [API Windows Animation](#the-windows-animation-api)
-   [Configurazioni](#configurations)
    -   [Animazione basata sull'applicazione](#application-driven-animation)
    -   [Animazione basata su timer](#timer-driven-animation)
-   [Funzionalità avanzate](#advanced-features)
    -   [Gestione delle interezioni](#contention-management)
-   [Argomenti correlati](#related-topics)

## <a name="basic-concepts"></a>Concetti di base

*L'animazione* è una sequenza di immagini fisse successive che genera un'illusione di movimento quando viene riprodotta. L'uso dell'animazione interattiva nell'interfaccia utente può offrire a un'applicazione una personalità unica e migliorare l'esperienza utente. L'animazione consente di comunicare le principali modifiche di stato nell'interfaccia utente e di gestire la complessità dell'interfaccia utente. L'animazione può anche aggiungere all'utente la percezione della qualità di un'applicazione.

Ad esempio, Windows animation viene usato nella barra delle applicazioni per gestire e accedere a file e programmi e Lente di ingrandimento per ingrandire diverse parti dello schermo per renderle più facili da visualizzare per gli utenti.

Le unità fondamentali di un'animazione sono la caratteristica di un elemento visivo da animare e la descrizione del modo in cui tale caratteristica cambia nel tempo. Un'applicazione può animare un'ampia gamma di caratteristiche, ad esempio posizione, colore, dimensioni, rotazione, contrasto e opacità.

In Windows animation, una *variabile di animazione* rappresenta la caratteristica da animare. Una *transizione descrive* come cambia il valore di tale variabile di animazione quando si verifica l'animazione. Ad esempio, un elemento visivo potrebbe avere una variabile di animazione che ne specifica l'opacità e un'azione dell'utente potrebbe generare una transizione che accetta tale opacità da un valore compreso tra 50 e 100, che rappresenta un'animazione da semitrasparente a completamente opaca.

Uno *storyboard* è un set di transizioni applicate a una o più variabili di animazione nel tempo. Un'applicazione visualizza le animazioni creando e riproducendo storyboard e quindi disegnando sequenze di fotogrammi discreti man mano che i valori delle variabili di animazione cambiano nel tempo.

## <a name="components-of-windows-animation"></a>Componenti dell'Windows animazione

Windows L'animazione è costituita dai componenti seguenti:

<dl> <dt>

<span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>Gestione animazione
</dt> <dd>

Le applicazioni usano un oggetto di gestione dell'animazione per creare variabili di animazione e storyboard, pianificare e controllare le animazioni e aggiornare le informazioni sullo stato prima che l'applicazione disegni ogni fotogramma. Un singolo oggetto di gestione dell'animazione gestisce in genere tutte le animazioni in un'applicazione e pertanto ha il controllo globale su tutti gli storyboard pianificati.

</dd> <dt>

<span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>variabili di animazione
</dt> <dd>

Prima di avviare le animazioni, un'applicazione deve creare oggetti variabili di animazione. Una variabile di animazione rappresenta un aspetto di un elemento visivo da animare. La variabile è un valore a virgola mobile scalare, anche se il valore può essere arrotondato a un valore integer.

Una variabile di animazione ha in genere la stessa durata dell'elemento visivo che deve animare. Il valore iniziale di una variabile di animazione viene specificato al momento della creazione della variabile. Successivamente, il relativo valore non può essere modificato direttamente. deve essere aggiornato tramite gestione animazione.

Una variabile di animazione può essere identificata da *un tag*, che è un abbinamento di un identificatore integer con un puntatore a un oggetto COM. Un tag non deve essere univoco, a meno che l'applicazione non lo usi per cercare una variabile. Per impostazione predefinita, una variabile di animazione non ha un tag e qualsiasi tentativo di leggerne il tag avrà esito negativo fino a quando non ne viene impostato uno.

</dd> <dt>

<span id="timing_system"></span><span id="TIMING_SYSTEM"></span>sistema di temporizzazione
</dt> <dd>

Windows L'animazione include un sistema di temporizzazione che consente di garantire il rendering delle animazioni a una frequenza di fotogrammi uniforme e coerente, riducendo al tempo stesso l'uso delle risorse di sistema per il rendering quando il sistema è occupato. Un *timer* consente di gestire il rendering dell'animazione indicando automaticamente il passaggio di una piccola unità di tempo, denominata *tick*. Il sistema di temporizzazione  monitora le prestazioni complessive del rendering del sistema e riduce le animazioni aumentando o diminuendo dinamicamente la frequenza dei tick. Le applicazioni possono consentire a un timer di guidare il gestore dell'animazione e di registrare un gestore per ricevere una notifica prima e dopo l'aggiornamento del gestore per ogni tick. Le applicazioni possono specificare la frequenza dei fotogrammi di animazione minima accettabile per un timer e ricevere una notifica se la frequenza effettiva dei fotogrammi di un'animazione scende al di sotto di questa frequenza.

Per risparmiare risorse di sistema, è possibile configurare un timer per disabilitare se stesso quando non viene attivata alcuna animazione.

</dd> </dl>

## <a name="the-windows-animation-api"></a>API Windows Animation

L Windows API Animation è un'API basata su COM a thread singolo che offre le funzionalità seguenti per gli sviluppatori:

-   Oggetto di gestione dell'animazione, [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)), per la creazione di oggetti di animazione e il controllo delle animazioni
-   Variabili di animazione e storyboard
-   Una libreria di base, [**UIAnimationTransitionLibrary,**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85))di transizioni pronte all'uso
-   Oggetto timer, [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)), per determinare l'ora corrente e, facoltativamente, per la guida dell'animazione
-   Hook di eventi per il monitoraggio dello stato e dello stato dell'animazione

Per informazioni di riferimento complete sull'API, vedere Windows [di animazione](windows-animation-reference.md). Per codice di esempio, vedere Windows [attività di animazione](using-windows-animation.md) e [Windows di animazione](windows-animation-samples.md).

## <a name="configurations"></a>Configurazioni

Le applicazioni devono ottenere l'ora corrente prima di pianificare una nuova animazione. Di seguito sono riportati i meccanismi di temporizzazione supportati Windows animation:

-   [Animazione basata sull'applicazione](#application-driven-animation)
-   [Animazione basata su timer](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven animazione

Le applicazioni che usano un'API grafica con accelerazione hardware possono eseguire la sincronizzazione con la frequenza di aggiornamento del monitoraggio per eseguire il rendering di animazioni uniformi. In alternativa, un'applicazione può usare un meccanismo di temporizzazione proprio per determinare quando disegnare ogni fotogramma di un'animazione. In entrambi i casi, l'applicazione dirà al gestore dell'animazione quando aggiornarne lo stato. Un timer di animazione può comunque essere usato per determinare l'ora corrente con precisione elevata, nelle unità richieste dal gestore dell'animazione.

Il diagramma seguente illustra le interazioni tra un'applicazione e i componenti Windows animation quando l'applicazione sta guidando direttamente gli aggiornamenti dell'animazione.

![diagramma che mostra le interazioni tra un'applicazione e i componenti di animazione di Windows quando l'applicazione sta guidando direttamente gli aggiornamenti dell'animazione.](images/animationupdates.png)

Nella configurazione più semplice, un'applicazione ridisegnerà tutto ogni volta che lo schermo viene aggiornato, anche quando non vengono riprodotte animazioni. Per evitare il lavoro sprecato, un'applicazione può registrare un gestore eventi di gestione per ricevere una notifica quando sono pianificate animazioni e può rilevare quando la pianificazione è vuota in modo che possa interrompere il ridisegno.

### <a name="timer-driven-animation"></a>Timer-Driven animazione

Anziché aggiornare direttamente gestione animazione, le applicazioni possono consentire al timer di animazione di indicare al gestore dell'animazione quando aggiornarne lo stato e di ricevere semplicemente una notifica quando è stato effettuato ogni aggiornamento. Questo approccio è consigliato per le API grafiche meno recenti. In generale, se è possibile eseguire la sincronizzazione con la frequenza di aggiornamento del monitoraggio, è meglio farlo e usare l'animazione basata sull'applicazione.

Il diagramma seguente illustra le interazioni tra un'applicazione e i componenti Windows animation quando il timer di animazione sta guidando gli aggiornamenti dell'animazione.

![diagramma che mostra le interazioni tra un'applicazione e i componenti di animazione di Windows quando il timer di animazione sta guidando gli aggiornamenti dell'animazione.](images/animationtimerupdates.png)

Il timer può essere configurato per l'esecuzione solo quando sono pianificate le animazioni. In questo modo è semplice passare un parametro specifico quando il timer e il gestore dell'animazione sono connessi.

## <a name="advanced-features"></a>Funzionalità avanzate

Oltre a una base di base per supportare l'animazione, Windows animation include il supporto per diverse tecniche di animazione avanzate, tra cui:

<dl> <dt>

<span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*durata sensibile al contesto*
</dt> <dd>

La durata di una transizione non deve essere fissata. può essere determinato in base al valore e alla velocità della variabile animata all'inizio della transizione.

</dd> <dt>

<span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*corrispondenza della velocità*
</dt> <dd>

Lo spostamento è in genere più piacevole per l'occhio se la posizione e la velocità di un oggetto in movimento non passano istantaneamente tra i valori. Quando un nuovo storyboard interrompe uno attualmente in esecuzione, la corrispondenza della velocità consente al nuovo storyboard di riprendere senza problemi il punto in cui è terminato quello precedente.

</dd> <dt>

<span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*gestione delle interezioni*
</dt> <dd>

Se due storyboard devono aggiornare la stessa variabile di animazione contemporaneamente, si verifica un conflitto di pianificazione. Anziché richiedere una priorità numerica specifica per ogni storyboard, Windows animation consente all'applicazione di determinare le priorità relative di due storyboard.

</dd> </dl>

### <a name="contention-management"></a>Gestione delle interezioni

Gli sviluppatori possono *implementare un* callback di confronto di priorità per confrontare la priorità dello storyboard da pianificare e lo storyboard già presente nella pianificazione. Un'applicazione che implementa un confronto di priorità può usare qualsiasi logica preferita per determinare quando uno storyboard ne preleva un altro. Per risolvere il conflitto di pianificazione, Windows animation chiede all'applicazione quale di queste azioni può essere eseguita, nell'ordine seguente:

-   **Annullare lo storyboard pianificato.** Se la riproduzione dello storyboard pianificato non è ancora iniziata, è possibile che venga annullata e immediatamente rimossa dalla pianificazione.
-   **Tagliare lo storyboard pianificato.** Quando un nuovo storyboard taglia uno storyboard pianificato, lo storyboard pianificato smette di influire sulla variabile non appena il nuovo storyboard inizia ad animarlo. Le velocità vengono abbinate, consentendo al nuovo storyboard di riprendere senza problemi il punto in cui quello precedente è stato lasciato.
-   **Chiudere lo storyboard pianificato.** Uno storyboard può essere terminato solo se contiene un ciclo che si ripete per un periodo illimitato. Se lo storyboard si trova in un ciclo di questo tipo quando viene terminato, la ripetizione corrente viene completata e viene riprodotta la parte restante dello storyboard. Se il ciclo non è ancora iniziato quando viene chiuso uno storyboard, il ciclo viene ignorato completamente.
-   **Comprimere lo storyboard pianificato.** Se il trimming o l'annullamento dello storyboard pianificato non è un'opzione, lo storyboard può essere completato. Windows L'animazione introduce la possibilità di comprimere il tempo disponibile per lo storyboard pianificato (e per tutti gli storyboard pianificati prima), in modo che le variabili raggiungano più rapidamente lo stato finale. Quando viene applicata la compressione, il tempo viene temporaneamente accelerato per gli storyboard interessati, in modo che la riproduzione sia più veloce.

Se nessuna delle azioni precedenti è consentita dagli oggetti di confronto di priorità registrati, il tentativo di pianificare il nuovo storyboard ha esito negativo. Per impostazione predefinita, tutti gli storyboard possono essere tagliati, concludeti o compressi per evitare errori, ma nessuno può essere annullato.

Il diagramma seguente illustra il ciclo di vita di uno storyboard, usando gli stati definiti dall'enumerazione [**UI \_ ANIMATION STORYBOARD \_ \_ STATUS.**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) Le applicazioni usano l Windows API animation per compilare uno storyboard e inviarlo per la pianificazione. Il gestore dell'animazione pianifica lo storyboard e gestisce l'animazione.

![Diagramma che illustra come il gestore dell'animazione pianifica lo storyboard e gestisce l'animazione.](images/statediagram.png)

Per altre informazioni sulla pianificazione e sulla gestione degli storyboard, vedere [Cenni preliminari sullo storyboard.](storyboard-construction.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Informazioni di riferimento sulle animazioni](windows-animation-reference.md)
</dt> <dt>

[Windows Esempi di animazione](windows-animation-samples.md)
</dt> <dt>

[Windows Attività di animazione](using-windows-animation.md)
</dt> </dl>

 

 