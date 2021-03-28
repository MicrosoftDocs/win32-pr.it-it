---
title: Limitazioni della creazione di dispositivi WARP e Reference
description: Esistono alcune limitazioni per la creazione di dispositivi WARP e Reference in Direct3D 10,1 e Direct3D 11,0. In questo argomento vengono illustrate tali limitazioni.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337558"
---
# <a name="limitations-creating-warp-and-reference-devices"></a>Limitazioni della creazione di dispositivi WARP e Reference

Esistono alcune limitazioni per la creazione di dispositivi WARP e Reference in Direct3D 10,1 e Direct3D 11,0. In questo argomento vengono illustrate tali limitazioni.

I tipi di driver di riferimento per il tipo di driver D3D10 e il driver \_ \_ \_ D3D10 \_ \_ \_ non sono supportati nei \_ \_ livelli di funzionalità di D3D10 da \_ 9 \_ a 2 \_ a D3D10 \_ \_ a livello di funzionalità 9 \_ 3 in Direct3D 10,1. Inoltre, il tipo di driver D3D del \_ \_ tipo \_ di driver non è supportato \_ nel livello di funzionalità D3D \_ \_ 11 \_ 0 in Direct3D 11,0. Ovvero, quando si chiama [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) per creare un dispositivo Direct3D 10,1 o quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare un dispositivo Direct3D 11,0, se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità nella chiamata, la chiamata non è valida. Solo le combinazioni seguenti di livelli di funzionalità, Runtime e tipi di driver sono valide per i dispositivi WARP e Reference:

-   \_ \_ Distorsione del tipo di driver D3D \_ a tutti i livelli di funzionalità in Direct3D 11,1, incluso in Windows 8

    Riferimento al tipo di driver D3D in \_ \_ \_ tutti i livelli di funzionalità in Direct3D 11,1

    Quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare un dispositivo Direct3D 11,1, la chiamata è valida se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità.

-   \_ \_ \_ Distorsione del tipo di driver D3D sul \_ livello di funzionalità D3D \_ \_ 9 \_ 1 tramite i \_ \_ \_ \_ livelli di funzionalità di 10 1 a livello di funzionalità D3D in Direct3D 11

    Informazioni \_ \_ di riferimento sul tipo di driver D3D \_ sul livello di \_ funzionalità D3D \_ \_ 9 \_ 1 tramite i \_ \_ livelli di funzionalità di livello funzionalità \_ di D3D 11 \_ in Direct3D 11

    Quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare un dispositivo Direct3D 11, la chiamata è valida se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità.

-   \_Guida \_ \_ \_ di riferimento al tipo di driver D3D10 e \_ al tipo di driver D3D10 \_ sul livello di funzionalità D3D10 da \_ \_ \_ 10 \_ 0 \_ a D3D10 \_ \_ \_ livelli di funzionalità 10 1 in Direct3D 10,1

    Quando si chiama [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) per creare un dispositivo Direct3D 10,1, la chiamata è valida se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> <dt>

[Introduzione a Direct3D 11 su hardware di livello inferiore](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[Procedura: creare un dispositivo WARP](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[Procedura: creare un dispositivo di riferimento](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[**\_Tipo di driver D3D10 \_**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[**\_Level1 funzionalità \_ D3D10**](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[**\_Tipo di driver D3D \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[**\_Livello di funzionalità D3D \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 