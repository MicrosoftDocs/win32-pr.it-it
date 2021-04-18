---
title: Strutture shader (grafica Direct3D 12)
description: d3d12shader. h dichiara le strutture seguenti, che vengono usate per creare e usare gli shader.
ms.assetid: b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0
keywords:
- strutture, Direct3D 12 shader
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400d50c48b8b94fc9a59d8e48179aae43e14a4f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300834"
---
# <a name="shader-structures-direct3d-12-graphics"></a><span data-ttu-id="072ec-104">Strutture shader (grafica Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="072ec-104">Shader Structures (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="072ec-105">d3d12shader. h dichiara le strutture seguenti, che vengono usate per creare e usare gli shader.</span><span class="sxs-lookup"><span data-stu-id="072ec-105">d3d12shader.h declares the following structures, which are used to create and use shaders.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="072ec-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="072ec-106">In this section</span></span>



| <span data-ttu-id="072ec-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="072ec-107">Topic</span></span>                                                                                  | <span data-ttu-id="072ec-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="072ec-108">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="072ec-109">**\_Funzione D3D12 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="072ec-109">**D3D12\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_function_desc)<br/>                        | <span data-ttu-id="072ec-110">Descrive una funzione.</span><span class="sxs-lookup"><span data-stu-id="072ec-110">Describes a function.</span></span> <br/>                                       |
| [<span data-ttu-id="072ec-111">**D3D12 \_ libreria \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="072ec-111">**D3D12\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_library_desc)<br/>                          | <span data-ttu-id="072ec-112">Descrive una libreria.</span><span class="sxs-lookup"><span data-stu-id="072ec-112">Describes a library.</span></span> <br/>                                        |
| [<span data-ttu-id="072ec-113">**\_Parametro D3D12 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="072ec-113">**D3D12\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_parameter_desc)<br/>                      | <span data-ttu-id="072ec-114">Descrive un parametro di funzione.</span><span class="sxs-lookup"><span data-stu-id="072ec-114">Describes a function parameter.</span></span> <br/>                             |
| [<span data-ttu-id="072ec-115">**D3D12 \_ buffer shader \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="072ec-115">**D3D12\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_buffer_desc)<br/>             | <span data-ttu-id="072ec-116">Descrive un buffer costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="072ec-116">Describes a shader constant-buffer.</span></span> <br/>                         |
| [<span data-ttu-id="072ec-117">**D3D12 \_ shader \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="072ec-117">**D3D12\_SHADER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_desc)<br/>                            | <span data-ttu-id="072ec-118">Descrive uno shader.</span><span class="sxs-lookup"><span data-stu-id="072ec-118">Describes a shader.</span></span> <br/>                                         |
| [<span data-ttu-id="072ec-119">**D3D12 di \_ \_ Binding shader input \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="072ec-119">**D3D12\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_input_bind_desc)<br/>    | <span data-ttu-id="072ec-120">Viene descritto come una risorsa shader è associata a un input dello shader.</span><span class="sxs-lookup"><span data-stu-id="072ec-120">Describes how a shader resource is bound to a shader input.</span></span> <br/> |
| [<span data-ttu-id="072ec-121">**D3D12 \_ shader di \_ tipo \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="072ec-121">**D3D12\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_type_desc)<br/>                 | <span data-ttu-id="072ec-122">Descrive un tipo di variabile shader.</span><span class="sxs-lookup"><span data-stu-id="072ec-122">Describes a shader-variable type.</span></span> <br/>                           |
| [<span data-ttu-id="072ec-123">**D3D12 \_ variabile shader \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="072ec-123">**D3D12\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_variable_desc)<br/>         | <span data-ttu-id="072ec-124">Descrive una variabile shader.</span><span class="sxs-lookup"><span data-stu-id="072ec-124">Describes a shader variable.</span></span> <br/>                                |
| [<span data-ttu-id="072ec-125">**\_Parametro della firma D3D12 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="072ec-125">**D3D12\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_signature_parameter_desc)<br/> | <span data-ttu-id="072ec-126">Descrive una firma dello shader.</span><span class="sxs-lookup"><span data-stu-id="072ec-126">Describes a shader signature.</span></span> <br/>                               |



 

## <a name="related-topics"></a><span data-ttu-id="072ec-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="072ec-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="072ec-128">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="072ec-128">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="072ec-129">Riferimento shader</span><span class="sxs-lookup"><span data-stu-id="072ec-129">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





