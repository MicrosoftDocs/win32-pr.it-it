---
description: Il decodificatore video Media Foundation DV è una trasformazione Media Foundation che decodifica il video DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Decoder video DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749258"
---
# <a name="dv-video-decoder"></a><span data-ttu-id="f98d1-103">Decoder video DV</span><span class="sxs-lookup"><span data-stu-id="f98d1-103">DV Video Decoder</span></span>

<span data-ttu-id="f98d1-104">Il decodificatore video Media Foundation DV è una [trasformazione Media Foundation](media-foundation-transforms.md) che decodifica il video DV.</span><span class="sxs-lookup"><span data-stu-id="f98d1-104">The Media Foundation DV video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes DV video.</span></span>

<span data-ttu-id="f98d1-105">Il decodificatore video DV supporta i tipi di input seguenti:</span><span class="sxs-lookup"><span data-stu-id="f98d1-105">The DV video decoder supports the following input types:</span></span>



| <span data-ttu-id="f98d1-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="f98d1-106">Subtype</span></span>                 | <span data-ttu-id="f98d1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f98d1-107">Description</span></span>                  |
|-------------------------|------------------------------|
| <span data-ttu-id="f98d1-108">**\_DVC MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="f98d1-108">**MFVideoFormat\_DVC**</span></span>  | <span data-ttu-id="f98d1-109">Video su DVC/DV</span><span class="sxs-lookup"><span data-stu-id="f98d1-109">DVC/DV Video</span></span>                 |
| <span data-ttu-id="f98d1-110">**\_DVHD MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="f98d1-110">**MFVideoFormat\_DVHD**</span></span> | <span data-ttu-id="f98d1-111">HD-DVCR (1125-60 o 1250-50)</span><span class="sxs-lookup"><span data-stu-id="f98d1-111">HD-DVCR (1125-60 or 1250-50)</span></span> |
| <span data-ttu-id="f98d1-112">**\_DVSD MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="f98d1-112">**MFVideoFormat\_DVSD**</span></span> | <span data-ttu-id="f98d1-113">SDL-DVCR (525-60 o 625-50)</span><span class="sxs-lookup"><span data-stu-id="f98d1-113">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="f98d1-114">**\_DVSL MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="f98d1-114">**MFVideoFormat\_DVSL**</span></span> | <span data-ttu-id="f98d1-115">SD-DVCR (525-60 o 625-50)</span><span class="sxs-lookup"><span data-stu-id="f98d1-115">SD-DVCR (525-60 or 625-50)</span></span>   |



 

<span data-ttu-id="f98d1-116">Supporta un solo tipo di output:</span><span class="sxs-lookup"><span data-stu-id="f98d1-116">It supports a single output type:</span></span>



| <span data-ttu-id="f98d1-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="f98d1-117">Subtype</span></span>             | <span data-ttu-id="f98d1-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f98d1-118">Description</span></span> |
|---------------------|-------------|
| <span data-ttu-id="f98d1-119">\_YUY2 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="f98d1-119">MFVideoFormat\_YUY2</span></span> | <span data-ttu-id="f98d1-120">Video di YUY2</span><span class="sxs-lookup"><span data-stu-id="f98d1-120">YUY2 video</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="f98d1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f98d1-121">Requirements</span></span>



| <span data-ttu-id="f98d1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f98d1-122">Requirement</span></span> | <span data-ttu-id="f98d1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f98d1-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f98d1-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f98d1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f98d1-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f98d1-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f98d1-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f98d1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f98d1-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f98d1-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f98d1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f98d1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f98d1-129"><dt>Mfdvdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f98d1-129"><dt>Mfdvdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f98d1-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f98d1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f98d1-131">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="f98d1-131">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="f98d1-132">Formati multimediali supportati in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f98d1-132">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f98d1-133">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="f98d1-133">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 




