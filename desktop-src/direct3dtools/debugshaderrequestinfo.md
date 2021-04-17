---
description: Rappresenta le informazioni su una richiesta del debugger shader.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura DebugShaderRequestInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a59bfb84bb7d4e8644c0cfadc4475be7d7da4a54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521586"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span data-ttu-id="a5d25-103"><span id="vspixengine.debugshaderrequestinfo"></span>Struttura DebugShaderRequestInfo</span><span class="sxs-lookup"><span data-stu-id="a5d25-103"><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo structure</span></span>

<span data-ttu-id="a5d25-104">Rappresenta le informazioni su una richiesta del debugger shader.</span><span class="sxs-lookup"><span data-stu-id="a5d25-104">Represents information about a shader debugger request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d25-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5d25-105">Syntax</span></span>


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a><span data-ttu-id="a5d25-106">Members</span><span class="sxs-lookup"><span data-stu-id="a5d25-106">Members</span></span>

<span data-ttu-id="a5d25-107">**fase**</span><span class="sxs-lookup"><span data-stu-id="a5d25-107">**stage**</span></span>  
<span data-ttu-id="a5d25-108">Fase della pipeline di cui eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="a5d25-108">The pipeline stage to debug.</span></span>

<span data-ttu-id="a5d25-109">**eventID**</span><span class="sxs-lookup"><span data-stu-id="a5d25-109">**eventID**</span></span>  
<span data-ttu-id="a5d25-110">ID dell'evento di grafica di cui eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="a5d25-110">The ID of the graphics event to debug.</span></span>

<span data-ttu-id="a5d25-111">**NumeroFrame**</span><span class="sxs-lookup"><span data-stu-id="a5d25-111">**frameNumber**</span></span>  
<span data-ttu-id="a5d25-112">Frame di cui eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="a5d25-112">The frame to debug.</span></span>

<span data-ttu-id="a5d25-113">**vertice**</span><span class="sxs-lookup"><span data-stu-id="a5d25-113">**vertex**</span></span>  
<span data-ttu-id="a5d25-114">Vertice di cui eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="a5d25-114">The vertex to debug.</span></span>

<span data-ttu-id="a5d25-115">**pixel**</span><span class="sxs-lookup"><span data-stu-id="a5d25-115">**pixel**</span></span>  
<span data-ttu-id="a5d25-116">Pixel di cui eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="a5d25-116">The pixel to debug.</span></span>

<span data-ttu-id="a5d25-117">**groupCoordinates**</span><span class="sxs-lookup"><span data-stu-id="a5d25-117">**groupCoordinates**</span></span>  
<span data-ttu-id="a5d25-118">Coordinate del gruppo di cui eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="a5d25-118">The coordinates of the group to debug.</span></span>

<span data-ttu-id="a5d25-119">**threadCoordinates**</span><span class="sxs-lookup"><span data-stu-id="a5d25-119">**threadCoordinates**</span></span>  
<span data-ttu-id="a5d25-120">Coordinate del thread di cui eseguire il debug</span><span class="sxs-lookup"><span data-stu-id="a5d25-120">The coordinates of the thread to debug</span></span>

## <a name="requirements"></a><span data-ttu-id="a5d25-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5d25-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a5d25-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5d25-122">Header</span></span></p></td><td><span data-ttu-id="a5d25-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a5d25-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



