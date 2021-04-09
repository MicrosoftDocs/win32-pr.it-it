---
description: Rappresenta una fase della pipeline, inclusi i dettagli dello shader utilizzato.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PipeLineStage
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965627"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span data-ttu-id="bda57-103"><span id="vspixengine.pipelinestage"></span>Struttura PipeLineStage</span><span class="sxs-lookup"><span data-stu-id="bda57-103"><span id="vspixengine.pipelinestage"></span>PipeLineStage structure</span></span>

<span data-ttu-id="bda57-104">Rappresenta una fase della pipeline, inclusi i dettagli dello shader utilizzato.</span><span class="sxs-lookup"><span data-stu-id="bda57-104">Represents a pipeline stage, including details of the shader used.</span></span>

## <a name="syntax"></a><span data-ttu-id="bda57-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bda57-105">Syntax</span></span>


```C++
} PipeLineStage;
```

## <a name="members"></a><span data-ttu-id="bda57-106">Members</span><span class="sxs-lookup"><span data-stu-id="bda57-106">Members</span></span>

<span data-ttu-id="bda57-107">**StageId**</span><span class="sxs-lookup"><span data-stu-id="bda57-107">**StageId**</span></span>  
<span data-ttu-id="bda57-108">ID della fase della pipeline.</span><span class="sxs-lookup"><span data-stu-id="bda57-108">The ID of the pipeline stage.</span></span>

<span data-ttu-id="bda57-109">**Debuggable**</span><span class="sxs-lookup"><span data-stu-id="bda57-109">**Debuggable**</span></span>  
<span data-ttu-id="bda57-110">true se la fase della pipeline supporta il debug; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="bda57-110">true if the pipeline stage supports debugging; otherwise, false.</span></span>

<span data-ttu-id="bda57-111">**StageName**</span><span class="sxs-lookup"><span data-stu-id="bda57-111">**StageName**</span></span>  
<span data-ttu-id="bda57-112">Stringa COM contenente il nome della fase della pipeline.</span><span class="sxs-lookup"><span data-stu-id="bda57-112">A COM string containing the name of the pipeline stage.</span></span>

<span data-ttu-id="bda57-113">**GuaranteedOutput**</span><span class="sxs-lookup"><span data-stu-id="bda57-113">**GuaranteedOutput**</span></span>  
<span data-ttu-id="bda57-114">true se la fase della pipeline contiene sempre l'output della pipeline. in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="bda57-114">true if the pipeline stage always has pipeline output; otherwise, false.</span></span>

<span data-ttu-id="bda57-115">**DebugEntryPoint**</span><span class="sxs-lookup"><span data-stu-id="bda57-115">**DebugEntryPoint**</span></span>  
<span data-ttu-id="bda57-116">Stringa COM contenente il nome del punto di ingresso dello shader, se presente.</span><span class="sxs-lookup"><span data-stu-id="bda57-116">A COM string containing the name of the shader entry point, if there is one.</span></span>

<span data-ttu-id="bda57-117">**ShaderFile**</span><span class="sxs-lookup"><span data-stu-id="bda57-117">**ShaderFile**</span></span>  
<span data-ttu-id="bda57-118">Stringa COM contenente il percorso del file di origine dello shader.</span><span class="sxs-lookup"><span data-stu-id="bda57-118">A COM string containing the filepath of the shader source file.</span></span>

<span data-ttu-id="bda57-119">**ShaderByteStreamPtr**</span><span class="sxs-lookup"><span data-stu-id="bda57-119">**ShaderByteStreamPtr**</span></span>  
<span data-ttu-id="bda57-120">FILEPTR per il flusso di byte dello shader.</span><span class="sxs-lookup"><span data-stu-id="bda57-120">A FILEPTR for the shader byte stream.</span></span> <span data-ttu-id="bda57-121">Questa operazione viene passata di nuovo per eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="bda57-121">This is passed back in order to debug.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda57-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bda57-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="bda57-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bda57-123">Header</span></span></p></td><td><span data-ttu-id="bda57-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="bda57-124">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



