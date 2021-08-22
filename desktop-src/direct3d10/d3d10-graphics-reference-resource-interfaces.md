---
description: 'Direct3D 10 definisce una serie di interfacce per i due tipi di risorse di base: buffer e trame.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Interfacce delle risorse (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94eb7a0f2ce0b6792ccb98b95605f00504fbf239ee0cecf0846814d84566de9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282821"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a>Interfacce delle risorse (grafica Direct3D 10)

Direct3D 10 definisce una serie di interfacce per i due tipi di risorse di base: [buffer](d3d10-graphics-programming-guide-resources-types.md) e trame.



| Interfacce                                           | Descrizione                                          |
|------------------------------------------------------|------------------------------------------------------|
| [**Interfaccia ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | Accede ai dati del buffer.                                |
| [**Interfaccia ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | Classe di base per una risorsa.                           |
| [**Interfaccia ID3D10Texture1D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | Accede ai dati in una trama 1D o in una matrice di trame 1D. |
| [**Interfaccia ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | Accede ai dati in una trama 2D o in una matrice di trame 2D  |
| [**Interfaccia ID3D10Texture3D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | Accede ai dati in una trama 3D o in una matrice di trame 3D. |



 

Un'applicazione usa una vista per associare una risorsa a una [fase della pipeline.](d3d10-graphics-programming-guide-pipeline-stages.md) La [visualizzazione](d3d10-graphics-programming-guide-resources-access-views.md) definisce come è possibile accedere alla risorsa durante il rendering. L'API contiene queste interfacce di visualizzazione.



| Interfacce                                                               | Descrizione                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Interfaccia ID3D10DepthStencilView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | Accede ai dati in una [trama depth-stencil.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) |
| [**Interfaccia ID3D10RenderTargetView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | Accede ai dati in una destinazione [di rendering.](d3d10-graphics-programming-guide-resources-creating-textures.md)        |
| [**Interfaccia ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | Accede ai dati in una risorsa shader in Direct3D 10.0.                                                         |
| [**Interfaccia ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | Accede ai dati in una risorsa shader in Direct3D 10.1.                                                         |
| [**Interfaccia ID3D10View**](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | Classe di base per una vista.                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla risorsa](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
