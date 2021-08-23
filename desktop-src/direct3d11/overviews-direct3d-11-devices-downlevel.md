---
title: Direct3D 11 in hardware di livello inferiore
description: Questa sezione illustra come Direct3D 11 è progettato per supportare hardware nuovo ed esistente, da DirectX 9 a DirectX 11.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb9dde5bfaa32808752206ebe96702aaaf10cc39c1e053675ddfced765331be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045509"
---
# <a name="direct3d-11-on-downlevel-hardware"></a>Direct3D 11 in hardware di livello inferiore

Questa sezione illustra come Direct3D 11 è progettato per supportare hardware nuovo ed esistente, da DirectX 9 a DirectX 11.

Questo diagramma illustra come Direct3D 11 supporta hardware nuovo ed esistente.

![diagramma dell'hardware supportato da Direct3d 11](images/d3d11-on-downlevel-hardware.png)

Con Direct3D 11 viene introdotto un nuovo paradigma denominato livelli di funzionalità. Un livello di funzionalità è un set ben definito di funzionalità GPU. Usando un livello di funzionalità, è possibile impostare come destinazione un'applicazione Direct3D per l'esecuzione in una versione di livello inferiore dell'hardware Direct3D.

La [sezione 10Level9 Reference](d3d11-graphics-reference-10level9.md) elenca le differenze tra il comportamento dei vari metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a vari livelli di funzionalità 10Level9.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                  | Descrizione                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Livelli di funzionalità Direct3D](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | Questo argomento illustra i livelli di funzionalità Direct3D.<br/>                                                                                                                       |
| [Eccezioni](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | Questo argomento descrive le eccezioni quando si usa Direct3D 11 nell'hardware di livello inferiore. <br/>                                                                                      |
| [Shader di calcolo nell'hardware di livello inferiore](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | Questo argomento illustra come usare gli shader di [calcolo](direct3d-11-advanced-stages-compute-shader.md) in un'app Direct3D 11 nell'hardware Direct3D 10.<br/>             |
| [Prevenzione degli SRV pixel shader NULL indesiderati](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | Questo argomento illustra come aggirare  il driver che riceve viste shader-risorsa NULL (SV) anche quando gli SPV non **NULL** sono associati alla pixel shader fase.<br/> |



 

## <a name="how-to-topics-about-feature-levels"></a>Argomenti relativi ai livelli di funzionalità



| Argomento                                                                                                                                                                                                                                                                   | Descrizione                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Procedura: Ottenere il livello di funzionalità del dispositivo](overviews-direct3d-11-devices-downlevel-get.md)<br/> | Come ottenere un livello di funzionalità.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





