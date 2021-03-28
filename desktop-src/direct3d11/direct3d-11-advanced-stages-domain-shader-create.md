---
title: Come creare uno shader di dominio
description: In questo argomento viene illustrato come creare un Domain shader.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044239"
---
# <a name="how-to-create-a-domain-shader"></a><span data-ttu-id="68e3e-103">Procedura: creare uno shader di dominio</span><span class="sxs-lookup"><span data-stu-id="68e3e-103">How To: Create a Domain Shader</span></span>

<span data-ttu-id="68e3e-104">Un Domain shader è il terzo di tre fasi che interagiscono per implementare lo [schema a mosaico](direct3d-11-advanced-stages-tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="68e3e-104">A domain shader is the third of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="68e3e-105">Gli input per la fase di shader del dominio provengono da uno scafo dello shader.</span><span class="sxs-lookup"><span data-stu-id="68e3e-105">The inputs for the domain-shader stage come from a hull shader.</span></span> <span data-ttu-id="68e3e-106">In questo argomento viene illustrato come creare un Domain shader.</span><span class="sxs-lookup"><span data-stu-id="68e3e-106">This topic shows how to create a domain shader.</span></span>

<span data-ttu-id="68e3e-107">Un Domain shader trasforma la geometria della superficie (creata dalla fase mosaico della funzione fissa) usando i punti di controllo di output di Hull shader, i dati della patch di output di Hull shader e un singolo set di coordinate UV di mosaico.</span><span class="sxs-lookup"><span data-stu-id="68e3e-107">A domain shader transforms surface geometry (created by the fixed-function tessellator stage) using hull shader output-control points, hull shader output patch-constant data, and a single set of tessellator uv coordinates.</span></span>

<span data-ttu-id="68e3e-108">**Per creare un Domain shader**</span><span class="sxs-lookup"><span data-stu-id="68e3e-108">**To create a domain shader**</span></span>

1.  <span data-ttu-id="68e3e-109">Progettare un Domain shader.</span><span class="sxs-lookup"><span data-stu-id="68e3e-109">Design a domain shader.</span></span> <span data-ttu-id="68e3e-110">Vedere [procedura: progettare un Domain shader](direct3d-11-advanced-stages-domain-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="68e3e-110">See [How To: Design a Domain Shader](direct3d-11-advanced-stages-domain-shader-design.md).</span></span>
2.  <span data-ttu-id="68e3e-111">Compilare il codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="68e3e-111">Compile the shader code.</span></span>
3.  <span data-ttu-id="68e3e-112">Creare un oggetto di shader di dominio usando [**ID3D11Device:: CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span><span class="sxs-lookup"><span data-stu-id="68e3e-112">Create a domain-shader object using [**ID3D11Device::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span></span>
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  <span data-ttu-id="68e3e-113">Inizializzare la fase della pipeline usando [**sul ID3D11DeviceContext::D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span><span class="sxs-lookup"><span data-stu-id="68e3e-113">Initialize the pipeline stage using [**ID3D11DeviceContext::DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span></span>
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="68e3e-114">Se è associato un Hull shader, è necessario associare un Domain shader alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="68e3e-114">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="68e3e-115">In particolare, non è consentito trasmettere direttamente i punti di controllo di Hull shader con il geometry shader.</span><span class="sxs-lookup"><span data-stu-id="68e3e-115">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68e3e-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68e3e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68e3e-117">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="68e3e-117">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="68e3e-118">Panoramica dello schema a mosaico</span><span class="sxs-lookup"><span data-stu-id="68e3e-118">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




