---
title: Come creare uno Hull shader
description: In questo argomento viene illustrato come creare un Hull shader.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708182"
---
# <a name="how-to-create-a-hull-shader"></a><span data-ttu-id="d403c-103">Procedura: creare un Hull shader</span><span class="sxs-lookup"><span data-stu-id="d403c-103">How To: Create a Hull Shader</span></span>

<span data-ttu-id="d403c-104">Un Hull shader è il primo di tre fasi che interagiscono per implementare lo [schema a mosaico](direct3d-11-advanced-stages-tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="d403c-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="d403c-105">Gli output dello shader dello scafo rappresentano la fase mosaico, oltre alla fase Domain shader.</span><span class="sxs-lookup"><span data-stu-id="d403c-105">The hull-shader outputs drive the tessellator stage, as well as the domain-shader stage.</span></span> <span data-ttu-id="d403c-106">In questo argomento viene illustrato come creare un Hull shader.</span><span class="sxs-lookup"><span data-stu-id="d403c-106">This topic shows how to create a hull shader.</span></span>

<span data-ttu-id="d403c-107">Uno scafo shader trasforma un set di punti di controllo di input (da un vertex shader) in un set di punti di controllo di output.</span><span class="sxs-lookup"><span data-stu-id="d403c-107">A hull shader transforms a set of input control points (from a vertex shader) into a set of output control points.</span></span> <span data-ttu-id="d403c-108">Il numero di punti di input e di output può variare in base al contenuto e al numero a seconda della trasformazione. una trasformazione tipica sarebbe una trasformazione di base.</span><span class="sxs-lookup"><span data-stu-id="d403c-108">The number of input and output points can vary in contents and number depending on the transform (a typical transformation would be a basis transformation).</span></span>

<span data-ttu-id="d403c-109">Un Hull shader restituisce anche informazioni sulle costanti della patch, ad esempio i fattori a mosaico, per uno shader del dominio e il mosaico.</span><span class="sxs-lookup"><span data-stu-id="d403c-109">A hull shader also outputs patch constant information, such as tessellation factors, for a domain shader and the tessellator.</span></span> <span data-ttu-id="d403c-110">La fase mosaico a funzione fissa usa i fattori a mosaico e altri stati dichiarati in uno scafo shader per determinare la quantità di conteggiarla suddividerla.</span><span class="sxs-lookup"><span data-stu-id="d403c-110">The fixed-function tessellator stage uses the tessellation factors as well as other state declared in a hull shader to determine how much to tessellate.</span></span>

<span data-ttu-id="d403c-111">**Per creare un Hull shader**</span><span class="sxs-lookup"><span data-stu-id="d403c-111">**To create a hull shader**</span></span>

1.  <span data-ttu-id="d403c-112">Progettare uno scafo dello shader.</span><span class="sxs-lookup"><span data-stu-id="d403c-112">Design a hull shader.</span></span> <span data-ttu-id="d403c-113">Vedere [procedura: progettare uno scafo dello shader](direct3d-11-advanced-stages-hull-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="d403c-113">See [How To: Design a Hull Shader](direct3d-11-advanced-stages-hull-shader-design.md).</span></span>
2.  <span data-ttu-id="d403c-114">Compilare il codice dello shader</span><span class="sxs-lookup"><span data-stu-id="d403c-114">Compile the shader code</span></span>
3.  <span data-ttu-id="d403c-115">Creare un oggetto Hull shader usando [**ID3D11Device:: CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span><span class="sxs-lookup"><span data-stu-id="d403c-115">Create a hull-shader object using [**ID3D11Device::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span></span>
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  <span data-ttu-id="d403c-116">Inizializzare la fase della pipeline utilizzando [**sul ID3D11DeviceContext:: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="d403c-116">Initialize the pipeline stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="d403c-117">Se è associato un Hull shader, è necessario associare un Domain shader alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d403c-117">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="d403c-118">In particolare, non è consentito trasmettere direttamente i punti di controllo di Hull shader con il geometry shader.</span><span class="sxs-lookup"><span data-stu-id="d403c-118">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d403c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d403c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d403c-120">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d403c-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="d403c-121">Panoramica dello schema a mosaico</span><span class="sxs-lookup"><span data-stu-id="d403c-121">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




