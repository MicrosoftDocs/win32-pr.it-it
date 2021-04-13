---
description: Tipi di dispositivo (Direct3D 9)
ms.assetid: 860f3de2-beaf-4df1-82d0-a4b7508156c2
title: Tipi di dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84efe80c022403c36e760860893f3619e1c9356
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341626"
---
# <a name="device-types-direct3d-9"></a>Tipi di dispositivo (Direct3D 9)

## <a name="hal-device"></a>Dispositivo HAL

Il tipo di dispositivo principale è il dispositivo Hal, che supporta la rasterizzazione accelerata hardware e l'elaborazione dei vertici hardware e software. Se il computer in cui è in esecuzione l'applicazione è dotato di una scheda di visualizzazione che supporta Direct3D, l'applicazione deve usarla per le operazioni Direct3D. I dispositivi Direct3D Hal implementano interamente o in parte i moduli di trasformazione, illuminazione e rasterizzazione nell'hardware.

Le applicazioni non accedono direttamente alle schede grafiche. Chiamano funzioni e metodi Direct3D. Direct3D accede all'hardware tramite HAL. Se il computer in cui è in esecuzione l'applicazione supporta l'HAL, otterrà le prestazioni migliori usando un dispositivo Hal.

Per creare un dispositivo Hal, chiamare [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) usando D3DDEVTYPE \_ HAL come tipo di dispositivo.

## <a name="reference-device"></a>Dispositivo di riferimento

Direct3D supporta un tipo di dispositivo aggiuntivo denominato dispositivo di riferimento o rasterizzazione dei riferimenti. A differenza di un dispositivo software, l'unità di rasterizzazione dei riferimenti supporta tutte le funzionalità Direct3D. Questo dispositivo deve essere usato a scopo di debug ed è pertanto disponibile solo nei computer in cui è installato DirectX SDK. Poiché queste funzionalità sono implementate per l'accuratezza anziché per la velocità e sono implementate nel software, i risultati non sono molto veloci. L'rasterizzazione dei riferimenti usa istruzioni della CPU speciali ogni volta che è possibile, ma non è destinata alle applicazioni di vendita al dettaglio. Utilizzare l'rasterizzazione dei riferimenti solo a scopo di test o dimostrazione di funzionalità. Per creare un dispositivo di riferimento, chiamare il metodo [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) usando D3DDEVTYPE \_ ref come tipo di dispositivo.

## <a name="hal-vs-ref-devices"></a>Dispositivi HAL e REF

I dispositivi HAL (Hardware Abstraction Layer) e i dispositivi REF (REFerence rasterizzator) sono i due tipi principali di dispositivo Direct3D; il primo è basato sul supporto hardware ed è molto veloce, ma potrebbe non supportare tutti gli elementi; Sebbene il secondo non usi l'accelerazione hardware, è molto lento, ma è garantito che supporti l'intero set di funzionalità Direct3D, in modo corretto. In generale, è necessario usare solo i dispositivi HAL, ma se si usa una funzionalità avanzata che non è supportata dalla scheda grafica, potrebbe essere necessario eseguire il fallback a REF.

L'altra volta è possibile usare REF se il dispositivo HAL produce risultati anomali, ovvero se il codice è corretto, ma il risultato non è quello che si sta aspettando. Il comportamento del dispositivo REF è garantito, quindi è consigliabile testare l'applicazione sul dispositivo REF e verificare se il comportamento anomalo continua. In caso contrario, significa che (a) l'applicazione presuppone che la scheda grafica supporti qualcosa che non lo è o (b) si tratta di un bug del driver. Se ancora non funziona con il dispositivo REF, si tratta di un bug dell'applicazione.

## <a name="hardware-vs-software-vertex-processing"></a>Elaborazione dei vertici hardware e software

L'elaborazione dei vertici hardware e software si applica effettivamente solo ai dispositivi HAL. Quando si effettua il push dei vertici attraverso la pipeline, è necessario trasformarli (dalle matrici di mondo, vista e proiezione a sua volta) e illuminati (da luci incorporate D3D's): questa fase di elaborazione è nota come T&L (per la trasformazione & illuminazione). L'elaborazione dei vertici hardware significa che questa operazione viene eseguita nell'hardware, se supportata dall'hardware. Ergo, l'elaborazione di vertici software è il software. La procedura generale consiste nel provare a creare un dispositivo T&L hardware per primo e, in caso di esito negativo, provare a combinare e in caso di esito negativo provare il software. Se il software ha esito negativo, rinunciare e uscire con un errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
