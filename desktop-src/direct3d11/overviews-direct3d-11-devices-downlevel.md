---
title: Direct3D 11 su hardware di livello inferiore
description: Questa sezione illustra il modo in cui Direct3D 11 è progettato per supportare hardware nuovi ed esistenti, da DirectX 9 a DirectX 11.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104557583"
---
# <a name="direct3d-11-on-downlevel-hardware"></a>Direct3D 11 su hardware di livello inferiore

Questa sezione illustra il modo in cui Direct3D 11 è progettato per supportare hardware nuovi ed esistenti, da DirectX 9 a DirectX 11.

Questo diagramma illustra in che modo Direct3D 11 supporta hardware nuovo ed esistente.

![diagramma dell'hardware supportato da Direct3D 11](images/d3d11-on-downlevel-hardware.png)

Con Direct3D 11, viene introdotto un nuovo paradigma denominato livelli di funzionalità. Un livello di funzionalità è un set di funzionalità GPU ben definito. Utilizzando un livello di funzionalità, è possibile fare riferimento a un'applicazione Direct3D per l'esecuzione in una versione di livello inferiore di hardware Direct3D.

Nella sezione di [riferimento 10Level9](d3d11-graphics-reference-10level9.md) sono elencate le differenze tra il comportamento di diversi metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a diversi livelli di funzionalità di 10Level9.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                  | Descrizione                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Livelli di funzionalità Direct3D](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | In questo argomento vengono illustrati i livelli di funzionalità Direct3D.<br/>                                                                                                                       |
| [Eccezioni](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | Questo argomento descrive le eccezioni quando si usa Direct3D 11 su hardware di livello inferiore. <br/>                                                                                      |
| [Compute Shaders su hardware di livello inferiore](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | Questo argomento illustra come usare [Compute Shaders](direct3d-11-advanced-stages-compute-shader.md) in un'app Direct3D 11 su hardware Direct3D 10.<br/>             |
| [Prevenzione del SRVs di pixel shader NULL indesiderati](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | In questo argomento viene illustrato come aggirare il driver che riceve i **valori null** shader-Resource views (SRVs) anche quando SRVs non **null** sono associati alla fase pixel shader.<br/> |



 

## <a name="how-to-topics-about-feature-levels"></a>Procedure per i livelli di funzionalità



| Argomento                                                                                                                                                                                                                                                                   | Descrizione                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Procedura: ottenere il livello di funzionalità del dispositivo](overviews-direct3d-11-devices-downlevel-get.md)<br/> | Come ottenere un livello di funzionalità.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





