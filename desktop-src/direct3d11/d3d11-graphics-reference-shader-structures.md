---
title: Strutture shader (grafica Direct3D 11)
description: Le strutture vengono usate per creare e usare gli shader.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- strutture, Direct3D 11 shader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739591"
---
# <a name="shader-structures-direct3d-11-graphics"></a><span data-ttu-id="77be1-104">Strutture shader (grafica Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="77be1-104">Shader Structures (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="77be1-105">Le strutture vengono usate per creare e usare gli shader.</span><span class="sxs-lookup"><span data-stu-id="77be1-105">Structures are used to create and use shaders.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="77be1-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="77be1-106">In this section</span></span>



| <span data-ttu-id="77be1-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="77be1-107">Topic</span></span>                                                                                       | <span data-ttu-id="77be1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77be1-108">Description</span></span>                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="77be1-109">**D3D11 ( \_ istanza della classe) \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-109">**D3D11\_CLASS\_INSTANCE\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | <span data-ttu-id="77be1-110">Descrive un'istanza della classe HLSL.</span><span class="sxs-lookup"><span data-stu-id="77be1-110">Describes an HLSL class instance.</span></span><br/>                           |
| [<span data-ttu-id="77be1-111">**\_Descrizione della traccia d3d11 Compute \_ shader \_ \_**</span><span class="sxs-lookup"><span data-stu-id="77be1-111">**D3D11\_COMPUTE\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | <span data-ttu-id="77be1-112">Descrive un'istanza di compute shader da tracciare.</span><span class="sxs-lookup"><span data-stu-id="77be1-112">Describes an instance of a compute shader to trace.</span></span><br/>         |
| [<span data-ttu-id="77be1-113">**D3D11 \_ di \_ traccia del dominio shader \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-113">**D3D11\_DOMAIN\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | <span data-ttu-id="77be1-114">Descrive un'istanza di un Domain shader per la traccia.</span><span class="sxs-lookup"><span data-stu-id="77be1-114">Describes an instance of a domain shader to trace.</span></span><br/>          |
| [<span data-ttu-id="77be1-115">**\_Funzione d3d11 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-115">**D3D11\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | <span data-ttu-id="77be1-116">Descrive una funzione.</span><span class="sxs-lookup"><span data-stu-id="77be1-116">Describes a function.</span></span><br/>                                       |
| [<span data-ttu-id="77be1-117">**D3D11 \_ Geometry \_ shader \_ trace \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-117">**D3D11\_GEOMETRY\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | <span data-ttu-id="77be1-118">Descrive un'istanza di un geometry shader da tracciare.</span><span class="sxs-lookup"><span data-stu-id="77be1-118">Describes an instance of a geometry shader to trace.</span></span><br/>        |
| [<span data-ttu-id="77be1-119">**D3D11 \_ Hull \_ shader \_ trace \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-119">**D3D11\_HULL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | <span data-ttu-id="77be1-120">Descrive un'istanza di uno Hull shader da tracciare.</span><span class="sxs-lookup"><span data-stu-id="77be1-120">Describes an instance of a hull shader to trace.</span></span><br/>            |
| [<span data-ttu-id="77be1-121">**D3D11 \_ libreria \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-121">**D3D11\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | <span data-ttu-id="77be1-122">Descrive una libreria.</span><span class="sxs-lookup"><span data-stu-id="77be1-122">Describes a library.</span></span><br/>                                        |
| [<span data-ttu-id="77be1-123">**\_Parametro d3d11 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-123">**D3D11\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | <span data-ttu-id="77be1-124">Descrive un parametro di funzione.</span><span class="sxs-lookup"><span data-stu-id="77be1-124">Describes a function parameter.</span></span> <br/>                            |
| [<span data-ttu-id="77be1-125">**\_Descrizione della \_ traccia del pixel shader d3d11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="77be1-125">**D3D11\_PIXEL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | <span data-ttu-id="77be1-126">Descrive un'istanza di un pixel shader da tracciare.</span><span class="sxs-lookup"><span data-stu-id="77be1-126">Describes an instance of a pixel shader to trace.</span></span><br/>           |
| [<span data-ttu-id="77be1-127">**D3D11 \_ buffer shader \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-127">**D3D11\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | <span data-ttu-id="77be1-128">Descrive un buffer costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="77be1-128">Describes a shader constant-buffer.</span></span><br/>                         |
| [<span data-ttu-id="77be1-129">**D3D11 \_ shader \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-129">**D3D11\_SHADER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | <span data-ttu-id="77be1-130">Descrive uno shader.</span><span class="sxs-lookup"><span data-stu-id="77be1-130">Describes a shader.</span></span><br/>                                         |
| [<span data-ttu-id="77be1-131">**D3D11 di \_ \_ Binding shader input \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-131">**D3D11\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | <span data-ttu-id="77be1-132">Viene descritto come una risorsa shader è associata a un input dello shader.</span><span class="sxs-lookup"><span data-stu-id="77be1-132">Describes how a shader resource is bound to a shader input.</span></span><br/> |
| [<span data-ttu-id="77be1-133">**Descrizione della traccia dello \_ shader d3d11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="77be1-133">**D3D11\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | <span data-ttu-id="77be1-134">Descrive un oggetto traccia shader.</span><span class="sxs-lookup"><span data-stu-id="77be1-134">Describes a shader-trace object.</span></span><br/>                            |
| [<span data-ttu-id="77be1-135">**D3D11 \_ shader di \_ tipo \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-135">**D3D11\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | <span data-ttu-id="77be1-136">Descrive un tipo di variabile shader.</span><span class="sxs-lookup"><span data-stu-id="77be1-136">Describes a shader-variable type.</span></span><br/>                           |
| [<span data-ttu-id="77be1-137">**D3D11 \_ variabile shader \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-137">**D3D11\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | <span data-ttu-id="77be1-138">Descrive una variabile shader.</span><span class="sxs-lookup"><span data-stu-id="77be1-138">Describes a shader variable.</span></span><br/>                                |
| [<span data-ttu-id="77be1-139">**\_Parametro della firma d3d11 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="77be1-139">**D3D11\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | <span data-ttu-id="77be1-140">Descrive una firma dello shader.</span><span class="sxs-lookup"><span data-stu-id="77be1-140">Describes a shader signature.</span></span><br/>                               |
| [<span data-ttu-id="77be1-141">**\_Registro di traccia d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="77be1-141">**D3D11\_TRACE\_REGISTER**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | <span data-ttu-id="77be1-142">Descrive un registro di traccia.</span><span class="sxs-lookup"><span data-stu-id="77be1-142">Describes a trace register.</span></span><br/>                                 |
| [<span data-ttu-id="77be1-143">**\_Statistiche traccia \_ d3d11**</span><span class="sxs-lookup"><span data-stu-id="77be1-143">**D3D11\_TRACE\_STATS**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | <span data-ttu-id="77be1-144">Specifica le statistiche relative a una traccia.</span><span class="sxs-lookup"><span data-stu-id="77be1-144">Specifies statistics about a trace.</span></span><br/>                         |
| [<span data-ttu-id="77be1-145">**\_Passaggio di traccia d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="77be1-145">**D3D11\_TRACE\_STEP**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | <span data-ttu-id="77be1-146">Descrive un passaggio della traccia, che è un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="77be1-146">Describes a trace step, which is an instruction.</span></span><br/>            |
| [<span data-ttu-id="77be1-147">**\_Valore di traccia d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="77be1-147">**D3D11\_TRACE\_VALUE**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | <span data-ttu-id="77be1-148">Descrive un valore Trace.</span><span class="sxs-lookup"><span data-stu-id="77be1-148">Describes a trace value.</span></span><br/>                                    |
| [<span data-ttu-id="77be1-149">**\_Descrizione della \_ traccia Vertex \_ shader \_ d3d11**</span><span class="sxs-lookup"><span data-stu-id="77be1-149">**D3D11\_VERTEX\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | <span data-ttu-id="77be1-150">Descrive un'istanza di un vertex shader da tracciare.</span><span class="sxs-lookup"><span data-stu-id="77be1-150">Describes an instance of a vertex shader to trace.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="77be1-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77be1-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77be1-152">Riferimento shader</span><span class="sxs-lookup"><span data-stu-id="77be1-152">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





