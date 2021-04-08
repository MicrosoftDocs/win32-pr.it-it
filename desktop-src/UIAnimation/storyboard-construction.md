---
title: Panoramica dello storyboard
description: Questa panoramica è incentrata sul modo in cui le transizioni e gli storyboard vengono usati nell'animazione di Windows.
ms.assetid: d37718ac-0256-4a24-a26c-d29173593be0
keywords:
- Animazione Windows Animation Windows, panoramica dello storyboard
- Animazione Windows storyboard, descritta
- Animazione Windows di transizione, descritta
- transizioni animazione Windows, personalizzata
- Animazione Windows degli interpolatori, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d8e0af3937cd31ccdc43216a9d3426bad0e7b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728103"
---
# <a name="storyboard-overview"></a>Panoramica dello storyboard

Questa panoramica è incentrata sul modo in cui le transizioni e gli storyboard vengono usati nell'animazione di Windows. Per una panoramica dei componenti di animazione Windows, vedere [Cenni preliminari sull'animazione di Windows](scenic-animation-api-overview.md).

In questo argomento sono incluse le sezioni seguenti:

-   [Transizioni](#custom-transitions)
    -   [Libreria di transizione](#transition-library)
    -   [Transizioni personalizzate](#custom-transitions)
-   [Storyboard](#storyboards)
    -   [Creazione di uno storyboard semplice](#building-a-simple-storyboard)
    -   [Utilizzo di una durata Context-Sensitive](#using-a-context-sensitive-duration)
    -   [Creazione di uno storyboard più complesso](#building-a-more-complex-storyboard)
    -   [Uso di fotogrammi chiave](#using-keyframes)
    -   [Variabili di contenimento](#holding-variables)
    -   [Pianificazione di uno storyboard](#scheduling-a-storyboard)
-   [Argomenti correlati](#related-topics)

## <a name="transitions"></a>Transizioni

Una transizione definisce il modo in cui una singola variabile di animazione viene modificata in un intervallo di tempo specifico. L'animazione Windows include una raccolta di transizioni comuni che gli sviluppatori possono applicare a una o più variabili di animazione. Tipi diversi di transizioni hanno set di parametri diversi, che possono includere il valore della variabile al termine della transizione, la durata della transizione o le quantità univoche della funzione matematica sottostante, ad esempio l'accelerazione o l'intervallo di oscillazione.

Tutte le transizioni condividono due parametri impliciti: il valore iniziale e la velocità iniziale (inclinazione) della funzione matematica. Questi possono essere specificati in modo esplicito dall'applicazione, ma vengono in genere impostati dal gestore delle animazioni sul valore e sulla velocità della variabile di animazione all'inizio della transizione.

-   [Libreria di transizione](#transition-library)
-   [Transizioni personalizzate](#custom-transitions)

### <a name="transition-library"></a>Libreria di transizione

La libreria di transizione attualmente fornisce le transizioni seguenti. Se un'applicazione richiede un effetto che non può essere specificato tramite la libreria di transizione, gli sviluppatori possono creare altri tipi di transizioni implementando un interpolatore personalizzato per l'applicazione o utilizzando una libreria di transizione da terze parti.



| Nome della transizione                        | Descrizione                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| accelerazione-decelerazione<br/>       | La variabile di animazione viene accelerata e quindi rallentata in una determinata durata.<br/>                                                                                                               |
| constant<br/>                    | La variabile di animazione rimane in corrispondenza del valore iniziale durante la transizione.<br/>                                                                                                            |
| cubiche<br/>                       | La variabile di animazione passa dal valore iniziale a un valore finale specificato, con una velocità finale specificata, in una determinata durata.<br/>                                                 |
| discreti<br/>                    | La variabile di animazione rimane in corrispondenza del valore iniziale per un intervallo di tempo specificato, quindi passa immediatamente a un valore finale specificato e rimane in corrispondenza di tale valore per un determinato periodo di tempo di attesa.<br/> |
| istantaneo<br/>               | La variabile di animazione cambia immediatamente dal valore corrente a un valore finale specificato.<br/>                                                                                               |
| linear<br/>                      | La variabile di animazione esegue la transizione lineare dal valore iniziale a un valore finale specificato in una durata specificata.<br/>                                                                      |
| lineare dalla velocità<br/>           | La variabile di animazione esegue la transizione lineare dal valore iniziale a un valore finale specificato con una velocità specificata.<br/>                                                                     |
| parabola dall'accelerazione<br/> | La variabile di animazione esegue la transizione dal valore iniziale a un valore finale specificato, con una velocità finale specificata, modificando la velocità con un'accelerazione specificata.<br/>               |
| inversione<br/>                    | La variabile cambia direzione per una durata specificata. Il valore finale sarà uguale al valore iniziale e la velocità finale sarà il negativo della velocità iniziale.<br/>          |
| sinusoidale dall'intervallo<br/>       | La variabile oscilla all'interno di un intervallo di valori specificato, con un periodo di oscillazione specificato, per una determinata durata.<br/>                                                                     |
| da velocità sinusoidale<br/>    | La variabile oscilla con un periodo di oscillazione specificato, per una durata specificata. L'ampiezza delle oscillazioni è determinata dalla velocità iniziale della variabile.<br/>                      |
| arresto graduale<br/>                 | La variabile di animazione passa a un punto di interruzione graduale in corrispondenza di un valore finale specificato, entro un intervallo di tempo massimo.<br/>                                                                              |



 

La tabella seguente contiene illustrazioni per ognuna di queste transizioni.



|                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![illustrazione di una transizione istantanea](images/instantaneoustransition.png)  ![illustrazione di una transizione costante](images/constanttransition.png)  ![illustrazione di una transizione lineare](images/lineartransition.png)  ![illustrazione di una transizione lineari dalla velocità](images/lineartransitionfromspeed.png)  ![illustrazione di una transizione discreta](images/discretetransition.png) |
| ![illustrazione di una transizione parabolica dall'accelerazione](images/parabolictransitionfromacceleration.png)  ![illustrazione di una transizione cubica](images/cubictransition.png)  ![illustrazione di una transizione senza interruzioni](images/smoothstoptransition.png)                                                                                                                                       |
| ![illustrazione di una transizione di inversione](images/reversaltransition.png)  ![illustrazione di una transizione sinusoidale dalla velocità](images/sinusolidaltransitionfromvelocity.png)  ![illustrazione di una transizione sinusoidale dall'intervallo](images/sinusolidaltransitionfromrange.png)                                                                                                                  |
| ![illustrazione di accellerate e decelerazione delle transizioni](images/acceleratedeceleratetransition.png)                                                                                                                                                                                                                                                                                               |



 

### <a name="custom-transitions"></a>Transizioni personalizzate

Un *interpolatore* definisce la funzione matematica che determina la modalità di modifica di una variabile di animazione nel tempo durante l'avanzamento dal valore iniziale a un valore finale. Ogni transizione nella libreria di transizione ha un oggetto interpolator associato fornito dal sistema e implementa la funzione di interpolazione. Se un'applicazione richiede un effetto che non può essere specificato tramite la libreria di transizione, può implementare una o più transizioni personalizzate implementando un oggetto interpolatore per ogni nuova transizione. Gli oggetti di interpolazione non possono essere usati direttamente dalle applicazioni ed è invece necessario eseguirne il wrapper in una transizione associata. Una *Factory di transizione* viene utilizzata per generare transizioni da un oggetto interpolatore. Per ulteriori informazioni, vedere [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) e [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory) .

Si noti che la maggior parte delle applicazioni disporrà di tutte le transizioni necessarie tramite la libreria di transizione e pertanto non sarà necessario implementare un interpolatore.

## <a name="storyboards"></a>Storyboard

Uno storyboard è una raccolta di transizioni applicate a una o più variabili di animazione nel tempo. È garantito che le transizioni in uno storyboard rimangano sincronizzate tra loro e che lo storyboard venga pianificato o annullato come unità. Dopo aver creato le transizioni desiderate, un'applicazione crea uno storyboard usando Gestione animazioni, aggiunge le transizioni allo storyboard, configura lo storyboard in modo appropriato e ne pianifica l'esecuzione appena possibile. Gestione animazioni determina l'ora di inizio effettiva dello storyboard, perché potrebbe esserci una contesa con altri storyboard che attualmente animano le stesse variabili.

La durata complessiva di uno storyboard dipende dalle durate delle transizioni all'interno dello storyboard. Non è necessario correggere la durata di una transizione. può essere determinato dal valore e dalla velocità delle variabili animate all'inizio della transizione. Quindi, la durata di uno storyboard può dipendere anche dallo stato delle variabili a cui viene aggiunta un'animazione.

Negli esempi seguenti si presuppone che siano stati creati un gestore delle animazioni, una libreria di transizione e un timer. Per altre informazioni, vedere [creare gli oggetti di animazione principali](adding-animation-to-an-application.md). Negli esempi si presuppone inoltre che l'applicazione abbia creato tre variabili di animazione (X, Y e Z) tramite il metodo [**IUIAnimationManager:: CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) e cinque transizioni (T1, T2, T3, T4 e T5) utilizzando uno dei metodi dell'interfaccia [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary) .

-   [Creazione di uno storyboard semplice](#building-a-simple-storyboard)
-   [Utilizzo di una durata Context-Sensitive](#using-a-context-sensitive-duration)
-   [Creazione di uno storyboard più complesso](#building-a-more-complex-storyboard)
-   [Uso di fotogrammi chiave](#using-keyframes)
-   [Variabili di contenimento](#holding-variables)
-   [Pianificazione di uno storyboard](#scheduling-a-storyboard)

### <a name="building-a-simple-storyboard"></a>Creazione di uno storyboard semplice

Per compilare uno storyboard semplice, usare il metodo [**IUIAnimationManager:: CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) per creare un nuovo storyboard, il metodo [**IUIAnimationTransitionLibrary:: CreateLinearTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition) per creare una transizione lineare, T1 e il metodo [**IUIAnimationStoryboard:: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) per applicare la transizione T1 alla variabile X e aggiungere la transizione risultante allo storyboard.

Questo processo produce uno storyboard semplice, come illustrato nella figura seguente. Lo storyboard contiene una transizione, T1, in modo che il valore della variabile X venga modificato in modo lineare per un periodo di tempo fisso.

![illustrazione che mostra uno storyboard semplice con una durata fissa](images/simplestoryboardfixedduration.png)

Si noti che per questo semplice scenario, un'opzione alternativa consiste nell'usare il metodo [**IUIAnimationManager:: ScheduleTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-scheduletransition) .

### <a name="using-a-context-sensitive-duration"></a>Utilizzo di una durata Context-Sensitive

Mentre alcune transizioni hanno una durata fissa, la durata di altri dipende dal valore iniziale o dalla velocità della variabile animata all'inizio della transizione. Ad esempio, il metodo [**IUIAnimationTransitionLibrary:: CreateLinearTransitionFromSpeed**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed) crea una transizione con una durata proporzionale alla differenza tra il valore iniziale della variabile di animazione e il valore finale specificato. In questa illustrazione e le illustrazioni rimanenti, ad esempio le transizioni con durate arbitrarie, vengono visualizzate con un punto interrogativo (?) e le durate effettive vengono determinate quando lo storyboard viene riprodotto.

![illustrazione che mostra uno storyboard semplice con durata sconosciuta](images/simplestoryboardunknownduration.png)

### <a name="building-a-more-complex-storyboard"></a>Creazione di uno storyboard più complesso

Dopo la creazione di uno storyboard e l'aggiunta di una singola transizione, T1, è possibile aggiungere una seconda transizione per la variabile X chiamando di nuovo il metodo [**IUIAnimationStoryboard:: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) , ma con T2 anziché T1.

Supponendo che la transizione T2 abbia una durata che è sensibile al contesto, lo storyboard contiene ora due transizioni back-to-back di durata arbitraria che interessano la variabile X.

![illustrazione che mostra uno storyboard contenente due transizioni sulla stessa variabile](images/appendingwithaddtransition.png)

La chiamata di [**AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) con la variabile Y e la transizione T3 aggiunge una terza transizione all'inizio dello storyboard. A seconda dei valori di X e Y quando lo storyboard viene riprodotto, T3 può terminare dopo T1 o anche dopo T2.

![illustrazione che mostra uno storyboard che contiene le transizioni tra più variabili](images/multivariablestoryboard.png)

### <a name="using-keyframes"></a>Uso di fotogrammi chiave

Per aggiungere una transizione in corrispondenza di un offset dall'inizio dello storyboard, è necessario innanzitutto aggiungere un fotogramma chiave. I fotogrammi chiave rappresentano istanti nel tempo e non hanno alcun effetto sul comportamento dello storyboard. Ogni Storyboard ha un fotogramma chiave implicito che rappresenta l'inizio dello storyboard, il fotogramma [**chiave di animazione dell'interfaccia utente \_ \_ \_ \_ iniziale**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85)). è possibile aggiungere nuovi fotogrammi chiave in corrispondenza degli offset dall'inizio chiamando il metodo [**IUIAnimationStoryboard:: AddKeyframeAtOffset**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset) con l' **avvio dello \_ \_ \_ Storyboard \_ del fotogramma chiave di animazione dell'interfaccia utente**.

L'offset in corrispondenza del quale si aggiunge un fotogramma chiave è sempre relativo a un altro fotogramma chiave. Il diagramma seguente mostra il risultato dell'aggiunta di keyframe1 e Transition T4, applicata alla variabile Z, allineata a keyframe1 e creata con una durata fissa. Naturalmente, poiché le durate delle altre transizioni non sono ancora note, T4 potrebbe non essere l'ultima transizione da completare.

![illustrazione che mostra l'aggiunta di una transizione allineata a un fotogramma chiave](images/addtransitionatkeyframe.png)

I fotogrammi chiave possono essere posizionati anche al termine delle transizioni, usando il metodo [**IUIAnimationStoryboard:: AddKeyframeAfterTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition) . Il diagramma seguente mostra il risultato dell'aggiunta di keyframe2 dopo T1 e keyframe3 dopo T2.

![illustrazione che mostra l'aggiunta di fotogrammi chiave dopo varie transizioni](images/addkeyframeaftertransition.png)

Poiché le durate di T1 e T2 non sono note finché lo storyboard non viene riprodotto, anche gli offset di keyframe2 e keyframe3 non vengono determinati fino a quel momento. Di conseguenza, keyframe2 e anche keyframe3 possono verificarsi prima di keyframe1.

Sia l'inizio che la fine di una transizione possono essere allineati con fotogrammi chiave usando il metodo [**IUIAnimationStoryboard:: AddTransitionBetweenKeyframes**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes) . Il diagramma seguente mostra il risultato dell'aggiunta di una quinta transizione, T5, sulla variabile Y, tra keyframe2 e keyframe3. Questa operazione modifica la durata di T5, rendendola più lunga o più breve a seconda degli offset relativi di keyframe2 e keyframe3.

![illustrazione che mostra additon di una transizione tra fotogrammi chiave](images/addtransitionbetweenkeyframes.png)

### <a name="holding-variables"></a>Variabili di contenimento

Se T4 termina dopo T2 e T5, lo storyboard interrompe l'animazione delle variabili X e Y, rendendole disponibili per l'animazione di altri storyboard. Tuttavia, l'applicazione può chiamare il metodo [**IUIAnimationStoryboard:: HoldVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-holdvariable) per richiedere che lo storyboard includa alcune o tutte le variabili a cui viene aggiunta un'animazione nei valori finali fino al completamento dello storyboard. Il diagramma seguente mostra il risultato dell'esecuzione di X e Z quando T4 termina per ultimo. Si noti che lo storyboard contiene X al valore finale fino al completamento dello storyboard. L'attesa non ha alcun effetto sulla Z perché lo storyboard termina quando T4 termina.

![illustrazione che mostra le variabili in corrispondenza dei valori finali fino al completamento dello storyboard](images/holdvariable.png)

Sebbene Y non venga mantenuto da questo storyboard, il relativo valore non viene modificato dopo il completamento di T5, a meno che un altro Storyboard non lo anima. Poiché Y non viene mantenuto, qualsiasi altro Storyboard, indipendentemente dalla priorità, può aggiungere un'animazione a Y dopo il completamento di T5. Al contrario, poiché viene mantenuta la X, uno storyboard con priorità inferiore non può animare X fino al termine dello storyboard.

Tutte queste illustrazioni hanno assunto un set arbitrario di valori correnti per le variabili quando lo storyboard inizia la riproduzione. Se vengono rilevati altri valori, è probabile che le durate delle transizioni sensibili al contesto siano diverse, come illustrato nella figura seguente.

![illustrazione che mostra il risultato della modifica delle condizioni iniziali usate per la figura precedente](images/holdvariablez.png)

In questo scenario T5 inizia prima del completamento di T3 e T3 viene quindi tagliato. Poiché T4 termina prima di T2 e T5, il valore di Z viene mantenuto fino alla fine dello storyboard. In generale, i valori e le velocità delle variabili quando uno storyboard inizia la riproduzione possono influenzare l'ordinamento dei fotogrammi chiave e la lunghezza e la forma complessiva dello storyboard.

### <a name="scheduling-a-storyboard"></a>Pianificazione di uno storyboard

Quando si pianifica uno storyboard, l'ora di inizio viene determinata in base alla struttura e ai contorni degli storyboard attualmente presenti nella pianificazione. In particolare, il primo e l'ultimo momento in cui lo storyboard aggiunge un'animazione a ogni singola variabile determina se e quando due storyboard sono in conflitto, ma i dettagli interni delle transizioni all'interno di non sono importanti.

Nella figura seguente viene illustrata la struttura di uno storyboard con cinque transizioni che animano tre variabili.

![illustrazione che mostra uno storyboard con cinque transizioni che animano tre variabili](images/storyboardwithoutline.png)

Un elemento fondamentale della piattaforma di animazione Windows è il supporto per consentire il completamento di un'animazione prima che un'altra venga avviata, se necessario. Sebbene questo elimini molti problemi logici, introduce anche una latenza arbitraria nell'interfaccia utente. Per risolvere questo problema, le applicazioni possono specificare il *ritardo accettabile più lungo* per l'avvio di uno storyboard, usando il metodo [**IUIAnimationStoryboard:: SetLongestAcceptableDelay**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay) e il gestore delle animazioni usa queste informazioni per pianificare lo storyboard prima della scadenza del periodo di latenza specificato. Quando si pianifica uno storyboard, gestione animazioni determina se è necessario prima annullare, tagliare, concludere e/o comprimere altri storyboard.

Un'applicazione può registrare un gestore che verrà chiamato quando viene modificato lo stato di uno storyboard. Ciò consente all'applicazione di rispondere quando lo storyboard inizia la riproduzione, viene eseguito fino al completamento, viene rimosso interamente dalla pianificazione o non può essere completato a causa di un'interruzione da parte di uno storyboard con priorità più alta. Per identificare gli storyboard passati ai gestori eventi Storyboard (o i confronti di priorità), un'applicazione può usare il metodo [**IUIAnimationStoryboard:: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-settag) per applicare tag agli storyboard, in modo analogo a quelli che possono essere usati per identificare le variabili. Come per il riutilizzo dello storyboard, gli sviluppatori devono prestare attenzione quando si usano i tag per identificare gli storyboard e assicurarsi che le ambiguità non si verifichino quando le azioni dell'utente comportano la coda di molti storyboard.

Negli esempi seguenti vengono illustrate due varianti di un tentativo di pianificazione dello storyboard compilato nelle sezioni precedenti di questo argomento.

In questo scenario, sei storyboard da A a F sono già stati pianificati per aggiungere un'animazione alle variabili W, X, Y e Z, ma solo A e B hanno iniziato a eseguire la riproduzione. Il nuovo storyboard, con etichetta G, ha un ritardo accettabile più lungo impostato sulla durata indicata nella figura seguente.

![illustrazione che mostra l'aggiunta di un nuovo storyboard alla pianificazione esistente](images/existingschedule1withlines.png)

L'applicazione ha registrato confronti di priorità che includono la logica seguente:

-   G può annullare solo C ed e e solo per evitare errori.
-   G può tagliare solo a, C, e e F e solo per evitare errori.
-   Qualsiasi storyboard può comprimere qualsiasi altro Storyboard (la compressione viene sempre eseguita solo per evitare errori).

> [!Note]  
> Il qualificatore "solo per evitare errori" indica che i confronti di priorità registrati restituiscono S \_ OK solo quando il parametro *priorityEffect* è un **\_ \_ \_ \_ errore di effetto priorità di animazione interfaccia utente**. Per informazioni dettagliate, vedere il metodo [**IUIAnimationPriorityComparison:: HasPriority**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationprioritycomparison-haspriority) .

 

Per avviare G prima che sia trascorso il ritardo accettabile più lungo, il gestore delle animazioni deve eseguire le operazioni seguenti:

-   Trim F
-   Annulla E

Quando E viene annullato, vengono individuati i risultati D e F e vengono ripristinati i relativi contorni originali:

![illustrazione che mostra le strutture originali](images/existingschedule1bwithlines.png)

Il gestore delle animazioni non deve annullare o tagliare C per pianificare prima che sia trascorso il ritardo accettabile più lungo, quindi la riunione di C e G determina quando G viene avviato.

![illustrazione che mostra che f viene tagliato per consentire il raggiungimento di c e g](images/schedule1withgwithlines.png)

Una volta pianificata correttamente G, è possibile determinare la durata delle transizioni e il resto del contorno è quindi noto. Tuttavia, la struttura può cambiare se un altro Storyboard viene successivamente rimosso dalla pianificazione.

Come secondo esempio, si consideri uno scenario come quello precedente, ma con un ritardo più breve accettabile più lungo specificato per G.

![illustrazione che mostra lo scenario precedente, ma con un ritardo più breve accettabile più lungo per g](images/existingschedule2withlines.png)

In questo caso, vengono eseguite le azioni seguenti:

-   Trim F
-   Annulla E
-   Annulla C

Inoltre, il gestore delle animazioni deve comprimere D in base alla quantità indicata per abilitare G per l'avvio dopo il ritardo accettabile più lungo e non in un secondo momento.

![illustrazione che mostra dove d deve essere compresso per consentire l'avvio di g a un ritardo più lungo accettabile](images/trimmedandcancelledwithlines.png)

Per mantenere l'intervallo relativo, A, B e F vengono compressi.

![illustrazione che mostra un oggetto, b, d e f compresso](images/schedule2withgwithlines.png)

Tuttavia, gli storyboard in variabili non correlate (non visualizzate) non vengono compressi.

Ancora una volta, il contorno di G è ora noto ed è diverso dal risultato nel primo scenario perché le variabili hanno valori diversi quando G inizia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationPriorityComparison**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)
</dt> <dt>

[**IUIAnimationStoryboard**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> </dl>

 

