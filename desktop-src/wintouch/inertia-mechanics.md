---
title: Meccanismi di inerzia
description: Meccanismi di inerzia
ms.assetid: 188b6936-b36e-4e57-9118-8b61ed134c17
keywords:
- Windows Touch, inerzia
- Windows Touch, Smooth Animation
- Windows Touch, margine elastico
- inerzia, meccanica
- inerzia, nozioni fondamentali sui calcoli
- inerzia, panoramica della fisica
- inerzia, Smooth Animation
- inerzia, margine elastico
- animazione uniforme
- margine elastico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79b27900c6921c972710e7e922ab42b834afc1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328964"
---
# <a name="inertia-mechanics"></a>Meccanismi di inerzia

L'inerzia viene utilizzata per eseguire calcoli per animare lo spostamento di oggetti e per abilitare il supporto per l'usabilità generica nelle applicazioni che incorporano Windows Touch. Questa sezione illustra le funzionalità seguenti che sono abilitate per inerzia.

-   Breve panoramica della fisica dell'inerzia.
-   Animazione di oggetti smussata utilizzando le proprietà velocità e decelerazione.
-   Animazione di oggetti smussata utilizzando una proprietà di spostamento.
-   Rimbalzo dai bordi dello schermo usando i limiti elastici.

## <a name="inertia-physics-overview"></a>Panoramica della fisica dell'inerzia

Il processore di inerzia usa un semplice modello di fisica che incorpora una posizione, un valore di decelerazione e una velocità iniziale. Time viene utilizzato come input dinamico per il modello per determinare la posizione corrente di un oggetto che viene spostato. Il grafico e la formula seguenti delineano il modello di fisica usato per il calcolo delle posizioni degli oggetti.

![illustrazione che mostra il grafico e la formula usati per calcolare le posizioni degli oggetti](images/velocity.png)

Nella formula utilizzata per calcolare la posizione corrente (x), la velocità iniziale (v) viene moltiplicata per il tempo trascorso (t) ed è ridotta dal fattore di decelerazione (d) volte al quadrato. Ciò comporta una decelerazione dell'oggetto uniforme. Nell'illustrazione precedente alla parte iniziale (a sinistra) della curva, l'oggetto si muove rapidamente perché la velocità corrente è la velocità iniziale. Alla parte finale (all'estrema destra) della curva, l'oggetto è stato completamente interrotto perché la velocità è 0. I calcoli della velocità dell'oggetto per la velocità x, la velocità y e la velocità rotazionale utilizzano questa formula per i calcoli.

Tutta la distanza utilizzata per il processore di inerzia è relativa. Se si desidera utilizzare le coordinate dello schermo, passare le coordinate dello schermo al processore di manipolazione (o inerzia); Se si desidera utilizzare le coordinate assolute, passarle al processore utilizzato. Indipendentemente dai valori utilizzati, il processore di manipolazione utilizzerà i tick del clock in millisecondi per l'elaborazione del tempo. Questi valori possono essere passati direttamente al processore di inerzia usando il metodo [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) o usando il timestamp predefinito tramite le chiamate a [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process).

## <a name="smooth-object-animation-using-the-velocity-and-deceleration-properties"></a>Animazione di oggetti Smooth usando le proprietà di velocità e decelerazione

È possibile abilitare Smooth Animation interagendo direttamente con il modello di fisica impostando i valori di velocità e decelerazione nell'interfaccia del processore di inerzia e quindi chiamando il [**processo**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process). Il **processo** chiamante attiverà le manipolazioni degli oggetti che a loro volta dovrebbero causare gli aggiornamenti dell'interfaccia utente. I valori relativi alla velocità degli oggetti passati al processore di inerzia vengono in genere ricavati dal processore di manipolazione al termine dell'esecuzione. Il valore di decelerazione dipenderà dal tempo per cui si desidera animare l'oggetto e dalle unità utilizzate per i calcoli. Poiché i valori sono dipendenti, a volte è necessario ridimensionare la velocità di input dal processore maniplation e utilizzare valori arbitrari per la decelerazione. I valori seguenti sono tipici per i vari scenari in cui si passano i valori centipixel dalle proprietà x e y della struttura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) al processore di manipolazione.



