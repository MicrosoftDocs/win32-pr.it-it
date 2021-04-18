---
description: Rappresenta le informazioni su un particolare oggetto.
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PixelHistoryIntersection
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304334"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span data-ttu-id="3b899-103"><span id="vspixengine.pixelhistoryintersection"></span>Struttura PixelHistoryIntersection</span><span class="sxs-lookup"><span data-stu-id="3b899-103"><span id="vspixengine.pixelhistoryintersection"></span>PixelHistoryIntersection structure</span></span>

<span data-ttu-id="3b899-104">Rappresenta le informazioni su un determinato oggetto</span><span class="sxs-lookup"><span data-stu-id="3b899-104">Represents information about a particular</span></span>

## <a name="syntax"></a><span data-ttu-id="3b899-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b899-105">Syntax</span></span>


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a><span data-ttu-id="3b899-106">Members</span><span class="sxs-lookup"><span data-stu-id="3b899-106">Members</span></span>

<span data-ttu-id="3b899-107">**NumeroFrame**</span><span class="sxs-lookup"><span data-stu-id="3b899-107">**frameNumber**</span></span>  
<span data-ttu-id="3b899-108">Frame dell'evento graphics associata con questa operazione.</span><span class="sxs-lookup"><span data-stu-id="3b899-108">The frame of the graphics event assocaited with this operation.</span></span>

