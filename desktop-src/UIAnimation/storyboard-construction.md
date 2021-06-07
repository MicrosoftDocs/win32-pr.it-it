---
title: Panoramica dello storyboard
description: Questa panoramica è incentrata sul modo in cui le transizioni e gli storyboard vengono usati nell'animazione di Windows.
ms.assetid: d37718ac-0256-4a24-a26c-d29173593be0
keywords:
- Animazione di Windows Animation , panoramica dello storyboard
- storyboard Animazione di Windows , descritto
- transizioni animazione di Windows, descritto
- transizioni animazione di Windows, personalizzata
- interpolatori Windows Animation ,descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58210ae98f6d3a96c554276466ad72b3364d72a1
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524285"
---
# <a name="storyboard-overview"></a>Panoramica dello storyboard

Questa panoramica è incentrata sul modo in cui le transizioni e gli storyboard vengono usati nell'animazione di Windows. Per una panoramica dei componenti dell'animazione di Windows, vedere [Cenni preliminari sull'animazione di Windows](scenic-animation-api-overview.md).

In questo argomento sono incluse le sezioni seguenti:

-   [Transizioni](#custom-transitions)
    -   [Libreria di transizioni](#transition-library)
    -   [Transizioni personalizzate](#custom-transitions)
-   [Storyboard](#storyboards)
    -   [Compilazione di uno storyboard semplice](#building-a-simple-storyboard)
    -   [Uso di una durata Context-Sensitive predefinita](#using-a-context-sensitive-duration)
    -   [Compilazione di uno storyboard più complesso](#building-a-more-complex-storyboard)
    -   [Uso dei fotogrammi chiave](#using-keyframes)
    -   [Contenere variabili](#holding-variables)
    -   [Pianificazione di uno storyboard](#scheduling-a-storyboard)
-   [Argomenti correlati](#related-topics)

## <a name="transitions"></a>Transizioni

Una transizione definisce il modo in cui una singola variabile di animazione cambia in un intervallo di tempo specifico. Windows Animation include una libreria di transizioni comuni che gli sviluppatori possono applicare a una o più variabili di animazione. Diversi tipi di transizioni hanno set diversi di parametri, che possono includere il valore della variabile al termine della transizione, la durata della transizione o quantità univoche per la funzione matematica sottostante, ad esempio accelerazione o intervallo di oscillazione.

Tutte le transizioni condividono due parametri impliciti: il valore iniziale e la velocità iniziale (pendenza) della funzione matematica. Possono essere specificati in modo esplicito dall'applicazione, ma in genere vengono impostati dal gestore dell'animazione sul valore e sulla velocità della variabile di animazione all'inizio della transizione.

-   [Libreria di transizioni](#transition-library)
-   [Transizioni personalizzate](#custom-transitions)

### <a name="transition-library"></a>Libreria di transizioni

Le transizioni seguenti sono attualmente fornite dalla libreria di transizione. Se un'applicazione richiede un effetto che non può essere specificato tramite la libreria di transizione, gli sviluppatori possono creare altri tipi di transizioni implementando un interpolatore personalizzato per l'applicazione o usando una libreria di transizione di terze parti.



| Nome della transizione                        | Descrizione                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| accelerate-decelerate<br/>       | La variabile di animazione accelera e quindi rallenta per una determinata durata.<br/>                                                                                                               |
| constant<br/>                    | La variabile di animazione rimane al valore iniziale durante la transizione.<br/>                                                                                                            |
| cubiche<br/>                       | La variabile di animazione cambia dal valore iniziale a un valore finale specificato, con una velocità finale specificata, per una determinata durata.<br/>                                                 |
| Discreti<br/>                    | La variabile di animazione rimane al valore iniziale per un tempo di ritardo specificato, quindi passa immediatamente a un valore finale specificato e rimane a tale valore per un determinato tempo di attesa.<br/> |
| Istantanea<br/>               | La variabile di animazione cambia immediatamente dal valore corrente a un valore finale specificato.<br/>                                                                                               |
| linear<br/>                      | La variabile di animazione esegue la transizione lineare dal valore iniziale a un valore finale specificato per una determinata durata.<br/>                                                                      |
| lineare dalla velocità<br/>           | La variabile di animazione esegue la transizione lineare dal valore iniziale a un valore finale specificato con una velocità specificata.<br/>                                                                     |
| parabolico dall'accelerazione<br/> | La variabile di animazione passa dal valore iniziale a un valore finale specificato, con una velocità finale specificata, modificandone la velocità con un'accelerazione specificata.<br/>               |
| Inversione<br/>                    | La variabile cambia direzione per una determinata durata. Il valore finale sarà uguale al valore iniziale e la velocità finale sarà negativa della velocità iniziale.<br/>          |
| sinusoidale dall'intervallo<br/>       | La variabile oscilla all'interno di un determinato intervallo di valori, con un periodo di oscillazione specificato, per una determinata durata.<br/>                                                                     |
| sinusoidale dalla velocità<br/>    | La variabile oscilla con un periodo di oscillazione specificato, per una determinata durata. L'ampiezza dell'oscillazione è determinata dalla velocità iniziale della variabile.<br/>                      |
| arresto uniforme<br/>                 | La variabile di animazione viene interrotta gradualmente in corrispondenza di un valore finale specificato, entro un periodo di tempo massimo.<br/>                                                                              |



 

La tabella seguente contiene illustrazioni per ognuna di queste transizioni.



|    Illustrazioni                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Illustrazione di una transizione istantanea](images/instantaneoustransition.png)  ![Illustrazione di una transizione costante](images/constanttransition.png)  ![illustrazione di una transizione lineare](images/lineartransition.png)  ![Illustrazione di una transizione lineare dalla velocità](images/lineartransitionfromspeed.png)  ![Illustrazione di una transizione discreta](images/discretetransition.png) |
| ![Illustrazione di una transizione parabolica dall'accelerazione](images/parabolictransitionfromacceleration.png)  ![illustrazione di una transizione cubica](images/cubictransition.png)  ![Illustrazione di una transizione di arresto uniforme](images/smoothstoptransition.png)                                                                                                                                       |
| ![Illustrazione di una transizione inversa](images/reversaltransition.png)  ![illustrazione di una transizione sinusoidale dalla velocità](images/sinusolidaltransitionfromvelocity.png)  ![Illustrazione di una transizione sinusoidale dall'intervallo](images/sinusolidaltransitionfromrange.png)                                                                                                                  |
| ![Illustrazione delle transizioni di accellerate e decelerate](images/acceleratedeceleratetransition.png)                                                                                                                                                                                                                                                                                               |



 

### <a name="custom-transitions"></a>Transizioni personalizzate

Un *interpolatore* definisce la funzione matematica che determina il modo in cui una variabile di animazione cambia nel tempo mentre avanza dal valore iniziale a un valore finale. A ogni transizione nella libreria di transizione è associato un oggetto interpolatore fornito dal sistema e implementa la funzione dell'interpolatore. Se un'applicazione richiede un effetto che non può essere specificato usando la libreria di transizione, può implementare una o più transizioni personalizzate implementando un oggetto interpolatore per ogni nuova transizione. Gli oggetti interpolatore non possono essere usati direttamente dalle applicazioni e devono invece essere incapsulati in una transizione associata. Una *factory di transizione* viene usata per generare transizioni da un oggetto interpolatore. Per [**altri dettagli, vedere IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) e [**IUIAnimationTransitionFactory.**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory)

Si noti che la maggior parte delle applicazioni avrà tutte le transizioni necessarie usando la libreria di transizione e pertanto non dovrà implementare un interpolatore.

## <a name="storyboards"></a>Storyboard

Uno storyboard è una raccolta di transizioni applicate a una o più variabili di animazione nel tempo. È garantito che le transizioni in uno storyboard rimangano sincronizzate l'una rispetto all'altra e lo storyboard viene pianificato o annullato come unità. Dopo aver creato le transizioni desiderate, un'applicazione crea uno storyboard usando gestione animazione, aggiunge le transizioni allo storyboard, configura lo storyboard in modo appropriato e lo pianifica per la riproduzione il prima possibile. Il gestore dell'animazione determina l'ora di inizio effettiva dello storyboard, perché potrebbero verificarsi problemi con altri storyboard che animano attualmente le stesse variabili.

La durata complessiva di uno storyboard dipende dalle durate delle transizioni all'interno dello storyboard. La durata di una transizione non deve essere fissata. può essere determinato dal valore e dalla velocità delle variabili animate all'inizio della transizione. La durata di uno storyboard può quindi dipendere anche dallo stato delle variabili a cui viene animata.

Gli esempi seguenti presuppongono che siano stati creati un gestore di animazione, una libreria di transizione e un timer. Per altre informazioni, vedere [Creare oggetti di animazione principali](adding-animation-to-an-application.md). Gli esempi presuppongono anche che l'applicazione abbia creato tre variabili di animazione (X, Y e Z) usando il metodo [**IUIAnimationManager::CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) e cinque transizioni (T1, T2, T3, T4 e T5) usando uno dei metodi [**dell'interfaccia IUIAnimationTransitionLibrary.**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)

-   [Compilazione di uno storyboard semplice](#building-a-simple-storyboard)
-   [Uso di una durata Context-Sensitive predefinita](#using-a-context-sensitive-duration)
-   [Compilazione di uno storyboard più complesso](#building-a-more-complex-storyboard)
-   [Uso dei fotogrammi chiave](#using-keyframes)
-   [Contenere variabili](#holding-variables)
-   [Pianificazione di uno storyboard](#scheduling-a-storyboard)

### <a name="building-a-simple-storyboard"></a>Compilazione di uno storyboard semplice

Per compilare uno storyboard semplice, usare il metodo [**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) per creare un nuovo storyboard, il metodo [**IUIAnimationTransitionLibrary::CreateLinearTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition) per creare una transizione lineare, T1, e il metodo [**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) per applicare la transizione T1 alla variabile X e aggiungere la transizione risultante allo storyboard.

Questo processo produce uno storyboard semplice, come illustrato nella figura seguente. Lo storyboard contiene una transizione, T1, in modo che il valore della variabile X cambi linearmente per un periodo di tempo fisso.

![Illustrazione che mostra uno storyboard semplice con una durata fissa](images/simplestoryboardfixedduration.png)

Si noti che per uno scenario così semplice, un'opzione alternativa consiste nell'usare il [**metodo IUIAnimationManager::ScheduleTransition.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-scheduletransition)

### <a name="using-a-context-sensitive-duration"></a>Uso di una durata Context-Sensitive predefinita

Anche se alcune transizioni hanno una durata fissa, la durata di altre dipende dal valore iniziale o dalla velocità della variabile animata all'inizio della transizione. Ad esempio, il metodo [**IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed) crea una transizione con una durata proporzionale alla differenza tra il valore iniziale della variabile di animazione e il valore finale specificato. In questa illustrazione, e nelle illustrazioni rimanenti, tali transizioni con durate arbitrarie vengono visualizzate con un punto interrogativo (?) e le relative durate effettive vengono determinate quando viene riprodotto lo storyboard.

![Illustrazione che mostra uno storyboard semplice con una durata sconosciuta](images/simplestoryboardunknownduration.png)

### <a name="building-a-more-complex-storyboard"></a>Compilazione di uno storyboard più complesso

Dopo aver creato uno storyboard e aver aggiunto una singola transizione, T1, è possibile aggiungere una seconda transizione per la variabile X chiamando di nuovo il metodo [**IUIAnimationStoryboard::AddTransition,**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) ma con T2 anziché con T1.

Supponendo che la transizione T2 abbia una durata sensibile al contesto, lo storyboard contiene ora due transizioni back-to-back di durata arbitraria che interessano la variabile X.

![Figura che mostra uno storyboard contenente due transizioni nella stessa variabile](images/appendingwithaddtransition.png)

Chiamando [**nuovamente AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) con la variabile Y e la transizione T3 viene aggiunta una terza transizione all'inizio dello storyboard. A seconda dei valori di X e Y quando viene riprodotto lo storyboard, T3 può terminare dopo T1 o anche dopo T2.

![Illustrazione che mostra uno storyboard contenente transizioni tra più variabili](images/multivariablestoryboard.png)

### <a name="using-keyframes"></a>Uso dei fotogrammi chiave

Per aggiungere una transizione in corrispondenza di un offset dall'inizio dello storyboard, è prima necessario aggiungere un fotogramma chiave. I fotogrammi chiave rappresentano istantanei nel tempo e di per sé non hanno alcun effetto sul comportamento dello storyboard. Ogni storyboard ha un fotogramma chiave implicito che rappresenta l'inizio dello storyboard, [**UI \_ ANIMATION \_ KEYFRAME STORYBOARD \_ \_ START.**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))È possibile aggiungere nuovi fotogrammi chiave in corrispondenza degli offset dall'inizio chiamando il metodo [**IUIAnimationStoryboard::AddKeyframeAtOffset**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset) con UI **ANIMATION \_ \_ KEYFRAME STORYBOARD \_ \_ START.**

L'offset in corrispondenza del quale si aggiunge un fotogramma chiave è sempre relativo a un altro fotogramma chiave. Il diagramma seguente mostra il risultato dell'aggiunta di keyframe1 e della transizione T4, che viene applicata alla variabile Z, allineata a keyframe1 e creata con una durata fissa. Naturalmente, poiché le durate delle altre transizioni non sono ancora note, T4 potrebbe non essere l'ultima transizione da completare.

![Figura che mostra l'aggiunta di una transizione allineata in corrispondenza di un fotogramma chiave](images/addtransitionatkeyframe.png)

I fotogrammi chiave possono anche essere posizionati alle estremità delle transizioni usando il metodo [**IUIAnimationStoryboard::AddKeyframeAfterTransition.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition) Il diagramma seguente mostra il risultato dell'aggiunta di keyframe2 dopo T1 e keyframe3 dopo T2.

![Illustrazione che mostra l'aggiunta di fotogrammi chiave dopo varie transizioni](images/addkeyframeaftertransition.png)

Poiché le durate di T1 e T2 non sono note fino alla riproduzione dello storyboard, gli offset di keyframe2 e keyframe3 non vengono determinati fino a quel momento. Di conseguenza, keyframe2 e anche keyframe3 possono verificarsi prima di keyframe1.

Sia l'inizio che la fine di una transizione possono essere allineati ai fotogrammi chiave usando il metodo [**IUIAnimationStoryboard::AddTransitionBetweenKeyframes.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes) Il diagramma seguente mostra il risultato dell'aggiunta di una quinta transizione, T5, sulla variabile Y, tra keyframe2 e keyframe3. Ciò modifica la durata di T5, rendendola più lunga o più breve a seconda degli offset relativi di keyframe2 e keyframe3.

![Figura che mostra l'additone di una transizione tra fotogrammi chiave](images/addtransitionbetweenkeyframes.png)

### <a name="holding-variables"></a>Contenere variabili

Se T4 termina dopo T2 e T5, lo storyboard interrompe l'animazione delle variabili X e Y, rendendole disponibili per l'animazione degli altri storyboard. Tuttavia, l'applicazione può chiamare il metodo [**IUIAnimationStoryboard::HoldVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-holdvariable) per richiedere che lo storyboard manteni alcune o tutte le variabili a cui aggiunge un'animazione ai valori finali fino al completamento dello storyboard. Il diagramma seguente mostra il risultato di mantenere X e Z quando T4 termina per ultimo. Si noti che lo storyboard mantiene X al valore finale fino al completamento dello storyboard. Il blocco non ha alcun effetto su Z perché lo storyboard termina al termine di T4.

![Illustrazione che mostra il controllo delle variabili ai valori finali fino al completamento dello storyboard](images/holdvariable.png)

Anche se Y non è contenuto in questo storyboard, il relativo valore non cambia dopo il completamento di T5, a meno che non venga animato da un altro storyboard. Poiché Y non viene mantenuto, qualsiasi altro storyboard, indipendentemente dalla priorità, può animare Y al termine di T5. Al contrario, poiché X viene mantenuto, uno storyboard con priorità inferiore non può animare X fino al completamento dello storyboard.

Tutte queste illustrazioni hanno assunto un set arbitrario di valori correnti per le variabili all'avvio della riproduzione dello storyboard. Se vengono rilevati altri valori, è probabile che le durate delle transizioni sensibili al contesto siano diverse, come illustrato nella figura seguente.

![Figura che mostra il risultato della modifica delle condizioni iniziali usate per l'illustrazione precedente](images/holdvariablez.png)

In questo scenario, T5 inizia prima del termine di T3 e T3 viene quindi tagliato. Poiché T4 termina prima di T2 e T5, il valore di Z viene mantenuto fino alla fine dello storyboard. In generale, i valori e le velocità delle variabili all'avvio della riproduzione di uno storyboard possono influire sull'ordinamento dei fotogrammi chiave e sulla lunghezza e la forma complessive dello storyboard.

### <a name="scheduling-a-storyboard"></a>Pianificazione di uno storyboard

Quando si pianifica uno storyboard, l'ora di inizio è determinata dalla struttura e dalle strutture degli storyboard attualmente nella pianificazione. In particolare, il primo e l'ultimo momento in cui lo storyboard aggiunge un'animazione a ogni singola variabile determinano se e quando due storyboard si scontrano, ma i dettagli interni delle transizioni all'interno non sono importanti.

La figura seguente illustra la struttura di uno storyboard con cinque transizioni che animano tre variabili.

![Figura che mostra uno storyboard con cinque transizioni che animano tre variabili](images/storyboardwithoutline.png)

Un elemento fondamentale della piattaforma Windows Animation è il supporto per consentire il completamento di un'animazione prima dell'inizio di un'altra, se necessario. Questa operazione elimina molti problemi logici, ma introduce anche una latenza arbitraria nell'interfaccia utente. Per risolvere questo problema,  le applicazioni possono specificare il ritardo accettabile più lungo per l'avvio di uno storyboard, usando il metodo [**IUIAnimationStoryboard::SetLongestAcceptableDelay**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay) e il gestore dell'animazione usa queste informazioni per pianificare lo storyboard prima che sia trascorso il periodo di latenza specificato. Quando viene pianificato uno storyboard, il gestore dell'animazione determina se gli altri storyboard devono prima essere annullati, tagliati, conclusi e/o compressi.

Un'applicazione può registrare un gestore che verrà chiamato quando cambia lo stato di uno storyboard. In questo modo l'applicazione può rispondere quando lo storyboard inizia a essere riprodotto, viene eseguito fino al completamento, viene rimosso completamente dalla pianificazione o viene impedito il completamento a causa di un'interruzione di uno storyboard con priorità più alta. Per identificare gli storyboard passati ai gestori eventi dello storyboard (o confronti di priorità), un'applicazione può usare il metodo [**IUIAnimationStoryboard::SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-settag) per applicare tag agli storyboard, in modo analogo a quelli che possono essere usati per identificare le variabili. Come per il ri-uso dello storyboard, gli sviluppatori devono prestare attenzione quando usano i tag per identificare gli storyboard e assicurarsi che le ambiguità non si verificano quando le azioni dell'utente comportano l'accodamento di molti storyboard.

Negli esempi seguenti vengono mostrate due varianti di un tentativo di pianificazione dello storyboard compilato nelle sezioni precedenti di questo argomento.

In questo scenario sono già stati pianificati sei storyboard, da A a F, per animare le variabili W, X, Y e Z, ma solo A e B hanno iniziato a riprodurre. Il nuovo storyboard, con etichetta G, ha il ritardo accettabile più lungo impostato sulla durata illustrata nella figura seguente.

![Figura che mostra l'aggiunta di un nuovo storyboard alla pianificazione esistente](images/existingschedule1withlines.png)

L'applicazione ha confronti di priorità registrati che includono la logica seguente:

-   G può annullare solo C ed E e solo per evitare errori.
-   G può tagliare solo A, C, E e F e solo per evitare errori.
-   Qualsiasi storyboard può comprimere qualsiasi altro storyboard (la compressione viene sempre eseguita solo per evitare errori).

> [!Note]  
> Il qualificatore "only to prevent failure" indica che i confronti di priorità registrati restituiscono S OK solo quando il \_ *parametro priorityEffect* è **UI ANIMATION PRIORITY EFFECT \_ \_ \_ \_ FAILURE**. Per informazioni dettagliate, vedere il metodo [**IUIAnimationPriorityComparison::HasPriority.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationprioritycomparison-haspriority)

 

Per avviare G prima che sia trascorso il ritardo accettabile più lungo, il gestore dell'animazione deve eseguire le operazioni seguenti:

-   Taglia F
-   Annulla E

Quando E viene annullato, D e F vengono scoperti e vengono ripristinati i contorni originali:

![Illustrazione che mostra i contorni originali](images/existingschedule1bwithlines.png)

Il gestore dell'animazione non deve annullare o tagliare C per pianificare prima che sia trascorso il ritardo accettabile più lungo, quindi la riunione di C e G determina quando inizia G.

![Figura che mostra che f viene tagliato per consentire a c e g di soddisfare](images/schedule1withgwithlines.png)

Dopo che G è stato pianificato correttamente, è possibile determinare la durata delle transizioni e il resto della struttura è quindi noto. Tuttavia, la struttura può cambiare se un altro storyboard viene successivamente rimosso dalla pianificazione.

Come secondo esempio, si consideri uno scenario simile a quello precedente, ma con un ritardo accettabile più lungo più breve specificato per G.

![figura che illustra lo scenario precedente, ma con un ritardo accettabile più lungo più breve per g](images/existingschedule2withlines.png)

In questo caso, vengono eseguite le azioni seguenti:

-   Taglia F
-   Annulla E
-   Annullare C

Inoltre, il gestore dell'animazione deve comprimere D in base alla quantità indicata per consentire a G di iniziare dopo il ritardo accettabile più lungo e non in un secondo momento.

![Figura che mostra dove deve essere compresso d per consentire a g di iniziare con il ritardo accettabile più lungo](images/trimmedandcancelledwithlines.png)

Per mantenere la relativa tempistica, vengono compressi anche A, B e F.

![Illustrazione che mostra a, b, d e f compressi](images/schedule2withgwithlines.png)

Tuttavia, gli storyboard in variabili non correlate (non visualizzate) non vengono compressi.

Ancora una volta, la struttura di G è ora nota ed è diversa dal risultato nel primo scenario perché le variabili hanno valori diversi all'inizio di G.

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

 

