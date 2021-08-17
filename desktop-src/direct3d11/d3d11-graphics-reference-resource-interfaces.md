---
title: Interfacce di risorse (grafica Direct3D 11)
description: Sono disponibili diverse interfacce per i due tipi di base di buffer e trame delle risorse.
ms.assetid: 8e40573a-b186-41ec-b2ff-81279d77bd3a
keywords:
- interfacce, risorsa Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0896bd04a51a989e502676ee314e17d1bf94a110df8a5af9dfe82210dd1b6b71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125345"
---
# <a name="resource-interfaces-direct3d-11-graphics"></a>Interfacce di risorse (grafica Direct3D 11)

Sono disponibili diverse interfacce per i due tipi di risorse di base: buffer e trame. Sono disponibili anche interfacce per le visualizzazioni delle risorse.

Un'applicazione usa una visualizzazione per associare una risorsa a una fase della pipeline. La visualizzazione definisce come è possibile accedere alla risorsa durante il rendering. In questa sezione vengono descritte le interfacce di visualizzazione.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                       | Descrizione                                                                                                                                                                                            |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)<br/>                             | Un'interfaccia del buffer accede a una risorsa buffer, ovvero una memoria non strutturata. I buffer archiviano in genere i dati dei vertici o degli indici.<br/>                                                                  |
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)<br/>         | Un'interfaccia depth-stencil-view accede a una risorsa trama durante il test di profondità-stencil.<br/>                                                                                                    |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)<br/>         | Un'interfaccia render-target-view identifica le sottorisorse della destinazione di rendering a cui è possibile accedere durante il rendering.<br/>                                                                             |
| [**ID3D11RenderTargetView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rendertargetview1)<br/>       | Un'interfaccia render-target-view rappresenta le sottorisorse di destinazione di rendering a cui è possibile accedere durante il rendering.<br/>                                                                             |
| [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)<br/>                         | Un'interfaccia delle risorse fornisce azioni comuni su tutte le risorse.<br/>                                                                                                                              |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)<br/>     | Un'interfaccia shader-resource-view specifica le sottorisorse a cui uno shader può accedere durante il rendering. Esempi di risorse shader includono un buffer costante, un buffer di trama e una trama.<br/>  |
| [**ID3D11ShaderResourceView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11shaderresourceview1)<br/>   | Un'interfaccia shader-resource-view rappresenta le sottorisorse a cui uno shader può accedere durante il rendering. Esempi di risorse shader includono un buffer costante, un buffer di trama e una trama.<br/> |
| [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)<br/>                       | Un'interfaccia di trama 1D accede ai dati texel, ovvero alla memoria strutturata.<br/>                                                                                                                     |
| [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)<br/>                       | Un'interfaccia di trama 2D gestisce i dati texel, ovvero la memoria strutturata.<br/>                                                                                                                      |
| [**ID3D11Texture2D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture2d1)<br/>                     | Un'interfaccia di trama 2D rappresenta i dati texel, ovvero la memoria strutturata.<br/>                                                                                                                   |
| [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d)<br/>                       | Un'interfaccia di trama 3D accede ai dati texel, ovvero alla memoria strutturata.<br/>                                                                                                                     |
| [**ID3D11Texture3D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture3d1)<br/>                     | Un'interfaccia di trama 3D rappresenta i dati texel, ovvero la memoria strutturata.<br/>                                                                                                                   |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)<br/>   | Un'interfaccia di visualizzazione specifica le parti di una risorsa a cui la pipeline può accedere durante il rendering.<br/>                                                                                                |
| [**ID3D11UnorderedAccessView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11unorderedaccessview1)<br/> | Un'interfaccia di visualizzazione di accesso non ordinato rappresenta le parti di una risorsa a cui la pipeline può accedere durante il rendering.<br/>                                                                             |
| [**ID3D11View**](/windows/desktop/api/D3D11/nn-d3d11-id3d11view)<br/>                                 | Un'interfaccia di visualizzazione specifica le parti di una risorsa a cui la pipeline può accedere durante il rendering.<br/>                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla risorsa](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





