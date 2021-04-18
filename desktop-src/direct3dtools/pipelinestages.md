---
description: Enumerazione utilizzata per indicare una fase della pipeline grafica.
MS-HAID: vspixengine.PIPELINESTAGES
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione PIPELINESTAGES
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AF40441A-8027-4028-9A02-D53754FD2596
api_name:
- PIPELINESTAGES
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11f52f62815228e459bed06d369fa6479d2b0e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304288"
---
# <a name="span-idvspixenginepipelinestagesspanpipelinestages-enumeration"></a><span data-ttu-id="7ee5b-103"><span id="vspixengine.pipelinestages"></span>Enumerazione PIPELINESTAGES</span><span class="sxs-lookup"><span data-stu-id="7ee5b-103"><span id="vspixengine.pipelinestages"></span>PIPELINESTAGES enumeration</span></span>

<span data-ttu-id="7ee5b-104">Enumerazione utilizzata per indicare una fase della pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-104">An enum used to indicate a stage of the graphics pipeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ee5b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ee5b-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="7ee5b-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="7ee5b-106">Constants</span></span>

<span data-ttu-id="7ee5b-107"><span id="PipeLineStages_InputAssembler"></span><span id="pipelinestages_inputassembler"></span><span id="PIPELINESTAGES_INPUTASSEMBLER"></span>**\_InputAssembler PipeLineStages**</span><span class="sxs-lookup"><span data-stu-id="7ee5b-107"><span id="PipeLineStages_InputAssembler"></span><span id="pipelinestages_inputassembler"></span><span id="PIPELINESTAGES_INPUTASSEMBLER"></span>**PipeLineStages\_InputAssembler**</span></span>  
<span data-ttu-id="7ee5b-108">Valore che corrisponde alla fase dell'assembler di input.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-108">A value that corresponds to the Input Assembler stage.</span></span>

<span data-ttu-id="7ee5b-109"><span id="PipeLineStages_VertexShader"></span><span id="pipelinestages_vertexshader"></span><span id="PIPELINESTAGES_VERTEXSHADER"></span>**\_Vertexshader PipeLineStages**</span><span class="sxs-lookup"><span data-stu-id="7ee5b-109"><span id="PipeLineStages_VertexShader"></span><span id="pipelinestages_vertexshader"></span><span id="PIPELINESTAGES_VERTEXSHADER"></span>**PipeLineStages\_VertexShader**</span></span>  
<span data-ttu-id="7ee5b-110">Valore che corrisponde alla fase vertex shader.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-110">A value that corresponds to the Vertex Shader stage.</span></span>

<span data-ttu-id="7ee5b-111"><span id="PipeLineStages_HullShader"></span><span id="pipelinestages_hullshader"></span><span id="PIPELINESTAGES_HULLSHADER"></span>**\_HullShader PipeLineStages**</span><span class="sxs-lookup"><span data-stu-id="7ee5b-111"><span id="PipeLineStages_HullShader"></span><span id="pipelinestages_hullshader"></span><span id="PIPELINESTAGES_HULLSHADER"></span>**PipeLineStages\_HullShader**</span></span>  
<span data-ttu-id="7ee5b-112">Valore che corrisponde alla fase Hull shader.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-112">A value that corresponds to the Hull Shader stage.</span></span>

<span data-ttu-id="7ee5b-113"><span id="PipeLineStages_Tesselator"></span><span id="pipelinestages_tesselator"></span><span id="PIPELINESTAGES_TESSELATOR"></span>**\_Tesselator PipeLineStages**</span><span class="sxs-lookup"><span data-stu-id="7ee5b-113"><span id="PipeLineStages_Tesselator"></span><span id="pipelinestages_tesselator"></span><span id="PIPELINESTAGES_TESSELATOR"></span>**PipeLineStages\_Tesselator**</span></span>  
<span data-ttu-id="7ee5b-114">Valore che corrisponde alla fase Tesselator.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-114">A value that corresponds to the Tesselator stage.</span></span>

<span data-ttu-id="7ee5b-115"><span id="PipeLineStages_DomainShader"></span><span id="pipelinestages_domainshader"></span><span id="PIPELINESTAGES_DOMAINSHADER"></span>**\_DomainShader PipeLineStages**</span><span class="sxs-lookup"><span data-stu-id="7ee5b-115"><span id="PipeLineStages_DomainShader"></span><span id="pipelinestages_domainshader"></span><span id="PIPELINESTAGES_DOMAINSHADER"></span>**PipeLineStages\_DomainShader**</span></span>  
<span data-ttu-id="7ee5b-116">Valore che corrisponde alla fase del Domain shader.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-116">A value that corresponds to the Domain Shader stage.</span></span>