| Scenario    | Insieme di proprietà                                                                       | Valore decelerazione | Scalabilità di input della velocità tipica                                  | Note                                                                                 |
|-------------|------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| Traduzione | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0.003 f             | Nessuna.                                                           | L'uso di questo valore comporterà animazioni a distanza più lunghe quando si usa l'input tocco.    |
| Traduzione | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,001 f             | 1/XX velocità iniziale per gli input di tocco, nessuna per gli input del mouse | L'uso di questo valore verrà animato per circa un secondo dato gli input di velocità tipici.      |
| Traduzione | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,5 f               | nessuno                                                            | L'uso di questo valore offre una sensazione naturale di animazione su schermi Windows Touch di grandi dimensioni.   |
| Rotazione    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000015 f          | Radianti convertiti in gradi.                                   | L'uso di questo valore comporta animazioni rotazionali più lunghe quando si usa l'input tocco.      |
| Rotazione    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.00001 f           | Delta di rotazione 1/40 per gli input di tocco, nessuno per gli input del mouse   | Questo valore è in radianti, quindi è necessario utilizzare valori di decelerazione e velocità molto ridotti. |
| Rotazione    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000005 f          | nessuno                                                            | Questo valore ha un aspetto naturale su schermi Windows Touch di grandi dimensioni.                        |



 

## <a name="smooth-object-animation-using-the-desired-displacement-property"></a>Animazione di oggetti Smooth usando la proprietà di spostamento desiderata

In alcuni casi, non si vuole usare l'input dell'utente per lo spostamento di oggetti, ma si vuole comunque che un oggetto venga animato in modo uniforme sullo schermo. In questo caso, è possibile usare le proprietà di spostamento nel processore di inerzia affinché il processore calcoli la velocità iniziale per lo spostamento di un oggetto sullo schermo.

## <a name="controlling-object-position-using-elastic-bounds"></a>Controllo della posizione dell'oggetto mediante i limiti elastici

Quando si dispone di un oggetto spostato sullo schermo, in genere si vuole arrestarlo prima che vada fuori dal punto di vista dell'utente. Il processore di inerzia Abilita questa funzionalità tramite le proprietà limite e margine elastico. Nell'immagine seguente vengono illustrate le varie proprietà limite e margine in un'applicazione tipica.

![screenshot che mostra le proprietà limite e margine elastico](images/elastic-illustrated.png)

Si impostano i limiti di sinistra, superiore, destro e inferiore e i margini elastici per l'applicazione e il processore di inerzia gestirà la conservazione degli elementi dell'interfaccia utente entro i limiti. Quando un oggetto raggiunge un margine elastico, verrà rallentato fino a raggiungere il limite. Non rilascerà mai tale margine durante l'inerzia, ma continuerà a spostarsi fino a quando il componente di inerzia perpendicolare dell'oggetto non rallenterà a 0. Nell'illustrazione un cerchio viene spostato verso il limite elastico sinistro. La freccia a tinta unita Mostra la direzione della manipolazione; il cerchio continuo è la posizione iniziale dell'oggetto. la freccia a tinta unita rappresenta le modifiche apportate prima che il cerchio raggiunga il margine elastico; la freccia tratteggiata indica il punto in cui il processore di inerzia manipola il cerchio dopo aver raggiunto il margine; e i cerchi tratteggiati mostrano dove si arresta l'oggetto.

> [!Note]  
> Impostando le proprietà dei margini, i limiti vengono spostati verso l'esterno. Se, ad esempio, il limite superiore è impostato su 50 e si imposta il margine elastico superiore su 10, il limite superiore diventerà effettivamente 40.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dell'inerzia nel codice non gestito](handling-inertia-in-unmanaged-code.md)
</dt> <dt>

[Inerzia](getting-started-with-inertia.md)
</dt> <dt>

[Modifiche](getting-started-with-manipulations.md)
</dt> </dl>

 

 




