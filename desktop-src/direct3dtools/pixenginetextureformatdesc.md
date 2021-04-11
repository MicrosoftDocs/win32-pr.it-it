---
description: Rappresenta una descrizione di un formato di trama.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PixEngineTextureFormatDesc
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965717"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span data-ttu-id="37710-103"><span id="vspixengine.pixenginetextureformatdesc"></span>Struttura PixEngineTextureFormatDesc</span><span class="sxs-lookup"><span data-stu-id="37710-103"><span id="vspixengine.pixenginetextureformatdesc"></span>PixEngineTextureFormatDesc structure</span></span>

<span data-ttu-id="37710-104">Rappresenta una descrizione di un formato di trama.</span><span class="sxs-lookup"><span data-stu-id="37710-104">Represents a description of a texture format.</span></span>

## <a name="syntax"></a><span data-ttu-id="37710-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37710-105">Syntax</span></span>


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a><span data-ttu-id="37710-106">Members</span><span class="sxs-lookup"><span data-stu-id="37710-106">Members</span></span>

<span data-ttu-id="37710-107">**dxgiFormat**</span><span class="sxs-lookup"><span data-stu-id="37710-107">**dxgiFormat**</span></span>  
<span data-ttu-id="37710-108">Formato DXGI della trama.</span><span class="sxs-lookup"><span data-stu-id="37710-108">The DXGI format of the texture.</span></span>

<span data-ttu-id="37710-109">**dataFormat**</span><span class="sxs-lookup"><span data-stu-id="37710-109">**dataFormat**</span></span>  
<span data-ttu-id="37710-110">Formato dati della trama.</span><span class="sxs-lookup"><span data-stu-id="37710-110">The data format of the texture.</span></span>

<span data-ttu-id="37710-111">**blockBytes**</span><span class="sxs-lookup"><span data-stu-id="37710-111">**blockBytes**</span></span>  
<span data-ttu-id="37710-112">Numero di byte in un blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="37710-112">The number of bytes in a data block.</span></span>

<span data-ttu-id="37710-113">**blockHeight**</span><span class="sxs-lookup"><span data-stu-id="37710-113">**blockHeight**</span></span>  
<span data-ttu-id="37710-114">Altezza (esempi di numero nell'asse Y) del blocco.</span><span class="sxs-lookup"><span data-stu-id="37710-114">The height (number samples in the Y axis) of the block.</span></span>

<span data-ttu-id="37710-115">**blockWidth**</span><span class="sxs-lookup"><span data-stu-id="37710-115">**blockWidth**</span></span>  
<span data-ttu-id="37710-116">Larghezza (numero di campioni nell'asse X) del blocco.</span><span class="sxs-lookup"><span data-stu-id="37710-116">The width (number of samples in the X axis) of the block.</span></span>

<span data-ttu-id="37710-117">**channelX**</span><span class="sxs-lookup"><span data-stu-id="37710-117">**channelX**</span></span>  
<span data-ttu-id="37710-118">Descrive le proprietà del canale X.</span><span class="sxs-lookup"><span data-stu-id="37710-118">Describes properties of the X channel.</span></span> <span data-ttu-id="37710-119">Per ulteriori informazioni, vedere la struttura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="37710-119">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="37710-120">**canale**</span><span class="sxs-lookup"><span data-stu-id="37710-120">**channelY**</span></span>  
<span data-ttu-id="37710-121">Descrive le proprietà del canale Y.</span><span class="sxs-lookup"><span data-stu-id="37710-121">Describes properties of the Y channel.</span></span> <span data-ttu-id="37710-122">Per ulteriori informazioni, vedere la struttura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="37710-122">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="37710-123">**channelZ**</span><span class="sxs-lookup"><span data-stu-id="37710-123">**channelZ**</span></span>  
<span data-ttu-id="37710-124">Descrive le proprietà del canale Z.</span><span class="sxs-lookup"><span data-stu-id="37710-124">Describes properties of the Z channel.</span></span> <span data-ttu-id="37710-125">Per ulteriori informazioni, vedere la struttura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="37710-125">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="37710-126">**channelW**</span><span class="sxs-lookup"><span data-stu-id="37710-126">**channelW**</span></span>  
<span data-ttu-id="37710-127">Descrive le proprietà del canale W.</span><span class="sxs-lookup"><span data-stu-id="37710-127">Describes properties of the W channel.</span></span> <span data-ttu-id="37710-128">Per ulteriori informazioni, vedere la struttura PixEngineChannelDescription.</span><span class="sxs-lookup"><span data-stu-id="37710-128">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="37710-129">**swizzle**</span><span class="sxs-lookup"><span data-stu-id="37710-129">**swizzle**</span></span>  
<span data-ttu-id="37710-130">Viene descritto il swizzle (swapping del canale) applicato all'esempio.</span><span class="sxs-lookup"><span data-stu-id="37710-130">Describes the swizzle (channel-swapping) applied to the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="37710-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37710-131">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="37710-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37710-132">Header</span></span></p></td><td><span data-ttu-id="37710-133">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="37710-133">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



