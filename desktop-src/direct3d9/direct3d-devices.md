---
description: Un dispositivo Direct3D è il componente di rendering di Direct3D. Incapsula e archivia lo stato di rendering. Inoltre, un dispositivo Direct3D esegue trasformazioni e operazioni di illuminazione e rasterizza un'immagine su una superficie.
ms.assetid: b592edb8-351a-4a82-9ff7-8a69d82723bc
title: Dispositivi Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b36ae856686c0f6a0b821b92a871ed98e016bf1a010200038281f2eb50964e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096056"
---
# <a name="direct3d-devices-direct3d-9"></a>Dispositivi Direct3D (Direct3D 9)

Un dispositivo Direct3D è il componente di rendering di Direct3D. Incapsula e archivia lo stato di rendering. Inoltre, un dispositivo Direct3D esegue trasformazioni e operazioni di illuminazione e rasterizza un'immagine su una superficie.

-   [XPDM e WDDM](xpdm-vs-wddm.md)
-   [Tipi di dispositivo (Direct3D 9)](device-types.md)
-   [Creazione di un dispositivo (Direct3D 9)](creating-a-device.md)
-   [Modalità finestra e Full-Screen predefinita (Direct3D 9)](windowed-vs-full-screen-mode.md)
-   [Selezione di un dispositivo (Direct3D 9)](selecting-a-device.md)
-   [Dispositivi persi (Direct3D 9)](lost-devices.md)
-   [Determinazione del supporto hardware (Direct3D 9)](determining-hardware-support.md)
-   [Elaborazione dei dati dei vertici (Direct3D 9)](processing-vertex-data.md)
-   [Primitives](primitives.md)

A livello di architettura, i dispositivi Direct3D contengono un modulo di trasformazione, un modulo di illuminazione e un modulo di rasterizzazione, come illustrato nel diagramma seguente.

![Diagramma dell'architettura dei dispositivi direct3d](images/d3ddev.png)

Direct3D supporta attualmente due tipi principali di dispositivi Direct3D:

-   Un dispositivo hal con rasterizzazione e ombreggiatura con accelerazione hardware con elaborazione dei vertici hardware e software
-   Un dispositivo di riferimento

È possibile pensare a questi dispositivi come a due driver separati. I dispositivi software e di riferimento sono rappresentati da driver software e il dispositivo hal è rappresentato da un driver hardware. Il modo più comune per sfruttare questi dispositivi è usare il dispositivo hal per la spedizione delle applicazioni e il dispositivo di riferimento per il test delle funzionalità. Queste vengono fornite da terze parti per emulare dispositivi specifici, ad esempio hardware di sviluppo che non è ancora stato rilasciato.

Il dispositivo Direct3D creato da un'applicazione deve corrispondere alle funzionalità dell'hardware in cui è in esecuzione l'applicazione. Direct3D offre funzionalità di rendering, accedendo all'hardware 3D installato nel computer o emulando le funzionalità dell'hardware 3D nel software. Pertanto, Direct3D fornisce dispositivi per l'accesso hardware e l'emulazione del software.

I dispositivi con accelerazione hardware offrono prestazioni molto migliori rispetto ai dispositivi software. Il tipo di dispositivo hal è disponibile in tutte le schede grafiche supportate da Direct3D. Nella maggior parte dei casi, le applicazioni hanno come destinazione computer con accelerazione hardware e che si basano sull'emulazione software per supportare i computer di fascia inferiore.

Ad eccezione del dispositivo di riferimento, i dispositivi software non supportano sempre le stesse funzionalità di un dispositivo hardware. Le applicazioni devono sempre eseguire query per le funzionalità del dispositivo per determinare quali funzionalità sono supportate.

Poiché il comportamento del software e dei dispositivi di riferimento forniti con Direct3D 9 è identico a quello del dispositivo hal, il codice dell'applicazione creato per funzionare con il dispositivo hal funzionerà con il software o i dispositivi di riferimento senza modifiche. Si noti che mentre il comportamento del software o del dispositivo di riferimento fornito è identico a quello del dispositivo hal, le funzionalità del dispositivo variano e un particolare dispositivo software può implementare un set di funzionalità molto più piccolo.

## <a name="behaviors"></a>Comportamenti

Direct3D consente di specificare il comportamento di un dispositivo, nonché il tipo di dispositivo. Il [**metodo IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) consente a una combinazione di uno o più flag di comportamento di controllare i comportamenti globali del dispositivo Direct3D. Questi comportamenti specificano che cosa è e non viene gestito nella parte di run-time di Direct3D e i tipi di dispositivo specificano il driver da usare. Anche se alcune combinazioni di comportamenti del dispositivo non sono valide, è possibile usare tutti i comportamenti dei dispositivi con tutti i tipi di dispositivo. Ad esempio, è possibile specificare D3DDEVTYPE SW in un \_ dispositivo creato con D3DCREATE \_ PUREDEVICE.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 
