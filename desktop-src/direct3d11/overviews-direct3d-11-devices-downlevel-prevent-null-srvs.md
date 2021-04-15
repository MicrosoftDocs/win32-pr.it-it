---
title: Prevenzione del SRVs di pixel shader NULL indesiderati
description: In questo argomento viene illustrato come aggirare il driver che riceve i valori NULL shader-Resource views (SRVs) anche quando SRVs non NULL sono associati alla fase pixel shader.
ms.assetid: c832c199-59b8-4079-a159-45490a2f6a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bacacf7704cffe12df44b9b0be667632307adb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992864"
---
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a>Prevenzione del SRVs di pixel shader NULL indesiderati

Le applicazioni Direct3D 11 eseguite su hardware grafico Direct3D 9 potrebbero inavvertitamente provocare la ricezione di visualizzazioni di risorse shader **null** (SRVs) anche quando le applicazioni associano SRVs non **null** alla fase pixel shader. Questa situazione può verificarsi solo se le applicazioni eliminano SRVs durante l'esecuzione. In questo argomento viene illustrato come aggirare il driver che riceve i **valori null** shader-Resource views (SRVs) anche quando SRVs non **null** sono associati alla fase pixel shader.

Per impedire al driver di ricevere SRVs **null** indesiderati, le applicazioni devono chiamare [**sul ID3D11DeviceContext::P ssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) per annullare tutti i SRVs prima di ogni chiamata a [**sul ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader). Tuttavia, se le applicazioni non distruggono SRVs fino alla fine dell'esecuzione del codice, non è necessario annullare il SRVs.

Nella sezione di [riferimento 10Level9](d3d11-graphics-reference-10level9.md) sono elencate le differenze tra il comportamento di diversi metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a diversi livelli di funzionalità di 10Level9.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direct3D 11 su hardware di livello inferiore](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




