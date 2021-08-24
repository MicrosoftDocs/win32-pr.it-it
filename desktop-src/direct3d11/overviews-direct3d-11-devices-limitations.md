---
title: Limitazioni relative alla creazione di dispositivi WARP e di riferimento
description: Esistono alcune limitazioni per la creazione di dispositivi WARP e Di riferimento in Direct3D 10.1 e Direct3D 11.0. In questo argomento vengono illustrate queste limitazioni.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0483ed6d5fd7348df39a4f3064f377845d6bfae1fe46abc47be5acd99e191c29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608611"
---
# <a name="limitations-creating-warp-and-reference-devices"></a>Limitazioni relative alla creazione di dispositivi WARP e di riferimento

Esistono alcune limitazioni per la creazione di dispositivi WARP e Di riferimento in Direct3D 10.1 e Direct3D 11.0. In questo argomento vengono illustrate queste limitazioni.

I tipi di driver D3D10 DRIVER TYPE WARP e D3D10 DRIVER TYPE REFERENCE non sono supportati nei livelli di funzionalità \_ \_ \_ \_ \_ \_ D3D10 \_ FEATURE \_ LEVEL 9 da 1 a \_ \_ D3D10 \_ FEATURE LEVEL \_ \_ 9 \_ 3 in Direct3D 10.1. Inoltre, il tipo di driver D3D DRIVER TYPE WARP non è supportato in \_ \_ \_ D3D \_ FEATURE \_ LEVEL \_ 11 \_ 0 in Direct3D 11.0. In altri casi, quando si chiama [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) per creare un dispositivo Direct3D 10.1 o quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare un dispositivo Direct3D 11.0, se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità nella chiamata, la chiamata non è valida. Solo le combinazioni seguenti di livelli di funzionalità, runtime e tipi di driver sono valide per i dispositivi WARP e Reference:

-   D3D DRIVER TYPE WARP in tutti i livelli di \_ \_ funzionalità in \_ Direct3D 11.1, che Windows 8 include

    RIFERIMENTO AL TIPO DI DRIVER D3D \_ in tutti i livelli di funzionalità in \_ \_ Direct3D 11.1

    Quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare un dispositivo Direct3D 11.1, la chiamata è valida se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità.

-   D3D \_ DRIVER \_ TYPE \_ WARP on D3D \_ FEATURE LEVEL \_ \_ \_ 9 1 through D3D \_ FEATURE LEVEL \_ \_ 10 \_ 1 feature levels in Direct3D 11

    D3D \_ DRIVER TYPE REFERENCE on \_ \_ D3D \_ FEATURE LEVEL \_ \_ 9 \_ 1 through D3D \_ FEATURE LEVEL \_ \_ 11 0 feature levels in \_ Direct3D 11

    Quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare un dispositivo Direct3D 11, la chiamata è valida se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità.

-   D3D10 \_ DRIVER \_ TYPE \_ WARP and D3D10 \_ DRIVER TYPE REFERENCE on \_ \_ D3D10 \_ FEATURE LEVEL \_ \_ 10 \_ 0 through D3D10 \_ FEATURE LEVEL \_ \_ \_ 10 1 feature levels in Direct3D 10.1

    Quando si chiama [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) per creare un dispositivo Direct3D 10.1, la chiamata è valida se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> <dt>

[Introduzione a Direct3D 11 nell'hardware di livello inferiore](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[Procedura: Creare un dispositivo WARP](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[Procedura: Creare un dispositivo di riferimento](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[**TIPO DI DRIVER D3D10 \_ \_**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[**D3D10 \_ FEATURE \_ LEVEL1**](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[**TIPO DI DRIVER D3D \_ \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[**LIVELLO DI FUNZIONALITÀ \_ \_ D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 