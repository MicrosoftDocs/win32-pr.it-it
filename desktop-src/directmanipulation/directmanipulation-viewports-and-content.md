---
description: La manipolazione diretta usa viewport, contenuti e contatti per descrivere gli elementi interattivi dell'interfaccia utente.
ms.assetid: 1564F6F2-844F-4392-9EB5-AA46059D514C
title: Viewport e contenuto
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a103df916e5880380064250d05806169ff4187e6a8be0b22d2dd72d92343f38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787126"
---
# <a name="viewports-and-content"></a>Viewport e contenuto

[La manipolazione diretta](direct-manipulation-portal.md) usa *viewport,* *contenuti* e *contatti* per descrivere gli elementi interattivi dell'interfaccia utente.

- [Configurazione di un viewport](#configuring-a-viewport)
- [Punti di ancoraggio e limiti](#snap-points-and-boundaries)
- [Offset del punto di ancoraggio e scenari RTL](#snap-point-offset-and-rtl-scenarios)
- [Comportamenti](#behaviors)
- [Sistema di coordinate](#coordinate-system)
- [Trasformazioni](#transforms)
- [Stato del viewport](#viewport-state)
- [Argomenti correlati](#related-topics)

Un *viewport è un'area* all'interno di una finestra che può ricevere ed elaborare l'input dalle interazioni dell'utente. Il viewport rappresenta l'area del contenuto che può essere vista dall'utente finale in un determinato momento (denominata anche clip del contenuto). Il viewport ha diverse funzioni:

- Gestisce lo stato di interazione (ad esempio, quando il contenuto è pronto per essere modificato, quando il contenuto è in fase di manipolazione, quando il contenuto è in un'animazione di inerzia) ed esegue il mapping dell'input alle trasformazioni di output.
- Contiene contenuto che si sposta in risposta all'interazione dell'utente. Può trattarsi di un elemento DIV HTML (scorrimento), di un elenco pan-able (Windows 8 schermata Start) o del menu a comparsa per un controllo select.

Un viewport viene creato chiamando [**CreateViewport**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport). È possibile creare più viewport in un'unica finestra per produrre un'esperienza di interfaccia utente ottimale.

*Il* contenuto rappresenta l'elemento che viene trasformato in risposta a un'interazione. In altre parole, il contenuto è ciò che si sposta o ridimensiona quando l'utente fa la panoramica o avvicina le dita. Esistono due tipi di contenuto:

- *Il contenuto primario* è il singolo elemento intrinseco all'interno di un viewport che risponde alle modifiche di input e all'inerzia. Il contenuto primario viene creato contemporaneamente al viewport e non può essere aggiunto o rimosso da un viewport. È possibile personalizzare il comportamento del contenuto primario usando punti di allineamento (descritti più avanti).
- *Il contenuto secondario* viene spostato rispetto al movimento del contenuto primario. Il contenuto secondario viene creato separatamente dal viewport e può essere aggiunto o rimosso da un viewport. Tutte le trasformazioni di contenuto secondario vengono calcolate in base alla trasformazione del contenuto primario. È possibile applicare regole specifiche per modificare il modo in cui la trasformazione viene calcolata in base allo scopo previsto dell'elemento, identificato dal RELATIVO CLSID durante la creazione.

In questo diagramma che mostra prima e dopo una panoramica, è stato usato un singolo contatto per eseguire la panoramica del contenuto primario. Anche se l'utente non interagisce direttamente con l'indicatore di panoramica (contenuto secondario), il contenuto secondario si sposta quando viene panoramica il contenuto primario. In questo modo vengono forniti segnali visivi per l'estensione della panoramica da parte dell'utente.

![diagramma che mostra prima/dopo una panoramica](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>Configurazione di un viewport

Dopo aver creato il viewport. configurare il comportamento usando una configurazione *di interazione*. La configurazione dell'interazione specifica quali modifiche, ad esempio la panoramica, sono supportate.

*La panoramica* modifica la posizione del contenuto lungo l'asse orizzontale o verticale o entrambi durante la panoramica dell'utente. Quando si configura la traduzione su entrambi gli assi, il contenuto si sposta liberamente in qualsiasi direzione.

Per vincolare il movimento del contenuto, configurare *le guide*, in genere sull'asse orizzontale e verticale. Se l'interazione di un utente si trova principalmente lungo un singolo asse (rappresentato dalle aree blu nel diagramma successivo), la panoramica diventa in ringhiera e il contenuto si sposta solo lungo l'asse in ringhiera.  Se l'utente ha eseguito la panoramica ed è attualmente in ringhiera ed esegue una seconda panoramica mentre il contenuto è in inerzia, la nuova panoramica continua a essere in ringhiera.

![diagramma che mostra il contenuto all'interno di un viewport in una panoramica con ringhiera](images/dm-art-3.png)

Esempio: un viewport è configurato per la panoramica orizzontale e verticale. Nel primo frame, il contatto scende. Nel secondo viene avviata una panoramica verticale e il contatto viene bloccato sulla guida verticale. Infine, una volta che la panoramica è in ringhiera, per spostare il contenuto viene usato solo il componente verticale di una panoramica diagonale.

Se l'utente fa una panoramica diagonale in modo che non si trova nelle  aree di rilevamento delle guide (le aree di colore bianco), la panoramica viene scollegata e il contenuto si sposterà liberamente in entrambi gli assi.

![Diagramma che mostra il contenuto in movimento in una panoramica non srotolata](images/dm-art-4.png)

*Lo zoom* modifica il fattore di scala del contenuto quando un utente avvicina le dita o si estende. Il punto intorno al quale viene ridimensionato il contenuto (chiamato centro dello zoom) si trova al centro dei contatti. Se è stato impostato l'allineamento orizzontale o verticale, il centro dello zoom cambia per mantenere l'allineamento.

![Diagramma che mostra lo zoom del contenuto con un allineamento specificato](images/dm-art-5.png)

È possibile eseguire l'override di questo comportamento specificando unlock center, che imposta il centro dello zoom al centro dei contatti.

![Diagramma che mostra lo zoom del contenuto con il centro zoom sbloccato](images/dm-art-6.png)

*L'inerzia* è la decelerazione graduale di una manipolazione, sia di panoramica che di zoom, dopo che tutti i contatti sono stati sollevati (nel caso del tocco) o dopo l'input da tastiera/mouse (ad esempio facendo clic su una barra di scorrimento o premendo i tasti di direzione). Quando un utente modifica il contenuto, la manipolazione non si arresta immediatamente dopo che il contatto è stato sollevato. Il contenuto continua invece nella direzione e nella velocità correnti, rallentando gradualmente fino a arrestarsi.

## <a name="snap-points-and-boundaries"></a>Punti di ancoraggio e limiti

Un'animazione di inerzia viene eseguita dopo la fine della manipolazione in seguito al sollevamento di un dito sullo schermo (nel caso del tocco) o a seguito di un'azione da tastiera/mouse (ad esempio tasti di direzione, pagina su/giù, scorrimento della rotellina del mouse e così via).

Esistono due informazioni che definiscono l'animazione di inerzia:

- Il punto rimanente dell'animazione, la posizione finale del componente di trasformazione specifico.
- Durata, curva e velocità dell'animazione: sono determinate dal tipo di punto di riposo.

L'animazione di inerzia è interessata da punti di ancoraggio e limiti. I limiti specificano i punti di riposo massimo e minimo per il contenuto. Se il contenuto raggiunge un limite durante l'inerzia, verrà applicata un'animazione limite. I punti di ancoraggio vengono definiti nel contenuto primario per modificare il punto di riposo e modificare la curva di animazione dell'inerzia stessa.

I punti di ancoraggio vengono definiti con [**SetSnapInterval**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) quando il contenuto viene disagiato regolarmente o con [**SetSnapPoints**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) quando il contenuto è disagiva in modo non uniforme. Ecco un esempio di punti di ancoraggio:

![Diagramma che illustra l'effetto della panoramica dei punti di allineamento impostati nel contenuto](images/dm-snappoint-states-3.png)

Nel diagramma è presente una parte di contenuto con una serie di blocchi di contenuto secondario: elementi di notizie in un'app di tipo lettore di notizie o elementi in una visualizzazione Griglia. Lo scopo è quello di allineare il bordo sinistro di un elemento sul bordo sinistro del viewport al termine dell'inerzia.

Esistono due gruppi di tipi di punti di ancoraggio:

- *Facoltativo o Obbligatorio:* un punto di snap facoltativo blocca l'animazione di inerzia solo se il punto di inerzia è vicino al punto di ancoraggio. Un punto di snap obbligatorio blocca sempre l'animazione di inerzia su un punto di snap specificato.
- *Singolo o Multiplo:* un tipo di punto di ancoraggio multiplo consente al contenuto di spostarsi oltre molti punti di snap prima di passare a un punto di ancoraggio in un punto di ancoraggio vicino al punto di riposo naturale. Un singolo tipo di punto di ancoraggio sceglie il punto di snap più vicino successivo come punto di riposo per l'animazione di inerzia.

Il diagramma successivo illustra come i tipi di punti di ancoraggio modificano la posizione rimanente dell'animazione di inerzia.

![Diagramma che illustra l'interazione tra inerzia e punti di ancoraggio](images/dm-snappoint-states-1.png)

In questo diagramma, il punto iniziale di inerzia è etichettato come "Start" e la posizione finale dell'inerzia naturale in assenza di punti di ancoraggio è "End". Le linee verticali contrassegnano i vari punti di ancoraggio. Questa tabella descrive in che modo ogni tipo di punto di ancoraggio influirà sulla posizione finale dell'animazione.

| Tipo di punto         | Descrizione                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| Obbligatorio singolo   | Il punto di ancoraggio P1 viene scelto perché è il primo punto di snap nella direzione dell'inerzia     |
| Multiplo obbligatorio | Viene scelto il punto di ancoraggio P2 perché è più vicino al punto finale nella direzione dell'inerzia |
| Singolo facoltativo    | Il punto di ancoraggio P1 viene scelto perché è il primo punto di snap rilevato durante l'inerzia      |
| Multiplo facoltativo  | Il punto di ancoraggio P2 viene scelto perché è vicino al punto finale naturale                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>Offset del punto di ancoraggio e scenari RTL

![Diagramma che mostra l'uso del punto di snap rtl](images/dm-snappoint-states-2.png)

Si applicano l'offset del punto di ancoraggio e il sistema di coordinate usando l'API [**SetSnapCoordinate,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) che esegue l'offset di tutti i punti di snap o gli intervalli di snap usando il sistema di offset/coordinate specificato.

Il sistema di coordinate è molto utile negli scenari RTL, in cui si vogliono descrivere i punti di ancoraggio dal bordo sinistro del contenuto nella direzione inversa. Nel diagramma [**precedente, SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) viene usato con il flag **DIRECTMANIPULATION \_ MOTION \_ TRANSLATEX** e **DIRECTMANIPULATION \_ COORDINATE \_ MIRRORED,** che esegue automaticamente l'offset dei punti di allineamento dal bordo sinistro del contenuto e li fornisce in ordine da destra a sinistra: S1 è a 0px, S2 è a 50px (e così via). Qualsiasi offset impostato usando **SetSnapCoordinate** verrà ulteriormente compensato da questo bordo sinistro del contenuto automaticamente, incluso il fattore di scala corretto.

Si userà quasi sempre [**SetSnapCoordinate con il**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) parametro *origin* impostato per evitare di impostare punti di ancoraggio all'esterno dell'area del contenuto.

Ad esempio, se il viewport è 200x200 e il contenuto è 1000x200 e l'interfaccia è RTL, il riquadro di visualizzazione avrà il bordo sinistro x=800 quando il viewport viene presentato per la prima volta. Chiamare [**SetSnapCoordinate con**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) per specificare che i punti di ancoraggio devono essere calcolati dall'ordine da destra a sinistra a partire dal bordo `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` DESTRO del contenuto.

## <a name="behaviors"></a>Comportamenti

Un *comportamento* è un oggetto che può essere associato a [](direct-manipulation-portal.md) un viewport per modificare il modo in cui la manipolazione diretta gestisce la trasformazione di output del contenuto primario o secondario di un viewport. Un oggetto comportamento può influire su uno o più aspetti di una manipolazione, ad esempio la modalità di elaborazione dell'input o l'applicazione dell'animazione di inerzia. Ad esempio, un comportamento di scorrimento automatico influisce sull'animazione di inerzia eseguendo un'animazione di scorrimento verso un'estremità del contenuto primario. Un comportamento di configurazione a scorrimento incrociato influisce sull'elaborazione dell'input di manipolazione diretta che rileva quando viene eseguita un'azione di scorrimento incrociato.

Un oggetto comportamento viene creato chiamando [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior), aggiunto a un viewport e quindi il relativo comportamento viene configurato in modo asincrono. Rimuovendo il comportamento dal viewport, ne vengono rimossi gli effetti.

## <a name="coordinate-system"></a>Sistema di coordinate

Esistono tre sistemi di coordinate principali utilizzati dalla [manipolazione diretta:](direct-manipulation-portal.md)

- Sistema di coordinate client: descrive il rettangolo della finestra client. Le unità sono espresse in pixel.
- Sistema di coordinate del viewport: descrive il rettangolo di un'area all'interno del client in grado di elaborare l'input. Le unità sono definite dall'applicazione [**(tramite SetViewportRect).**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)
- Sistema di coordinate del contenuto: descrive il rettangolo o le dimensioni del contenuto primario. Le unità sono definite dall'applicazione [**(tramite SetContentRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)).

Per tutti e tre i sistemi, le coordinate vengono definite in relazione alla rispettiva origine in alto a sinistra e sono positive che aumentano verso destra e verso il basso. Questi sistemi di coordinate sono illustrati nel diagramma seguente. Solo la sezione del contenuto all'interno del rettangolo di visualizzazione può essere vista o manipolata dall'utente finale.

![Diagramma che illustra l'interazione tra le coordinate di contenuto, client e riquadro di visualizzazione](images/dm-art-7.png)

## <a name="transforms"></a>Trasformazioni

[La manipolazione](direct-manipulation-portal.md) diretta mantiene diverse trasformazioni che contribuiscono all'output visualizzato complessivo.

- *Trasformazione del* contenuto: trasformazione iniziale calcolata dalla [manipolazione](direct-manipulation-portal.md) diretta in base a una manipolazione o a un'inerzia. Acquisisce gli effetti delle animazioni punti di ancoraggio, guida, overpan predefinito (manipolazione), overbounce predefinito (inerzia) e ZoomToRect.
- *Trasformazione di output:* l'oggetto visivo o la trasformazione di output finale. È la combinazione sia del contenuto che delle trasformazioni di sincronizzazione.
- *Trasformazione di sincronizzazione:* calcolata quando si chiama [**SyncContentTransform.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform) Consente alla [manipolazione diretta di](direct-manipulation-portal.md) applicare una nuova trasformazione del contenuto fornita dall'applicazione, mantenendo al tempo stesso la trasformazione di output esistente.
- *Trasformazione di* visualizzazione: applicata dall'applicazione come parte della post-elaborazione. Per [**altri dettagli, vedere SyncDisplayTransform.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)

Poiché la trasformazione di output è progettata per eseguire l'offset visivo di una superficie sullo [schermo,](direct-manipulation-portal.md) la manipolazione diretta esegue l'arrotondamento necessario sui componenti di trasformazione di output in modo che il rendering o la composizione di testo e altri contenuti siano sempre eseguano il rendering o la composizione su un limite di pixel integrale. Il meccanismo di arrotondamento dipende da più fattori, tra cui la velocità del movimento e la presenza di Desktop remoto. Il meccanismo di arrotondamento per il contenuto secondario corrisponde a quello del contenuto primario, tenendo conto della differenza nel movimento tra i due. I client [**di GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) non devono dipendere dall'esatto meccanismo di arrotondamento della trasformazione di output, perché vari fattori influiscono su di essa.

> [!Note]
>
> Ciò significa che i componenti di una trasformazione del contenuto potrebbero non essere integrali e contenere offset di subpixe. I client [che usano la manipolazione](direct-manipulation-portal.md) diretta sono invitati a usare [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) per calcolare la trasformazione visiva corretta da applicare al contenuto quando si usa la modalità di aggiornamento manuale. Quando si usa la modalità di aggiornamento automatico usando il compositor incorporato, la manipolazione diretta applica automaticamente questa trasformazione per conto del client. Questa trasformazione viene generata dalla manipolazione diretta per garantire risultati visivamente gradevoli durante la composizione dell'output visivo.

## <a name="viewport-state"></a>Stato del viewport

Durante l'elaborazione dell'input, il viewport gestisce lo stato di interazione e il mapping dell'input alle trasformazioni di output. Controllare lo stato di interazione del viewport chiamando [**GetStatus**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus).

![Diagramma che mostra gli stati di interazione directmanipulation](images/dm-states-diagram.png)

- Compilazione: il viewport è in fase di creazione e non è ancora in grado di elaborare l'input. Per elaborare l'input, chiamare [**IDirectManipulationViewport::Enable.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable) Se **l'opzione** Abilita non viene chiamata, il viewport passa allo stato Disabilitato.

    > [!Note]  
    > Questo è lo stato iniziale dell'interazione.

- Abilitato: il viewport è pronto per elaborare l'input. Quando un contatto non è disponibile (viene chiamato [**SetContact)**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) e viene rilevata una manipolazione, il viewport passa a In esecuzione.

- In esecuzione: il viewport sta attualmente elaborando l'input e aggiornando il contenuto. Quando il contatto viene elevato, il viewport passa a Inerzia, se configurato.

- Inerzia: il contenuto si sta spostando in un'animazione di inerzia. Al termine dell'inerzia, il viewport passa a Pronto. Se la disabilitazione automatica è stata impostata nel viewport, passa da Inerzia a Pronto e quindi a Disabilitato.

- Pronto: il viewport è pronto per elaborare l'input. Quando un contatto non è disponibile (viene chiamato [**SetContact)**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) e viene rilevata una manipolazione, il viewport passa a In esecuzione.

- Sospeso: il viewport può diventare Sospeso quando il relativo input è stato promosso a elemento padre nella [**catena SetContact.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) Questo argomento viene illustrato in modo più dettagliato in [Multiple viewports: hit testing and viewport hierarchy (Più viewport: hit testing e gerarchia del viewport).](directmanipulation-multiple-vieports.md)

- Disabilitato: il viewport non eelaborare l'input né effettuare callback. Un viewport può essere disabilitato da vari stati chiamando [**IDirectManipulationViewport::D isable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable). Se la disabilitazione automatica è stata impostata nel viewport, passa automaticamente a Disabilitato dopo l'elaborazione di una manipolazione. Per abilitare nuovamente un viewport disabilitato, chiamare [**IDirectManipulationViewport::Enable.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable)

## <a name="related-topics"></a>Argomenti correlati

[Più viewport: hit testing e gerarchia del viewport,](directmanipulation-multiple-vieports.md) [**ActivateConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration) [**GetOutputTransform,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