<span data-ttu-id="7ee5b-117"><span id="PipeLineStages_GeometryShader"></span><span id="pipelinestages_geometryshader"></span><span id="PIPELINESTAGES_GEOMETRYSHADER"></span>**\_GeometryShader PipeLineStages**</span><span class="sxs-lookup"><span data-stu-id="7ee5b-117"><span id="PipeLineStages_GeometryShader"></span><span id="pipelinestages_geometryshader"></span><span id="PIPELINESTAGES_GEOMETRYSHADER"></span>**PipeLineStages\_GeometryShader**</span></span>  
<span data-ttu-id="7ee5b-118">Valore che corrisponde alla fase geometry shader.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-118">A value that corresponds to the Geometry Shader stage.</span></span>

<span data-ttu-id="7ee5b-119"><span id="PipeLineStages_StreamOutput"></span><span id="pipelinestages_streamoutput"></span><span id="PIPELINESTAGES_STREAMOUTPUT"></span>**\_StreamOutput PipeLineStages**</span><span class="sxs-lookup"><span data-stu-id="7ee5b-119"><span id="PipeLineStages_StreamOutput"></span><span id="pipelinestages_streamoutput"></span><span id="PIPELINESTAGES_STREAMOUTPUT"></span>**PipeLineStages\_StreamOutput**</span></span>  
<span data-ttu-id="7ee5b-120">Valore che corrisponde alla fase di output del flusso.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-120">A value that corresponds to the Stream Output stage.</span></span>

<span data-ttu-id="7ee5b-121"><span id="PipeLineStages_Rasterizer"></span><span id="pipelinestages_rasterizer"></span><span id="PIPELINESTAGES_RASTERIZER"></span>**\_Rasterizzatore PipeLineStages**</span><span class="sxs-lookup"><span data-stu-id="7ee5b-121"><span id="PipeLineStages_Rasterizer"></span><span id="pipelinestages_rasterizer"></span><span id="PIPELINESTAGES_RASTERIZER"></span>**PipeLineStages\_Rasterizer**</span></span>  
<span data-ttu-id="7ee5b-122">Valore che corrisponde alla fase di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-122">A value that corresponds to the Rasterizer stage.</span></span>

<span data-ttu-id="7ee5b-123"><span id="PipeLineStages_PixelShader"></span><span id="pipelinestages_pixelshader"></span><span id="PIPELINESTAGES_PIXELSHADER"></span>**\_PixelShader PipeLineStages**</span><span class="sxs-lookup"><span data-stu-id="7ee5b-123"><span id="PipeLineStages_PixelShader"></span><span id="pipelinestages_pixelshader"></span><span id="PIPELINESTAGES_PIXELSHADER"></span>**PipeLineStages\_PixelShader**</span></span>  
<span data-ttu-id="7ee5b-124">Valore che corrisponde alla fase del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-124">A value that corresponds to the Pixel Shader stage.</span></span>

<span data-ttu-id="7ee5b-125"><span id="PipeLineStages_OutputMerger"></span><span id="pipelinestages_outputmerger"></span><span id="PIPELINESTAGES_OUTPUTMERGER"></span>**\_OutputMerger PipeLineStages**</span><span class="sxs-lookup"><span data-stu-id="7ee5b-125"><span id="PipeLineStages_OutputMerger"></span><span id="pipelinestages_outputmerger"></span><span id="PIPELINESTAGES_OUTPUTMERGER"></span>**PipeLineStages\_OutputMerger**</span></span>  
<span data-ttu-id="7ee5b-126">Valore che corrisponde alla fase di Unione dell'output.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-126">A value that corresponds to the Output Merger stage.</span></span>

<span data-ttu-id="7ee5b-127"><span id="PipeLineStages_ComputeShader"></span><span id="pipelinestages_computeshader"></span><span id="PIPELINESTAGES_COMPUTESHADER"></span>**\_ComputeShader PipeLineStages**</span><span class="sxs-lookup"><span data-stu-id="7ee5b-127"><span id="PipeLineStages_ComputeShader"></span><span id="pipelinestages_computeshader"></span><span id="PIPELINESTAGES_COMPUTESHADER"></span>**PipeLineStages\_ComputeShader**</span></span>  
<span data-ttu-id="7ee5b-128">Valore che corrisponde alla fase compute shader.</span><span class="sxs-lookup"><span data-stu-id="7ee5b-128">A value that corresponds to the Compute Shader stage.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ee5b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ee5b-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7ee5b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ee5b-130">Header</span></span></p></td><td><span data-ttu-id="7ee5b-131">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7ee5b-131">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



