---
description: Un dispositivo Direct3D è il componente di rendering di Direct3D. Incapsula e archivia lo stato di rendering. Inoltre, un dispositivo Direct3D esegue trasformazioni e operazioni di illuminazione e Rasterizza un'immagine in una superficie.
ms.assetid: b592edb8-351a-4a82-9ff7-8a69d82723bc
title: Dispositivi Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07726069b952ba99d608e5f36df8e1fb7745cd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225389"
---
# <a name="direct3d-devices-direct3d-9"></a>Dispositivi Direct3D (Direct3D 9)

Un dispositivo Direct3D è il componente di rendering di Direct3D. Incapsula e archivia lo stato di rendering. Inoltre, un dispositivo Direct3D esegue trasformazioni e operazioni di illuminazione e Rasterizza un'immagine in una superficie.

-   [Confronto tra XPDM e WDDM](xpdm-vs-wddm.md)
-   [Tipi di dispositivo (Direct3D 9)](device-types.md)
-   [Creazione di un dispositivo (Direct3D 9)](creating-a-device.md)
-   [Modalità di confronto Full-Screen finestra (Direct3D 9)](windowed-vs-full-screen-mode.md)
-   [Selezione di un dispositivo (Direct3D 9)](selecting-a-device.md)
-   [Dispositivi persi (Direct3D 9)](lost-devices.md)
-   [Determinazione del supporto hardware (Direct3D 9)](determining-hardware-support.md)
-   [Elaborazione dei dati dei vertici (Direct3D 9)](processing-vertex-data.md)
-   [Primitives](primitives.md)

In architettura, i dispositivi Direct3D contengono un modulo di trasformazione, un modulo di illuminazione e un modulo di rasterizzazione, come illustrato nella figura seguente.

![diagramma dell'architettura del dispositivo Direct3D](images/d3ddev.png)

Direct3D supporta attualmente due tipi principali di dispositivi Direct3D:

-   Un dispositivo HAL con rasterizzazione e ombreggiatura con accelerazione hardware con l'elaborazione dei vertici hardware e software
-   Un dispositivo di riferimento

È possibile considerare questi dispositivi come due driver distinti. I dispositivi software e di riferimento sono rappresentati da driver software e il dispositivo Hal è rappresentato da un driver hardware. Il modo più comune per sfruttare questi dispositivi consiste nell'usare il dispositivo HAL per la distribuzione delle applicazioni e il dispositivo di riferimento per il test delle funzionalità. Questi vengono forniti da terze parti per emulare determinati dispositivi, ad esempio hardware di sviluppo che non sono stati ancora rilasciati.

Il dispositivo Direct3D creato da un'applicazione deve corrispondere alle funzionalità dell'hardware su cui è in esecuzione l'applicazione. Direct3D fornisce funzionalità di rendering, accedendo a hardware 3D installato nel computer o emulando le funzionalità dell'hardware 3D nel software. Pertanto, Direct3D fornisce i dispositivi sia per l'accesso hardware che per l'emulazione del software.

I dispositivi con accelerazione hardware offrono prestazioni decisamente migliori rispetto ai dispositivi software. Il tipo di dispositivo Hal è disponibile in tutte le schede grafiche supportate da Direct3D. Nella maggior parte dei casi, le applicazioni hanno come destinazione computer con accelerazione hardware e si basano sull'emulazione software per gestire i computer di fascia bassa.

Fatta eccezione per il dispositivo di riferimento, i dispositivi software non supportano sempre le stesse funzionalità di un dispositivo hardware. Le applicazioni devono sempre eseguire una query per le funzionalità del dispositivo per determinare quali funzionalità sono supportate.

Poiché il comportamento del software e dei dispositivi di riferimento forniti con Direct3D 9 è identico a quello del dispositivo Hal, il codice dell'applicazione creato per funzionare con il dispositivo Hal funzionerà con il software o con i dispositivi di riferimento senza modifiche. Si noti che anche se il software o il comportamento del dispositivo di riferimento è identico a quello del dispositivo Hal, le funzionalità del dispositivo variano e un particolare dispositivo software può implementare un set di funzionalità molto più piccolo.

## <a name="behaviors"></a>Comportamenti

Direct3D consente di specificare il comportamento di un dispositivo, nonché il tipo del dispositivo. Il metodo [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) Abilita una combinazione di uno o più flag di comportamento per controllare i comportamenti globali del dispositivo Direct3D. Questi comportamenti specificano cosa è e non vengono mantenuti nella parte runtime di Direct3D e i tipi di dispositivo specificano il driver da usare. Sebbene alcune combinazioni di comportamenti del dispositivo non siano valide, è possibile usare tutti i comportamenti del dispositivo con tutti i tipi di dispositivo. Ad esempio, è possibile specificare D3DDEVTYPE \_ SW in un dispositivo creato con D3DCREATE \_ PUREDEVICE.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 
