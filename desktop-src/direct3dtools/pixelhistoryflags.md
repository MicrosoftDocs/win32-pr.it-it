---
description: Enumerazione contenente i flag utilizzati per descrivere il risultato di una cronologia pixel. Vedere PixelHistoryOperation.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione PIXELHISTORYFLAGS
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124158"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span data-ttu-id="332b6-104"><span id="vspixengine.pixelhistoryflags"></span>Enumerazione PIXELHISTORYFLAGS</span><span class="sxs-lookup"><span data-stu-id="332b6-104"><span id="vspixengine.pixelhistoryflags"></span>PIXELHISTORYFLAGS enumeration</span></span>

<span data-ttu-id="332b6-105">Enumerazione contenente i flag utilizzati per descrivere il risultato di una cronologia pixel.</span><span class="sxs-lookup"><span data-stu-id="332b6-105">An enum containing flags used to describe a pixel history result.</span></span> <span data-ttu-id="332b6-106">Vedere PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="332b6-106">See PixelHistoryOperation.</span></span>

## <a name="syntax"></a><span data-ttu-id="332b6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="332b6-107">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="332b6-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="332b6-108">Constants</span></span>

<span data-ttu-id="332b6-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**\_InitialValue PHF**</span><span class="sxs-lookup"><span data-stu-id="332b6-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF\_INITIALVALUE**</span></span>  
<span data-ttu-id="332b6-110">Flag che corrisponde al valore di colore iniziale (prima del frame).</span><span class="sxs-lookup"><span data-stu-id="332b6-110">A flag that corresponds to the initial color value (prior to frame).</span></span>

<span data-ttu-id="332b6-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="332b6-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF\_CLEAR**</span></span>  
<span data-ttu-id="332b6-112">Flag che corrisponde al risultato del colore non crittografato.</span><span class="sxs-lookup"><span data-stu-id="332b6-112">A flag that corresponds to the clear color result.</span></span>

<span data-ttu-id="332b6-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF- \_ disegni**</span><span class="sxs-lookup"><span data-stu-id="332b6-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF\_DRAW**</span></span>  
<span data-ttu-id="332b6-114">Flag che corrisponde al risultato del colore di traccia.</span><span class="sxs-lookup"><span data-stu-id="332b6-114">A flag that corresponds to the draw color result.</span></span>

<span data-ttu-id="332b6-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**\_FINALVALUE PHF**</span><span class="sxs-lookup"><span data-stu-id="332b6-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF\_FINALVALUE**</span></span>  
<span data-ttu-id="332b6-116">Flag che corrisponde al risultato del colore finale.</span><span class="sxs-lookup"><span data-stu-id="332b6-116">A flag that corresponds to the final color result.</span></span>

<span data-ttu-id="332b6-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**\_HASCOLOR PHF**</span><span class="sxs-lookup"><span data-stu-id="332b6-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF\_HASCOLOR**</span></span>  
<span data-ttu-id="332b6-118">Flag che corrisponde a se il risultato del colore è presente nello struct PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="332b6-118">A flag that corresponds to whether the color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="332b6-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**\_HASFBCOLOR PHF**</span><span class="sxs-lookup"><span data-stu-id="332b6-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF\_HASFBCOLOR**</span></span>  
<span data-ttu-id="332b6-120">Flag che corrisponde a se il risultato del colore del buffer finale è presente nello struct PixelHistoryOperation.</span><span class="sxs-lookup"><span data-stu-id="332b6-120">A flag that corresponds to whether the final buffer color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="332b6-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**\_errore PHF**</span><span class="sxs-lookup"><span data-stu-id="332b6-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**PHF\_ERROR**</span></span>  

<span data-ttu-id="332b6-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**\_VERTEXPROCESSINGSKIPPED PHF**</span><span class="sxs-lookup"><span data-stu-id="332b6-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF\_VERTEXPROCESSINGSKIPPED**</span></span>  
<span data-ttu-id="332b6-123">Non usato.</span><span class="sxs-lookup"><span data-stu-id="332b6-123">Not used.</span></span>

<span data-ttu-id="332b6-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**\_MODIFYRESOURCE PHF**</span><span class="sxs-lookup"><span data-stu-id="332b6-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF\_MODIFYRESOURCE**</span></span>  

<span data-ttu-id="332b6-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**\_CANNOTRUNFULLDEPTHSTENCILTEST PHF**</span><span class="sxs-lookup"><span data-stu-id="332b6-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF\_CANNOTRUNFULLDEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="332b6-126">Flag che corrisponde a non essere in grado di eseguire il test di profondità o stencil.</span><span class="sxs-lookup"><span data-stu-id="332b6-126">A flag that corresponds to not being able to run the depth or stencil test.</span></span>

## <a name="requirements"></a><span data-ttu-id="332b6-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="332b6-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="332b6-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="332b6-128">Header</span></span></p></td><td><span data-ttu-id="332b6-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="332b6-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



