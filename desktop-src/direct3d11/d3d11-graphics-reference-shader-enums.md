---
title: Enumerazioni shader (grafica Direct3D 11)
description: Le enumerazioni vengono utilizzate per specificare informazioni sugli shader.
ms.assetid: 068ce652-8596-4492-992c-658d1fcf8a2c
keywords:
- enumerazioni, Direct3D 11 shader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d8a82f0844dba0a4fc1a8eed1cd2222f6b6680
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104976943"
---
# <a name="shader-enumerations-direct3d-11-graphics"></a><span data-ttu-id="a8549-104">Enumerazioni shader (grafica Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="a8549-104">Shader Enumerations (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="a8549-105">Le enumerazioni vengono utilizzate per specificare informazioni sugli shader.</span><span class="sxs-lookup"><span data-stu-id="a8549-105">Enumerations are used to specify information about shaders.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="a8549-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a8549-106">In this section</span></span>



| <span data-ttu-id="a8549-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="a8549-107">Topic</span></span>                                                                                          | <span data-ttu-id="a8549-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8549-108">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a8549-109">[**\_Tipo di CBUFFER d3d11 \_**](/previous-versions/windows/desktop/legacy/ff476097(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a8549-109">[**D3D11\_CBUFFER\_TYPE**](/previous-versions/windows/desktop/legacy/ff476097(v=vs.85))</span></span><br/>                                  | <span data-ttu-id="a8549-110">Indica il tipo di un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="a8549-110">Indicates a constant buffer's type.</span></span><br/>                     |
| [<span data-ttu-id="a8549-111">**\_Flag di parametro D3D \_**</span><span class="sxs-lookup"><span data-stu-id="a8549-111">**D3D\_PARAMETER\_FLAGS**</span></span>](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_parameter_flags)<br/>                                | <span data-ttu-id="a8549-112">Indica i flag semantici per i parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="a8549-112">Indicates semantic flags for function parameters.</span></span><br/>       |
| [<span data-ttu-id="a8549-113">**\_ \_ Tipo restituito della risorsa d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="a8549-113">**D3D11\_RESOURCE\_RETURN\_TYPE**</span></span>](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_resource_return_type)<br/>                 | <span data-ttu-id="a8549-114">Indica il tipo di valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a8549-114">Indicates return value type.</span></span><br/>                            |
| [<span data-ttu-id="a8549-115">**\_Tipo di shader \_ d3d11**</span><span class="sxs-lookup"><span data-stu-id="a8549-115">**D3D11\_SHADER\_TYPE**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ne-d3d11shadertracing-d3d11_shader_type)<br/>                                    | <span data-ttu-id="a8549-116">Identifica un tipo di shader per la traccia.</span><span class="sxs-lookup"><span data-stu-id="a8549-116">Identifies a shader type for tracing.</span></span><br/>                   |
| [<span data-ttu-id="a8549-117">**\_ \_ Tipo di versione shader \_ d3d11**</span><span class="sxs-lookup"><span data-stu-id="a8549-117">**D3D11\_SHADER\_VERSION\_TYPE**</span></span>](/windows/desktop/api/d3d11shader/ne-d3d11shader-d3d11_shader_version_type)<br/>                   | <span data-ttu-id="a8549-118">Indica il tipo di shader.</span><span class="sxs-lookup"><span data-stu-id="a8549-118">Indicates shader type.</span></span><br/>                                  |
| [<span data-ttu-id="a8549-119">**\_Dominio mosaico \_ d3d11**</span><span class="sxs-lookup"><span data-stu-id="a8549-119">**D3D11\_TESSELLATOR\_DOMAIN**</span></span>](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_tessellator_domain)<br/>                      | <span data-ttu-id="a8549-120">Opzioni di dominio per i dati mosaico.</span><span class="sxs-lookup"><span data-stu-id="a8549-120">Domain options for tessellator data.</span></span><br/>                    |
| [<span data-ttu-id="a8549-121">**\_ \_ Partizionamento d3d11 mosaico**</span><span class="sxs-lookup"><span data-stu-id="a8549-121">**D3D11\_TESSELLATOR\_PARTITIONING**</span></span>](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_tessellator_partitioning)<br/>          | <span data-ttu-id="a8549-122">Opzioni di partizionamento.</span><span class="sxs-lookup"><span data-stu-id="a8549-122">Partitioning options.</span></span><br/>                                   |
| [<span data-ttu-id="a8549-123">**\_ \_ Primitiva output mosaico d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="a8549-123">**D3D11\_TESSELLATOR\_OUTPUT\_PRIMITIVE**</span></span>](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_tessellator_output_primitive)<br/> | <span data-ttu-id="a8549-124">Tipi primitivi di output.</span><span class="sxs-lookup"><span data-stu-id="a8549-124">Output primitive types.</span></span><br/>                                 |
| [<span data-ttu-id="a8549-125">**\_ \_ \_ Primitiva input GS traccia d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="a8549-125">**D3D11\_TRACE\_GS\_INPUT\_PRIMITIVE**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ne-d3d11shadertracing-d3d11_trace_gs_input_primitive)<br/>        | <span data-ttu-id="a8549-126">Identifica il tipo della primitiva di input geometry shader.</span><span class="sxs-lookup"><span data-stu-id="a8549-126">Identifies the type of geometry shader input primitive.</span></span><br/> |
| [<span data-ttu-id="a8549-127">**\_Tipo di \_ Registro di traccia d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="a8549-127">**D3D11\_TRACE\_REGISTER\_TYPE**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ne-d3d11shadertracing-d3d11_trace_register_type)<br/>                   | <span data-ttu-id="a8549-128">Identifica un tipo di registro di traccia.</span><span class="sxs-lookup"><span data-stu-id="a8549-128">Identifies a type of trace register.</span></span><br/>                    |



 

## <a name="related-topics"></a><span data-ttu-id="a8549-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8549-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8549-130">Riferimento shader</span><span class="sxs-lookup"><span data-stu-id="a8549-130">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

