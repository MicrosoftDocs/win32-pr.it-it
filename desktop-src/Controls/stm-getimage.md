---
title: Messaggio STM_GETIMAGE (winuser. h)
description: Un'applicazione invia un \_ messaggio STM GetImage per recuperare un handle per l'immagine (icona o bitmap) associata a un controllo statico.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- Controlli di Windows Message STM_GETIMAGE
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047917"
---
# <a name="stm_getimage-message"></a><span data-ttu-id="33ce8-104">\_Messaggio GETIMAGE STM</span><span class="sxs-lookup"><span data-stu-id="33ce8-104">STM\_GETIMAGE message</span></span>

<span data-ttu-id="33ce8-105">Un'applicazione invia un messaggio **STM \_ GetImage** per recuperare un handle per l'immagine (icona o bitmap) associata a un controllo statico.</span><span class="sxs-lookup"><span data-stu-id="33ce8-105">An application sends an **STM\_GETIMAGE** message to retrieve a handle to the image (icon or bitmap) associated with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="33ce8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="33ce8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33ce8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33ce8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33ce8-108">Specifica il tipo di immagine da recuperare.</span><span class="sxs-lookup"><span data-stu-id="33ce8-108">Specifies the type of image to retrieve.</span></span> <span data-ttu-id="33ce8-109">Questo parametro può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="33ce8-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="33ce8-110">Valore</span><span class="sxs-lookup"><span data-stu-id="33ce8-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="33ce8-111">Significato</span><span class="sxs-lookup"><span data-stu-id="33ce8-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="33ce8-112"><dt>**\_bitmap immagine**</dt></span><span class="sxs-lookup"><span data-stu-id="33ce8-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="33ce8-113">Bitmap.</span><span class="sxs-lookup"><span data-stu-id="33ce8-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="33ce8-114"><dt>**\_cursore immagine**</dt></span><span class="sxs-lookup"><span data-stu-id="33ce8-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="33ce8-115">Cursore.</span><span class="sxs-lookup"><span data-stu-id="33ce8-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="33ce8-116"><dt>**\_ENHMETAFILE immagine**</dt></span><span class="sxs-lookup"><span data-stu-id="33ce8-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="33ce8-117">Enhanced Metafile.</span><span class="sxs-lookup"><span data-stu-id="33ce8-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="33ce8-118"><dt>**\_icona immagine**</dt></span><span class="sxs-lookup"><span data-stu-id="33ce8-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="33ce8-119">Icona.</span><span class="sxs-lookup"><span data-stu-id="33ce8-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="33ce8-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33ce8-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33ce8-121">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="33ce8-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33ce8-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33ce8-122">Return value</span></span>

<span data-ttu-id="33ce8-123">Il valore restituito è un handle per l'immagine, se disponibile. in caso contrario, è **null**.</span><span class="sxs-lookup"><span data-stu-id="33ce8-123">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="33ce8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33ce8-124">Requirements</span></span>



| <span data-ttu-id="33ce8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ce8-125">Requirement</span></span> | <span data-ttu-id="33ce8-126">Valore</span><span class="sxs-lookup"><span data-stu-id="33ce8-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ce8-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33ce8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="33ce8-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33ce8-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="33ce8-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33ce8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="33ce8-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33ce8-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33ce8-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33ce8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="33ce8-132"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33ce8-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ce8-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33ce8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ce8-134">**\_Immagine STM**</span><span class="sxs-lookup"><span data-stu-id="33ce8-134">**STM\_SETIMAGE**</span></span>](stm-setimage.md)
</dt> </dl>

 

 





