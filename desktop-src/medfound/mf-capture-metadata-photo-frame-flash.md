---
description: Indica se è stato attivato un flash per il frame acquisito.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: Attributo MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309575"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a><span data-ttu-id="b1e58-103">\_ \_ \_ \_ Attributo fotogramma Flash per \_ l'acquisizione di metadati MF</span><span class="sxs-lookup"><span data-stu-id="b1e58-103">MF\_CAPTURE\_METADATA\_PHOTO\_FRAME\_FLASH attribute</span></span>

<span data-ttu-id="b1e58-104">Indica se è stato attivato un flash per il frame acquisito.</span><span class="sxs-lookup"><span data-stu-id="b1e58-104">Indicates if a flash was triggered for the captured frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1e58-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b1e58-105">Data type</span></span>

<span data-ttu-id="b1e58-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b1e58-106">**UINT32**</span></span>



| <span data-ttu-id="b1e58-107">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e58-107">Value</span></span>                                                                               | <span data-ttu-id="b1e58-108">Significato</span><span class="sxs-lookup"><span data-stu-id="b1e58-108">Meaning</span></span>                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1e58-109"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b1e58-109"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="b1e58-110">Un flash non è stato attivato in questo frame.</span><span class="sxs-lookup"><span data-stu-id="b1e58-110">A flash was not triggered on this frame.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="b1e58-111"><dt>non zero</dt></span><span class="sxs-lookup"><span data-stu-id="b1e58-111"><dt>non-zero</dt></span></span> </dl> | <span data-ttu-id="b1e58-112">Un flash è stato attivato su questo frame.</span><span class="sxs-lookup"><span data-stu-id="b1e58-112">A flash was triggered on this frame.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="b1e58-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b1e58-113"><dt>1</dt></span></span> </dl>        | <span data-ttu-id="b1e58-114">Riservato</span><span class="sxs-lookup"><span data-stu-id="b1e58-114">Reserved</span></span><br/> <span data-ttu-id="b1e58-115">Non verificare in modo esplicito il valore 1.</span><span class="sxs-lookup"><span data-stu-id="b1e58-115">Do not explicitly check for a value of 1.</span></span> <span data-ttu-id="b1e58-116">Le applicazioni devono verificare solo! = 0 per indicare se è stato attivato un flash.</span><span class="sxs-lookup"><span data-stu-id="b1e58-116">Applications should only check for !=0 to indicate if a flash was triggered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b1e58-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1e58-117">Requirements</span></span>



| <span data-ttu-id="b1e58-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1e58-118">Requirement</span></span> | <span data-ttu-id="b1e58-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e58-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e58-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1e58-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b1e58-121">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1e58-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b1e58-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1e58-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b1e58-123">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1e58-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b1e58-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1e58-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1e58-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1e58-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1e58-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1e58-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e58-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b1e58-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




