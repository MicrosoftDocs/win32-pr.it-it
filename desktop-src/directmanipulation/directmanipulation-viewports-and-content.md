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

[La manipolazione diretta](direct-manipulation-portal.md) usa *viewport,* *contenuti e* *contatti* per descrivere gli elementi interattivi dell'interfaccia utente.

- [Configurazione di un viewport](#configuring-a-viewport)
- [Punti di ancoraggio e limiti](#snap-points-and-boundaries)
- [Offset del punto di ancoraggio e scenari RTL](#snap-point-offset-and-rtl-scenarios)
- [Comportamenti](#behaviors)
- [Sistema di coordinate](#coordinate-system)
- [Trasformazioni](#transforms)
- [Stato del viewport](#viewport-state)
- [Argomenti correlati](#related-topics)

Un *viewport è un'area* all'interno di una finestra che può ricevere ed elaborare l'input dalle interazioni dell'utente. Il viewport rappresenta l'area del contenuto che può essere visualizzato dall'utente finale in un determinato momento (chiamato anche clip di contenuto). Il viewport ha diverse funzioni:

- Gestisce lo stato di interazione (ad esempio, quando il contenuto è pronto per essere modificato, quando il contenuto è in fase di manipolazione, quando il contenuto è in un'animazione di inerzia) ed esegue il mapping dell'input alle trasformazioni di output.
- Contiene contenuto che si sposta in risposta all'interazione dell'utente. Può trattarsi di un elemento DIV HTML (scorrimento), di un elenco a scorrimento (Windows 8 schermata Start) o del menu a comparsa per un controllo di selezione.

Un viewport viene creato chiamando [**CreateViewport.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport) È possibile creare più viewport in un'unica finestra per produrre un'esperienza di interfaccia utente più ricca.

*Il* contenuto rappresenta l'elemento che viene trasformato in risposta a un'interazione. In altre parole, il contenuto è ciò che si sposta o ridimensiona mentre l'utente fa una panoramica o un avvicinamento delle dita. Esistono due tipi di contenuto:

- *Il contenuto principale* è il singolo elemento intrinseco all'interno di un viewport che risponde alle modifiche di input e all'inerzia. Il contenuto primario viene creato contemporaneamente al viewport e non può essere aggiunto o rimosso da un viewport. È possibile personalizzare il comportamento del contenuto primario usando i punti di ancoraggio (descritti più avanti).
- *Il contenuto secondario* si sposta in relazione al movimento del contenuto primario. Il contenuto secondario viene creato separatamente dal viewport e può essere aggiunto o rimosso da un viewport. Tutte le trasformazioni del contenuto secondario vengono calcolate in base alla trasformazione del contenuto primario. È possibile applicare regole specifiche per modificare la modalità di calcolo della trasformazione in base allo scopo previsto dell'elemento, identificato dal CLSID durante la creazione.

In questo diagramma che mostra prima e dopo una panoramica, è stato usato un singolo contatto per eseguire la panoramica del contenuto primario. Anche se l'utente non interagisce direttamente con l'indicatore di panoramica (contenuto secondario), il contenuto secondario si sposta mentre viene panoramica il contenuto primario. In questo modo vengono forniti segnali visivi per la distanza tra le panoramica dell'utente.

![diagramma che mostra prima/dopo una panoramica](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>Configurazione di un viewport

Dopo aver creato il viewport. configurarne il comportamento usando una *configurazione di interazione*. La configurazione dell'interazione specifica quali manipolazioni, ad esempio la panoramica, sono supportate.

*La panoramica* modifica la posizione del contenuto lungo l'asse orizzontale o verticale o entrambi durante la panoramica dell'utente. Quando si configura la traduzione su entrambi gli assi, il contenuto si sposta liberamente in qualsiasi direzione.

Per vincolare il movimento del contenuto, configurare *le guide*, in genere sia sull'asse orizzontale che su quello verticale. Se l'interazione di un utente si trova principalmente lungo un singolo asse (rappresentato dalle aree blu nel diagramma successivo), la panoramica diventa in *railed* e il contenuto si sposta solo lungo l'asse guidato. Se l'utente ha eseguito una panoramica ed è attualmente in binario ed esegue una seconda panoramica mentre il contenuto è in inerzia, la nuova panoramica continua a essere eseguita.

![diagramma che mostra il contenuto all'interno di un viewport in una panoramica con guide](images/dm-art-3.png)

Esempio: un riquadro di visualizzazione è configurato per la panoramica orizzontale e verticale. Nel primo fotogramma, il contatto scende in basso. Nel secondo viene avviata una panoramica verticale e il contatto è bloccato sulla guida verticale. Infine, una volta che la panoramica è in binario, per spostare il contenuto viene usato solo il componente verticale di una panoramica diagonale.

Se l'utente fa una panoramica diagonale in modo che non si trova nelle  aree di rilevamento delle guide (le aree bianchi), la panoramica non viene spostata e il contenuto si sposterà liberamente su entrambi gli assi.

![diagramma che mostra il contenuto che si sposta in una panoramica senza slittamento](images/dm-art-4.png)

*Lo zoom modifica* il fattore di scala del contenuto quando un utente avvicina le dita o si estende. Il punto intorno al quale viene ridimensionato il contenuto (denominato centro dello zoom) si trova al centro dei contatti. Se è stato impostato l'allineamento orizzontale o verticale, il centro dello zoom cambia per mantenere l'allineamento.

![Diagramma che mostra lo zoom del contenuto con un allineamento specificato](images/dm-art-5.png)

È possibile eseguire l'override di questo comportamento specificando il centro di sblocco, che imposta il centro dello zoom al centro dei contatti.

![Diagramma che mostra lo zoom del contenuto con il centro dello zoom sbloccato](images/dm-art-6.png)

*L'inerzia* è la decelerazione graduale di una manipolazione, sia di panoramica che di zoom, dopo che tutti i contatti sono stati sollevati (nel caso del tocco) o dopo l'input da tastiera/mouse (ad esempio facendo clic su una barra di scorrimento o premendo i tasti di direzione). Quando un utente modifica il contenuto, la manipolazione non si arresta immediatamente dopo che il contatto è stato elevato. Al contrario, il contenuto continua nella direzione e nella velocità correnti, rallentando gradualmente fino a un arresto.

## <a name="snap-points-and-boundaries"></a>Punti di ancoraggio e limiti

Un'animazione di inerzia viene eseguita dopo la fine della manipolazione in seguito all'elevazione di un dito sullo schermo (in caso di tocco) o a seguito di un'azione da tastiera/mouse (ad esempio tasti di direzione, pggi su/giù, scorrimento della rotellina del mouse e così via).

Esistono due informazioni che definiscono l'animazione dell'inerzia:

- Il resto dell'animazione, la posizione finale finale del componente di trasformazione specifico.
- Durata, curva e velocità dell'animazione, determinate dal tipo di punto rimanente.

L'animazione dell'inerzia è influenzata da punti di ancoraggio e limiti. I limiti specificano i punti di ripristino massimo e minimo per il contenuto. Se il contenuto raggiunge un limite durante l'inerzia, verrà applicata un'animazione limite. I punti di ancoraggio vengono definiti sul contenuto primario per modificare il punto rimanente e modificare la curva di animazione dell'inerzia stessa.

I punti di ancoraggio vengono definiti con [**SetSnapInterval**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) quando il contenuto viene disagito regolarmente o con [**SetSnapPoints**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) quando il contenuto è disartinciato in modo non uniforme. Ecco un esempio di punti di ancoraggio:

![Diagramma che illustra l'effetto dei punti di ancoraggio impostati nel contenuto sulla panoramica](images/dm-snappoint-states-3.png)

Nel diagramma è presente una parte di contenuto con una serie di blocchi di contenuto secondario: notizie in un'app di tipo lettore di notizie o elementi in una visualizzazione griglia. Lo scopo è quello di allineare il bordo sinistro di un elemento sul bordo sinistro del riquadro di visualizzazione al termine dell'inerzia.

Esistono due gruppi di tipi di punti di ancoraggio:

- *Facoltativo o obbligatorio:* un punto di ancoraggio facoltativo blocca l'animazione di inerzia solo se il punto di inerzia si trova vicino al punto di ancoraggio. Un punto di allineamento obbligatorio blocca sempre l'animazione dell'inerzia su un punto di allineamento specificato.
- *Singolo o Multiplo:* un tipo di punto di ancoraggio multiplo consente al contenuto di spostarsi oltre molti punti di ancoraggio prima di passare a un punto di ancoraggio in un punto di ancoraggio vicino al punto di ripristino naturale. Un singolo tipo di punto di ancoraggio sceglie il punto di allineamento più vicino successivo come punto rimanente per l'animazione di inerzia.

Il diagramma seguente illustra come i tipi di punti di ancoraggio modificano la posizione rimanente dell'animazione di inerzia.

![Diagramma che illustra l'interazione tra inerzia e punti di ancoraggio](images/dm-snappoint-states-1.png)

In questo diagramma, il punto iniziale di inerzia è etichettato come 'Start' e la posizione finale dell'inerzia naturale in assenza di punti di ancoraggio come 'Fine'. Le linee verticali contrassegnano i vari punti di ancoraggio. Questa tabella descrive in che modo ogni tipo di punto di ancoraggio influirà sulla posizione finale dell'animazione.

| Tipo di punto         | Descrizione                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| Obbligatorio singolo   | Il punto di ancoraggio P1 viene scelto perché è il primo punto di ancoraggio nella direzione dell'inerzia     |
| Multiplo obbligatorio | Il punto di ancoraggio P2 viene scelto perché è più vicino al punto finale nella direzione dell'inerzia |
| Facoltativo singolo    | Il punto di ancoraggio P1 viene scelto perché è il primo punto di ancoraggio rilevato durante l'inerzia      |
| Facoltativo multiplo  | Il punto di ancoraggio P2 viene scelto perché si trova vicino al punto finale naturale                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>Offset del punto di ancoraggio e scenari RTL

![diagramma che illustra l'uso del punto di ancoraggio rtl](images/dm-snappoint-states-2.png)

L'offset del punto di ancoraggio e il sistema di coordinate vengono applicati usando l'API [**SetSnapCoordinate,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) che esegue l'offset di tutti i punti di ancoraggio o gli intervalli di allineamento usando il sistema di offset/coordinate specificato.

Il sistema di coordinate è molto utile negli scenari RTL, in cui si vogliono descrivere i punti di allineamento dal bordo sinistro del contenuto nella direzione inversa. Nel diagramma [**precedente, SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) viene usato con il flag **DIRECTMANIPULATION \_ MOTION \_ TRANSLATEX** e **DIRECTMANIPULATION \_ COORDINATE \_ MIRRORED,** che esegue automaticamente l'offset dei punti di allineamento dal bordo sinistro del contenuto e li fornisce in ordine da destra a sinistra: S1 è a 0px, S2 è a 50px (e così via). Qualsiasi offset impostato con **SetSnapCoordinate** verrà ulteriormente offset da questo bordo sinistro del contenuto automaticamente, incluso il fattore di scala corretto.

Si userà quasi sempre [**SetSnapCoordinate con il**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) parametro *origin* impostato per evitare di impostare punti di ancoraggio all'esterno dell'area del contenuto.

Ad esempio, se il viewport è 200x200 e il contenuto è 1000x200 e l'interfaccia è RTL, il riquadro di visualizzazione avrà il bordo sinistro x=800 quando il viewport viene presentato per la prima volta. Chiamare [**SetSnapCoordinate con**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) per specificare che i punti di ancoraggio devono essere calcolati da destra a sinistra a partire dal bordo DESTRO `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` del contenuto.

## <a name="behaviors"></a>Comportamenti

Un *comportamento* è un oggetto che può essere collegato a [](direct-manipulation-portal.md) un viewport per modificare il modo in cui la manipolazione diretta gestisce la trasformazione di output del contenuto primario o secondario di un viewport. Un oggetto comportamento può influire su uno o più aspetti di una manipolazione, ad esempio la modalità di elaborazione dell'input o l'applicazione dell'animazione di inerzia. Ad esempio, un comportamento di scorrimento automatico influisce sull'animazione di inerzia eseguendo un'animazione di scorrimento verso un'estremità del contenuto primario. Un comportamento di configurazione a scorrimento incrociato influisce sull'elaborazione dell'input di manipolazione diretta che rileva quando viene eseguita un'azione di scorrimento incrociato.

Un oggetto comportamento viene creato chiamando [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior), aggiunto a un viewport e quindi il relativo comportamento viene configurato in modo asincrono. La rimozione del comportamento dal viewport ne rimuove gli effetti.

## <a name="coordinate-system"></a>Sistema di coordinate

Esistono tre sistemi di coordinate principali utilizzati dalla [manipolazione diretta:](direct-manipulation-portal.md)

- Sistema di coordinate client: descrive il rettangolo della finestra client. Le unità sono in pixel.
- Sistema di coordinate del viewport: descrive il rettangolo di un'area all'interno del client in grado di elaborare l'input. Le unità sono definite dall'applicazione (usando [**SetViewportRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)).
- Sistema di coordinate del contenuto: descrive il rettangolo o le dimensioni del contenuto primario. Le unità sono definite dall'applicazione (usando [**SetContentRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)).

Per tutti e tre i sistemi, le coordinate vengono definite in relazione alla rispettiva origine in alto a sinistra e sono positive che aumentano verso destra e verso il basso. Questi sistemi di coordinate sono illustrati nel diagramma successivo. Solo la sezione del contenuto all'interno del rettangolo del viewport può essere vista o manipolata dall'utente finale.

![diagramma che illustra l'interazione tra contenuto, client e coordinate del viewport](images/dm-art-7.png)

## <a name="transforms"></a>Trasformazioni

[La manipolazione](direct-manipulation-portal.md) diretta mantiene diverse trasformazioni che contribuiscono all'output visualizzato complessivo.

- *Trasformazione del* contenuto: trasformazione iniziale calcolata dalla [manipolazione](direct-manipulation-portal.md) diretta in base a una manipolazione o inerzia. Acquisisce gli effetti dei punti di allineamento, della ringhiera, dell'overpan predefinito (manipolazione), dell'overbounce predefinito (inerzia) e delle animazioni ZoomToRect.
- *Trasformazione di output:* l'oggetto visivo o la trasformazione di output finale. È la combinazione sia del contenuto che delle trasformazioni di sincronizzazione.
- *Trasformazione di sincronizzazione:* calcolata quando si chiama [**SyncContentTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform). Consente alla [manipolazione diretta di](direct-manipulation-portal.md) applicare una nuova trasformazione di contenuto fornita dall'applicazione mantenendo al tempo stesso la trasformazione di output esistente.
- *Trasformazione di* visualizzazione: applicata dall'applicazione come parte della post-elaborazione. Per [**altri dettagli, vedere SyncDisplayTransform.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)

Poiché la trasformazione di output ha lo scopo di eseguire l'offset visivo di una superficie sullo [schermo,](direct-manipulation-portal.md) La manipolazione diretta esegue l'arrotondamento necessario sui componenti di trasformazione di output in modo che il rendering o la composizione di testo e altro contenuto siano sempre in corrispondenza di un limite di pixel integrale. Il meccanismo di arrotondamento dipende da più fattori, tra cui la velocità del movimento e la presenza di Desktop remoto. Il meccanismo di arrotondamento per il contenuto secondario corrisponde a quello del contenuto primario, tenendo conto della differenza nel movimento tra i due. I client [**di GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) non devono dipendere dal meccanismo di arrotondamento esatto della trasformazione di output, in quanto diversi fattori influiscono sulla trasformazione.

> [!Note]
>
> Ciò significa che i componenti di una trasformazione del contenuto non possono essere integrali e possono contenere offset di sotto pixel. I client [che usano la manipolazione](direct-manipulation-portal.md) diretta sono invitati a usare [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) per calcolare la trasformazione visiva corretta da applicare al contenuto quando si usa la modalità di aggiornamento manuale. Quando si usa la modalità di aggiornamento automatico usando il compositor incorporato, Direct Manipulation applica automaticamente questa trasformazione per conto del client. Questa trasformazione viene generata dalla manipolazione diretta per garantire risultati visivamente gradevoli durante la composizione dell'output visivo.

## <a name="viewport-state"></a>Stato del viewport

Durante l'elaborazione dell'input, il viewport gestisce lo stato di interazione e il mapping dell'input alle trasformazioni di output. Controllare lo stato di interazione del viewport chiamando [**GetStatus**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus).

![Diagramma che mostra gli stati di interazione directmanipulation](images/dm-states-diagram.png)

- Compilazione: il viewport viene creato e non è ancora in grado di elaborare l'input. Per elaborare l'input, chiamare [**IDirectManipulationViewport::Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable). Se **l'opzione** Enable non viene chiamata, il viewport passa allo stato Disabled.

    > [!Note]  
    > Questo è lo stato iniziale dell'interazione.

- Abilitato: il viewport è pronto per elaborare l'input. Quando un contatto scende [**(viene chiamato SetContact)**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) e viene rilevata una manipolazione, il viewport passa a In esecuzione.

- In esecuzione: il viewport sta attualmente elaborando l'input e aggiornando il contenuto. Quando il contatto viene sollevato, il viewport passa a Inerzia, se configurato.

- Inerzia: il contenuto si sta spostando in un'animazione di inerzia. Al termine dell'inerzia, il viewport passa a Pronto. Se la disabilitazione automatica è stata impostata nel viewport, passa da Inerzia a Pronto e quindi a Disabilitato.

- Pronto: il viewport è pronto per elaborare l'input. Quando un contatto scende [**(viene chiamato SetContact)**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) e viene rilevata una manipolazione, il viewport passa a In esecuzione.

- Sospeso: il viewport può diventare Sospeso quando il relativo input è stato promosso a elemento padre nella [**catena SetContact.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) Questo argomento viene descritto in modo più dettagliato in [Più viewport: hit testing e gerarchia del viewport.](directmanipulation-multiple-vieports.md)

- Disabilitato: il viewport non elabora l'input né effettua callback. Un viewport può essere disabilitato da vari stati chiamando [**IDirectManipulationViewport::D isable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable). Se la disabilitazione automatica è stata impostata nel viewport, la transizione verrà eseguita automaticamente a Disabilitato dopo l'elaborazione di una manipolazione. Per abilitare nuovamente un viewport disabilitato, chiamare [**IDirectManipulationViewport::Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable).

## <a name="related-topics"></a>Argomenti correlati

[Più viewport: hit testing e gerarchia del viewport,](directmanipulation-multiple-vieports.md) [**ActivateConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration) [**GetOutputTransform,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
