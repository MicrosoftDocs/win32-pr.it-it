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
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a><span data-ttu-id="09714-103">Prevenzione del SRVs di pixel shader NULL indesiderati</span><span class="sxs-lookup"><span data-stu-id="09714-103">Preventing Unwanted NULL Pixel Shader SRVs</span></span>

<span data-ttu-id="09714-104">Le applicazioni Direct3D 11 eseguite su hardware grafico Direct3D 9 potrebbero inavvertitamente provocare la ricezione di visualizzazioni di risorse shader **null** (SRVs) anche quando le applicazioni associano SRVs non **null** alla fase pixel shader.</span><span class="sxs-lookup"><span data-stu-id="09714-104">Direct3D 11 applications that run on Direct3D 9 graphics hardware could inadvertently cause the driver to receive **NULL** shader-resource views (SRVs) even when the applications bind non-**NULL** SRVs to the pixel shader stage.</span></span> <span data-ttu-id="09714-105">Questa situazione può verificarsi solo se le applicazioni eliminano SRVs durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="09714-105">This situation can occur only if the applications destroy SRVs while they execute.</span></span> <span data-ttu-id="09714-106">In questo argomento viene illustrato come aggirare il driver che riceve i **valori null** shader-Resource views (SRVs) anche quando SRVs non **null** sono associati alla fase pixel shader.</span><span class="sxs-lookup"><span data-stu-id="09714-106">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span>

<span data-ttu-id="09714-107">Per impedire al driver di ricevere SRVs **null** indesiderati, le applicazioni devono chiamare [**sul ID3D11DeviceContext::P ssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) per annullare tutti i SRVs prima di ogni chiamata a [**sul ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span><span class="sxs-lookup"><span data-stu-id="09714-107">To prevent the driver from receiving unwanted **NULL** SRVs, the applications must call [**ID3D11DeviceContext::PSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) to unset all SRVs before each call to [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span></span> <span data-ttu-id="09714-108">Tuttavia, se le applicazioni non distruggono SRVs fino alla fine dell'esecuzione del codice, non è necessario annullare il SRVs.</span><span class="sxs-lookup"><span data-stu-id="09714-108">However, if the applications do not destroy SRVs until the end of their code execution, they do not need to unset the SRVs.</span></span>

<span data-ttu-id="09714-109">Nella sezione di [riferimento 10Level9](d3d11-graphics-reference-10level9.md) sono elencate le differenze tra il comportamento di diversi metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a diversi livelli di funzionalità di 10Level9.</span><span class="sxs-lookup"><span data-stu-id="09714-109">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09714-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="09714-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09714-111">Direct3D 11 su hardware di livello inferiore</span><span class="sxs-lookup"><span data-stu-id="09714-111">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




