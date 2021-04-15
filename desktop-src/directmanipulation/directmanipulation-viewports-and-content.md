---
description: La manipolazione diretta USA viewport, contenuto e contatti per descrivere gli elementi interattivi dell'interfaccia utente.
ms.assetid: 1564F6F2-844F-4392-9EB5-AA46059D514C
title: Viewport e contenuto
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9cda367067ea860ce6a42a16e81d38393937276a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104570535"
---
# <a name="viewports-and-content"></a>Viewport e contenuto

La [manipolazione diretta](direct-manipulation-portal.md) USA *viewport*, *contenuto* e *contatti* per descrivere gli elementi interattivi dell'interfaccia utente.

- [Configurazione di un viewport](#configuring-a-viewport)
- [Punti di allineamento e limiti](#snap-points-and-boundaries)
- [Scenari di offset e offset del punto di allineamento](#snap-point-offset-and-rtl-scenarios)
- [Comportamenti](#behaviors)
- [Sistema di coordinate](#coordinate-system)
- [Trasformazioni](#transforms)
- [Stato del viewport](#viewport-state)
- [Argomenti correlati](#related-topics)

Un *viewport* è un'area all'interno di una finestra che può ricevere ed elaborare l'input dalle interazioni degli utenti. Il viewport rappresenta l'area del contenuto che può essere visualizzata dall'utente finale in un determinato momento (detta anche clip di contenuto). Il viewport presenta diverse funzioni:

- Gestisce lo stato di interazione (ad esempio, quando il contenuto è pronto per essere modificato, quando il contenuto è in fase di manipolazione, quando il contenuto è in un'animazione di inerzia) ed esegue il mapping dell'input alle trasformazioni di output.
- Contiene contenuto che si sposta in risposta all'interazione dell'utente. Potrebbe trattarsi di un elemento div HTML (scorrimento), di un elenco di Pan (la schermata Start di Windows 8) o del menu a comparsa per un controllo SELECT.

Un viewport viene creato chiamando [**CreateViewport**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport). È possibile creare più viewport in un'unica finestra per offrire un'esperienza di interfaccia utente avanzata.

Il *contenuto* rappresenta l'elemento che viene trasformato in risposta a un'interazione. In altre parole, il contenuto viene spostato o ridimensionato come l'utente pentole o i pizzicotti. Esistono due tipi di contenuto:

- Il *contenuto primario* è il singolo elemento intrinseco all'interno di un viewport che risponde alle modifiche e all'inerzia di input. Il contenuto primario viene creato allo stesso tempo del viewport e non può essere aggiunto o rimosso da un viewport. È possibile personalizzare il comportamento del contenuto primario usando i punti di blocco (descritto più avanti).
- Il *contenuto secondario* si sposta rispetto al movimento del contenuto primario. Il contenuto secondario viene creato separatamente dal viewport e può essere aggiunto o rimosso da un viewport. Tutte le trasformazioni di contenuto secondario vengono calcolate in base alla trasformazione del contenuto primario. È possibile applicare regole specifiche per modificare il modo in cui la trasformazione viene calcolata in base allo scopo designato dell'elemento, identificato dal relativo CLSID durante la creazione.

In questo diagramma che illustra prima e dopo una panoramica, è stato usato un singolo contatto per eseguire il panning del contenuto primario. Anche se l'utente non interagisce direttamente con l'indicatore di panning (contenuto secondario), il contenuto secondario viene spostato mentre viene stroncato il contenuto primario. In questo modo vengono visualizzati i segnali visivi per quanto l'utente ha completato la panoramica.

![diagramma che mostra prima/dopo una panoramica](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>Configurazione di un viewport

Dopo aver creato il viewport. configurare il comportamento mediante una *configurazione di interazione*. La configurazione di interazione specifica quali modifiche, come la panoramica, sono supportate.

Il *panning* modifica la posizione del contenuto lungo l'asse orizzontale o verticale o entrambi come un tegame utente. Quando si configura la traduzione in entrambi gli assi, il contenuto viene spostato liberamente in qualsiasi direzione.

Per vincolare il movimento del contenuto, configurare le *guide*, in genere sull'asse orizzontale e verticale. Se l'interazione di un utente è principalmente lungo un singolo asse (rappresentato dalle aree blu nel diagramma successivo), il panning viene sottoposto a *ringhiera* e il contenuto si sposta solo lungo l'asse rotante. Se l'utente ha eseguito il panning ed è attualmente recintato ed esegue una seconda padella mentre il contenuto è in inerzia, il nuovo PAN continua a essere barrato.

![diagramma che mostra il contenuto all'interno di un riquadro di visualizzazione in una padella a barre](images/dm-art-3.png)

Esempio: un viewport è configurato per la panoramica orizzontale e verticale. Nel primo frame il contatto viene disattivato. Nel secondo viene avviato un pan verticale e il contatto viene bloccato sulla barra verticale. Infine, una volta che il Pan è recintato, per spostare il contenuto viene usato solo il componente verticale di un panning diagonale.

Se l'utente si sposta in diagonale in modo che non si trovino nelle aree di rilevamento delle guide (le aree bianche), il Pan viene sottoposto a *ringhiera* e il contenuto verrà spostato liberamente in entrambi gli assi.

![diagramma che mostra il contenuto che si sposta in un Pan non recintato](images/dm-art-4.png)

Lo *Zoom* cambia il fattore di scala del contenuto come un pizzico o un'estensione dell'utente. Il punto intorno al quale il contenuto viene ridimensionato (denominato centro zoom) si trova al centro dei contatti. Se è stato impostato l'allineamento orizzontale o verticale, il centro zoom viene modificato per mantenere l'allineamento.

![diagramma che mostra lo zoom del contenuto con un allineamento specificato](images/dm-art-5.png)

È possibile eseguire l'override di questo comportamento specificando il centro di sblocco, che imposta il centro zoom al centro dei contatti.

![diagramma che mostra lo zoom del contenuto con lo zoom Center sbloccato](images/dm-art-6.png)

L' *inerzia* è la decelerazione graduale di una manipolazione, sia panoramica che zoom, dopo che tutti i contatti sono stati rimossi (in caso di tocco) o dopo l'input da tastiera/mouse (ad esempio, facendo clic su una barra di scorrimento o premendo i tasti di direzione). Quando un utente modifica il contenuto, la manipolazione non viene arrestata immediatamente dopo la revoca del contatto. Il contenuto continua invece con la direzione e la velocità correnti, rallentando gradualmente fino a fermarsi.

## <a name="snap-points-and-boundaries"></a>Punti di allineamento e limiti

Un'animazione di inerzia viene eseguita al termine della manipolazione in seguito alla chiusura di un dito dallo schermo (in caso di tocco) o a seguito di un'azione di tastiera/mouse (ad esempio, tasti di direzione, PGSU/giù, scorrimento della rotellina del mouse e così via).

Esistono due tipi di informazioni che definiscono l'animazione di inerzia:

- Il punto rimanente dell'animazione, ovvero la posizione finale finale del particolare componente di trasformazione.
- La durata, la curva e la velocità dell'animazione sono determinate dal tipo di punto Rest.

L'animazione di inerzia è interessata da punti di allineamento e limiti. I limiti specificano i punti Rest massimi e minimi per il contenuto. Se il contenuto raggiunge un limite durante l'inerzia, viene applicata un'animazione limite. I punti di blocco vengono definiti nel contenuto primario per modificare il punto REST e modificare la curva di animazione dell'inerzia stessa.

I punti di blocco vengono definiti con [**SetSnapInterval**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) quando il contenuto è regolarmente spaziato o con [**SetSnapPoints**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) quando il contenuto è distanziato in modo non uniforme. Di seguito è riportato un esempio di punti di allineamento:

![diagramma che illustra come i punti di blocco impostati nel contenuto influiscono sulla panoramica](images/dm-snappoint-states-3.png)

Nel diagramma è presente una porzione di contenuto con una serie di blocchi di sottocontenuto, ovvero elementi di notizie in un'app di tipo lettore di notizie o elementi in una visualizzazione griglia. Lo scopo è quello di bloccare il bordo sinistro di un elemento sul bordo sinistro del viewport dopo che l'inerzia è terminata.

Sono disponibili due gruppi di tipi di punti di allineamento:

- *Facoltativo e obbligatorio*: un punto di blocco facoltativo blocca l'animazione dell'inerzia solo se il punto REST di inerzia si trova vicino al punto di allineamento. Un punto di blocco obbligatorio blocca sempre l'animazione di inerzia a un punto di allineamento specificato.
- *Singolo e multiplo*: un tipo di punto di blocco multiplo consente al contenuto di spostarsi oltre molti punti di blocco prima di passare a un altro punto di aggancio vicino al punto Rest naturale. Un tipo di punto di blocco singolo sceglie il punto di blocco successivo più vicino come punto rimanente per l'animazione dell'inerzia.

Il diagramma seguente illustra come i tipi di punto di blocco modifichino la posizione Rest dell'animazione di inerzia.

![diagramma che illustra la modalità di interazione tra inerzia e punti di allineamento](images/dm-snappoint-states-1.png)

In questo diagramma, il punto iniziale di inerzia è contrassegnato come ' Start ' e la posizione finale dell'inerzia naturale in assenza di punti di blocco come ' end '. Le linee verticali contrassegnano i vari punti di aggancio. In questa tabella viene descritto il modo in cui ogni tipo di punto di allineamento influirà sulla posizione finale dell'animazione.

| Tipo di punto         | Descrizione                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| Singolo obbligatorio   | Viene scelto il punto di aggancio P1 perché è il primo punto di blocco nella direzione di inerzia     |
| Multiplo obbligatorio | Viene scelto il punto di aggancio P2 perché è più vicino al punto finale nella direzione di inerzia |
| Singolo facoltativo    | Viene scelto il punto di aggancio P1 perché si tratta del primo punto di blocco rilevato durante l'inerzia      |
| Multiplo facoltativo  | Viene scelto il punto di aggancio P2 perché si trova vicino al punto finale naturale                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>Scenari di offset e offset del punto di allineamento

![diagramma che mostra l'uso del punto di aggancio RTL](images/dm-snappoint-states-2.png)

Applicare l'offset e il sistema di coordinate del punto di blocco usando l'API [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) , che compensa tutti i punti di blocco o gli intervalli di snap usando il sistema di coordinate/offset specificato.

Il sistema di coordinate è molto utile negli scenari di RTL, in cui si desidera descrivere i punti di aggancio dal bordo sinistro del contenuto nella direzione inversa. Nel diagramma precedente, [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) viene usato con il flag **DIRECTMANIPULATION \_ Motion \_ TranslateX** e **DIRECTMANIPULATION \_ coordinata con \_ mirroring** , che compensa automaticamente i punti di aggancio dal bordo sinistro del contenuto e li fornisce in ordine da destra a sinistra: S1 è in 0px, S2 si trova in 50px e così via. Tutti gli offset impostati con **SetSnapCoordinate** verranno ulteriormente spostati automaticamente da questo bordo sinistro del contenuto, incluso il fattore di scala corretto.

Si userà quasi sempre [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) con il set di parametri *Origin* per evitare l'impostazione di punti di blocco all'esterno dell'area di contenuto.

Se, ad esempio, il viewport è 200x200 e il contenuto è 1000x200 e l'interfaccia è di RTL, il viewport avrà il bordo sinistro a x = 800 quando il viewport viene presentato per la prima volta. Chiamare [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) con `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` per specificare che i punti di blocco devono essere calcolati dall'ordine da destra a sinistra a partire dal bordo destro del contenuto.

## <a name="behaviors"></a>Comportamenti

Un *comportamento* è un oggetto che può essere collegato a un viewport per modificare il modo in cui la [manipolazione diretta](direct-manipulation-portal.md) gestisce la trasformazione di output del contenuto primario o secondario di un viewport. Un oggetto Behavior può influire su uno o più aspetti di una manipolazione, ad esempio come viene elaborato l'input o come viene applicata l'animazione di inerzia. Ad esempio, un comportamento di scorrimento automatico influiscono sull'animazione di inerzia eseguendo un'animazione a scorrimento verso un'estremità del contenuto primario. Un comportamento di configurazione tra le diapositive influiscono sull'elaborazione dell'input di manipolazione diretta che rileva quando viene eseguita un'azione tra diapositive.

Un oggetto Behavior viene creato chiamando [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior), aggiunto a un viewport e quindi il relativo comportamento viene configurato in modo asincrono. La rimozione del comportamento dal viewport ne rimuove gli effetti.

## <a name="coordinate-system"></a>Sistema di coordinate

Esistono tre sistemi di coordinate principali utilizzati dalla [manipolazione diretta](direct-manipulation-portal.md):

- Sistema di coordinate client: descrive il rettangolo della finestra client. Le unità sono in pixel.
- Sistema di coordinate del viewport: descrive il rettangolo di un'area all'interno del client in grado di elaborare l'input. Le unità sono definite dall'applicazione (tramite [**SetViewportRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)).
- Sistema di coordinate del contenuto: descrive il rettangolo o le dimensioni del contenuto primario. Le unità sono definite dall'applicazione (tramite [**SetContentRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)).

Per tutti e tre i sistemi, le coordinate sono definite in relazione alla rispettiva origine superiore sinistra e sono un aumento positivo a destra e in basso. Questi sistemi di coordinate sono illustrati nel diagramma seguente. Solo la sezione del contenuto all'interno del rettangolo Viewport può essere visualizzata o modificata dall'utente finale.

![diagramma che illustra il modo in cui le coordinate di contenuto, client e Viewport interagiscono](images/dm-art-7.png)

## <a name="transforms"></a>Trasformazioni

La [manipolazione diretta](direct-manipulation-portal.md) mantiene diverse trasformazioni che contribuiscono all'output generale visualizzato.

- *Trasformazione del contenuto* : la trasformazione iniziale calcolata in base a una [manipolazione diretta](direct-manipulation-portal.md) basata su una manipolazione o un'inerzia. Acquisisce gli effetti dei punti di blocco, della ringhiera, della overpan predefinita (manipolazione), delle animazioni predefinite di overbounce (inerzia) e ZoomToRect.
- *Trasformazione output* : la trasformazione visiva o di output finale. Si tratta della combinazione del contenuto e delle trasformazioni di sincronizzazione.
- *Sincronizza trasformazione* : calcolata quando si chiama [**SyncContentTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform). Consente alla [manipolazione diretta](direct-manipulation-portal.md) di applicare una nuova trasformazione del contenuto fornita dall'applicazione, mantenendo al tempo stesso la trasformazione di output esistente.
- *Visualizzazione della trasformazione* : applicata dall'applicazione nell'ambito della post-elaborazione. Per ulteriori informazioni, vedere [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform) .

Poiché la trasformazione di output è progettata per compensare visivamente una superficie sullo schermo, la [manipolazione diretta](direct-manipulation-portal.md) esegue l'arrotondamento necessario sui componenti di trasformazione di output in modo che il rendering del testo e di altri contenuti venga sempre eseguito in un limite di pixel integrale. Il meccanismo di arrotondamento dipende da diversi fattori, tra cui la velocità del movimento e la presenza di Desktop remoto. Il meccanismo di arrotondamento per il contenuto secondario corrisponde a quello del contenuto primario, prendendo in considerazione la differenza nel movimento tra i due. I client di [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) non devono dipendere dal meccanismo di arrotondamento esatto della trasformazione di output, in quanto diversi fattori influiscono su di esso.

> [!Note]
>
> Ciò significa che i componenti di una trasformazione del contenuto potrebbero non essere integrali e possono contenere offset di pixel secondari. I client che usano la [manipolazione diretta](direct-manipulation-portal.md) sono invitati a usare [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) per calcolare la trasformazione visiva corretta da applicare al contenuto quando si usa la modalità di aggiornamento manuale. Quando si usa la modalità di aggiornamento automatico usando il compositor incorporato, la manipolazione diretta applica automaticamente questa trasformazione per conto del client. Questa trasformazione viene generata dalla manipolazione diretta per garantire risultati gradevoli visivamente quando si compone l'output visivo.

## <a name="viewport-state"></a>Stato del viewport

Quando l'input viene elaborato, il viewport gestisce lo stato interazione e il mapping dell'input alle trasformazioni di output. Verificare lo stato di interazione del viewport chiamando [**GetStatus**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus).

![diagramma che Mostra gli Stati di interazione directmanipulation](images/dm-states-diagram.png)

- Compilazione: il viewport viene creato e non è ancora in grado di elaborare l'input. Per elaborare l'input, chiamare [**IDirectManipulationViewport:: Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable). Se l' **Abilitazione** non viene chiamata, il viewport passa allo stato disabilitato.

    > [!Note]  
    > Si tratta dello stato iniziale dell'interazione.

- Abilitato: il viewport è pronto per l'elaborazione dell'input. Quando un contatto viene disattivato (viene chiamato il metodo [**secontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) ) e viene rilevata una manipolazione, il viewport passa a in esecuzione.

- Running: il viewport sta attualmente elaborando l'input e aggiornando il contenuto. Quando il contatto viene sollevato, il viewport passa a inerzia, se configurato.

- Inerzia: il contenuto viene spostato in un'animazione di inerzia. Una volta completata l'inerzia, il viewport passerà a Ready. Se è stata impostata la disabilitazione automatica nel viewport, la transizione da inerzia a pronta e quindi a disabilitata.

- Ready: il viewport è pronto per l'elaborazione dell'input. Quando un contatto viene disattivato (viene chiamato il metodo [**secontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) ) e viene rilevata una manipolazione, il viewport passa a in esecuzione.

- Suspended: è possibile che il viewport venga sospeso quando il relativo input è stato innalzato a un elemento padre nella catena dei [**contatti**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) . Questo argomento viene illustrato più dettagliatamente in [più viewport: hit testing e Viewport Hierarchy](directmanipulation-multiple-vieports.md).

- Disabled: il viewport non elaborerà l'input o effettuerà i callback. Un viewport può essere disabilitato da vari stati chiamando [**IDirectManipulationViewport::D able**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable). Se nel viewport è stata impostata la disabilitazione automatica, la transizione automatica viene disabilitata dopo l'elaborazione di una manipolazione. Per riabilitare un viewport disabilitato, chiamare [**IDirectManipulationViewport:: Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable).

## <a name="related-topics"></a>Argomenti correlati

[Più viewport: hit testing e gerarchia viewport](directmanipulation-multiple-vieports.md), [**ActivateConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration), [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform), [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