<span data-ttu-id="3b899-109">**Eid**</span><span class="sxs-lookup"><span data-stu-id="3b899-109">**eid**</span></span>  
<span data-ttu-id="3b899-110">ID dell'evento di grafica associato a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="3b899-110">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="3b899-111">**renderTargetPtr**</span><span class="sxs-lookup"><span data-stu-id="3b899-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="3b899-112">Destinazione di rendering originariamente associata (all'interno dell'applicazione acquisita) con questa operazione.</span><span class="sxs-lookup"><span data-stu-id="3b899-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="3b899-113">**eventType**</span><span class="sxs-lookup"><span data-stu-id="3b899-113">**eventType**</span></span>  
<span data-ttu-id="3b899-114">Tipo di evento associato a questa operazione (in particolare, se l'evento è una chiamata di tipo di progetto).</span><span class="sxs-lookup"><span data-stu-id="3b899-114">The kind of event associated with this operation (specifically, whether this event is a draw call).</span></span>

<span data-ttu-id="3b899-115">**punto**</span><span class="sxs-lookup"><span data-stu-id="3b899-115">**point**</span></span>  
<span data-ttu-id="3b899-116">Coordinate del pixel nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="3b899-116">The coordinates of the pixel in the framebuffer.</span></span>

<span data-ttu-id="3b899-117">**bAssemblerStageGeneratesInstanceID**</span><span class="sxs-lookup"><span data-stu-id="3b899-117">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="3b899-118">true se l'assembler di input genera gli ID istanza; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="3b899-118">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="3b899-119">**flags**</span><span class="sxs-lookup"><span data-stu-id="3b899-119">**flags**</span></span>  
<span data-ttu-id="3b899-120">Combinazione di valori PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="3b899-120">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="3b899-121">Per ulteriori informazioni, vedere l'enumerazione PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="3b899-121">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="3b899-122">**fbInitialRed**</span><span class="sxs-lookup"><span data-stu-id="3b899-122">**fbInitialRed**</span></span>  
<span data-ttu-id="3b899-123">Framebuffer: valore del componente colore rosso del framebuffer prima che venga eseguito il merge di qualsiasi pixel shader output; ovvero all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="3b899-123">Framebuffer: value of red color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="3b899-124">**fbInitialGreen**</span><span class="sxs-lookup"><span data-stu-id="3b899-124">**fbInitialGreen**</span></span>  
<span data-ttu-id="3b899-125">Framebuffer: valore del componente colore verde del framebuffer prima dell'Unione di qualsiasi pixel shader output; ovvero all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="3b899-125">Framebuffer: value of green color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="3b899-126">**fbInitialBlue**</span><span class="sxs-lookup"><span data-stu-id="3b899-126">**fbInitialBlue**</span></span>  
<span data-ttu-id="3b899-127">Framebuffer: valore del componente colore blu del framebuffer prima che venga eseguito il merge di qualsiasi pixel shader output; ovvero all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="3b899-127">Framebuffer: value of blue color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="3b899-128">**fbInitialAlpha**</span><span class="sxs-lookup"><span data-stu-id="3b899-128">**fbInitialAlpha**</span></span>  
<span data-ttu-id="3b899-129">Framebuffer: valore del componente a colori alfa del framebuffer prima dell'Unione di qualsiasi pixel shader output; ovvero all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="3b899-129">Framebuffer: value of alpha color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="3b899-130">**LabelFBInitialRed**</span><span class="sxs-lookup"><span data-stu-id="3b899-130">**LabelFBInitialRed**</span></span>  
<span data-ttu-id="3b899-131">Stringa COM contenente il nome dell'etichetta associata al componente colore rosso del framebuffer prima di qualsiasi ombreggiatura dei pixel; ovvero all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="3b899-131">A COM string containing the name of the label associated with the red color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="3b899-132">**LabelFBInitialGreen**</span><span class="sxs-lookup"><span data-stu-id="3b899-132">**LabelFBInitialGreen**</span></span>  
<span data-ttu-id="3b899-133">Stringa COM contenente il nome dell'etichetta associata al componente colore verde del framebuffer prima di qualsiasi ombreggiatura dei pixel; ovvero all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="3b899-133">A COM string containing the name of the label associated with the green color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="3b899-134">**LabelFBInitialBlue**</span><span class="sxs-lookup"><span data-stu-id="3b899-134">**LabelFBInitialBlue**</span></span>  
<span data-ttu-id="3b899-135">Stringa COM contenente il nome dell'etichetta associata al componente colore blu del framebuffer prima di qualsiasi ombreggiatura dei pixel; ovvero all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="3b899-135">A COM string containing the name of the label associated with the blue color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="3b899-136">**LabelFBInitialAlpha**</span><span class="sxs-lookup"><span data-stu-id="3b899-136">**LabelFBInitialAlpha**</span></span>  
<span data-ttu-id="3b899-137">Stringa COM contenente il nome dell'etichetta associata al componente colore alfa del framebuffer prima di qualsiasi ombreggiatura dei pixel; ovvero all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="3b899-137">A COM string containing the name of the label associated with the alpha color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="3b899-138">**fbRed**</span><span class="sxs-lookup"><span data-stu-id="3b899-138">**fbRed**</span></span>  
<span data-ttu-id="3b899-139">Framebuffer: valore del componente colore rosso del framebuffer dopo l'Unione di tutti i pixel shader output; ovvero il colore del framebuffer finale.</span><span class="sxs-lookup"><span data-stu-id="3b899-139">Framebuffer: value of red color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="3b899-140">**fbGreen**</span><span class="sxs-lookup"><span data-stu-id="3b899-140">**fbGreen**</span></span>  
<span data-ttu-id="3b899-141">Framebuffer: valore del componente colore verde del framebuffer dopo l'Unione di tutti i pixel shader output; ovvero il colore del framebuffer finale.</span><span class="sxs-lookup"><span data-stu-id="3b899-141">Framebuffer: value of green color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="3b899-142">**fbBlue**</span><span class="sxs-lookup"><span data-stu-id="3b899-142">**fbBlue**</span></span>  
<span data-ttu-id="3b899-143">Framebuffer: valore del componente colore blu del framebuffer dopo l'Unione di tutti i pixel shader output; ovvero il colore del framebuffer finale.</span><span class="sxs-lookup"><span data-stu-id="3b899-143">Framebuffer: value of blue color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="3b899-144">**fbAlpha**</span><span class="sxs-lookup"><span data-stu-id="3b899-144">**fbAlpha**</span></span>  
<span data-ttu-id="3b899-145">Framebuffer: valore del componente a colori alfa del framebuffer dopo l'Unione di tutti i pixel shader output; ovvero il colore del framebuffer finale.</span><span class="sxs-lookup"><span data-stu-id="3b899-145">Framebuffer: value of alpha color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="3b899-146">**LabelFBRed**</span><span class="sxs-lookup"><span data-stu-id="3b899-146">**LabelFBRed**</span></span>  
<span data-ttu-id="3b899-147">Stringa COM contenente il nome dell'etichetta associata al componente colore rosso del framebuffer dopo l'ombreggiatura di tutti i pixel; ovvero il colore del framebuffer finale.</span><span class="sxs-lookup"><span data-stu-id="3b899-147">A COM string containing the name of the label associated with the red color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="3b899-148">**LabelFBGreen**</span><span class="sxs-lookup"><span data-stu-id="3b899-148">**LabelFBGreen**</span></span>  
<span data-ttu-id="3b899-149">Stringa COM contenente il nome dell'etichetta associata al componente colore verde del framebuffer dopo l'ombreggiatura di tutti i pixel; ovvero il colore del framebuffer finale.</span><span class="sxs-lookup"><span data-stu-id="3b899-149">A COM string containing the name of the label associated with the green color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="3b899-150">**LabelFBBlue**</span><span class="sxs-lookup"><span data-stu-id="3b899-150">**LabelFBBlue**</span></span>  
<span data-ttu-id="3b899-151">Stringa COM contenente il nome dell'etichetta associata al componente colore blu del framebuffer dopo l'ombreggiatura di tutti i pixel; ovvero il colore del framebuffer finale.</span><span class="sxs-lookup"><span data-stu-id="3b899-151">A COM string containing the name of the label associated with the blue color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="3b899-152">**LabelFBAlpha**</span><span class="sxs-lookup"><span data-stu-id="3b899-152">**LabelFBAlpha**</span></span>  
<span data-ttu-id="3b899-153">Stringa COM contenente il nome dell'etichetta associata al componente colore alfa del framebuffer dopo l'ombreggiatura di tutti i pixel; ovvero il colore del framebuffer finale.</span><span class="sxs-lookup"><span data-stu-id="3b899-153">A COM string containing the name of the label associated with the alpha color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="3b899-154">**pixelKillReason**</span><span class="sxs-lookup"><span data-stu-id="3b899-154">**pixelKillReason**</span></span>  
<span data-ttu-id="3b899-155">Specifica il motivo per cui il contributo di colore del pixel è stato terminato.</span><span class="sxs-lookup"><span data-stu-id="3b899-155">Specifies the reason that the pixel's color contribution was killed.</span></span>

<span data-ttu-id="3b899-156">**HResult**</span><span class="sxs-lookup"><span data-stu-id="3b899-156">**HResult**</span></span>  
<span data-ttu-id="3b899-157">Se si è verificato un errore, contiene il valore HRESULT di DirectX che specifica l'errore.</span><span class="sxs-lookup"><span data-stu-id="3b899-157">If an error occurred, contains the DirectX HRESULT that specifies the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b899-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b899-158">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3b899-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b899-159">Header</span></span></p></td><td><span data-ttu-id="3b899-160">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3b899-160">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



