---
title: Messaggio BM_GETIMAGE (winuser. h)
description: Recupera un handle per l'immagine (icona o bitmap) associata al pulsante.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- Controlli di Windows Message BM_GETIMAGE
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340972"
---
# <a name="bm_getimage-message"></a><span data-ttu-id="d0c77-104">\_Messaggio BM GETimage</span><span class="sxs-lookup"><span data-stu-id="d0c77-104">BM\_GETIMAGE message</span></span>

<span data-ttu-id="d0c77-105">Recupera un handle per l'immagine (icona o bitmap) associata al pulsante.</span><span class="sxs-lookup"><span data-stu-id="d0c77-105">Retrieves a handle to the image (icon or bitmap) associated with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0c77-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0c77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0c77-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0c77-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c77-108">Tipo di immagine da associare al pulsante.</span><span class="sxs-lookup"><span data-stu-id="d0c77-108">The type of image to associate with the button.</span></span> <span data-ttu-id="d0c77-109">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d0c77-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d0c77-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d0c77-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="d0c77-111">Significato</span><span class="sxs-lookup"><span data-stu-id="d0c77-111">Meaning</span></span>              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="d0c77-112"><dt>**\_bitmap immagine**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c77-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl> | <span data-ttu-id="d0c77-113">Bitmap.</span><span class="sxs-lookup"><span data-stu-id="d0c77-113">A bitmap.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="d0c77-114"><dt>**\_icona immagine**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c77-114"><dt>**IMAGE\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="d0c77-115">Un'icona.</span><span class="sxs-lookup"><span data-stu-id="d0c77-115">An icon.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="d0c77-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0c77-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c77-117">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="d0c77-117">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0c77-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0c77-118">Return value</span></span>

<span data-ttu-id="d0c77-119">Il valore restituito è un handle per l'immagine, se disponibile. in caso contrario, è **null**.</span><span class="sxs-lookup"><span data-stu-id="d0c77-119">The return value is a handle to the image, if any; otherwise, it is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c77-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0c77-120">Requirements</span></span>



| <span data-ttu-id="d0c77-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0c77-121">Requirement</span></span> | <span data-ttu-id="d0c77-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d0c77-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c77-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0c77-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d0c77-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0c77-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d0c77-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0c77-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d0c77-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0c77-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d0c77-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0c77-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0c77-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0c77-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c77-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0c77-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d0c77-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d0c77-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d0c77-131">**\_immagine BM**</span><span class="sxs-lookup"><span data-stu-id="d0c77-131">**BM\_SETIMAGE**</span></span>](bm-setimage.md)
</dt> <dt>

<span data-ttu-id="d0c77-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d0c77-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d0c77-133">Pulsanti</span><span class="sxs-lookup"><span data-stu-id="d0c77-133">Buttons</span></span>](buttons.md)
</dt> </dl>

 

 





