---
title: Messaggio STM_SETIMAGE (winuser. h)
description: Un'applicazione invia un \_ messaggio di immagine STM per associare una nuova immagine a un controllo statico.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- Controlli di Windows Message STM_SETIMAGE
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963889"
---
# <a name="stm_setimage-message"></a><span data-ttu-id="00e37-104">\_Messaggio immagine STM</span><span class="sxs-lookup"><span data-stu-id="00e37-104">STM\_SETIMAGE message</span></span>

<span data-ttu-id="00e37-105">Un'applicazione invia un messaggio di **\_ Immagine STM** per associare una nuova immagine a un controllo statico.</span><span class="sxs-lookup"><span data-stu-id="00e37-105">An application sends an **STM\_SETIMAGE** message to associate a new image with a static control.</span></span>

## <a name="parameters"></a><span data-ttu-id="00e37-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00e37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00e37-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00e37-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00e37-108">Specifica il tipo di immagine da associare al controllo statico.</span><span class="sxs-lookup"><span data-stu-id="00e37-108">Specifies the type of image to associate with the static control.</span></span> <span data-ttu-id="00e37-109">Questo parametro può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="00e37-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="00e37-110">Valore</span><span class="sxs-lookup"><span data-stu-id="00e37-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="00e37-111">Significato</span><span class="sxs-lookup"><span data-stu-id="00e37-111">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <span data-ttu-id="00e37-112"><dt>**\_bitmap immagine**</dt></span><span class="sxs-lookup"><span data-stu-id="00e37-112"><dt>**IMAGE\_BITMAP**</dt></span></span> </dl>                | <span data-ttu-id="00e37-113">Bitmap.</span><span class="sxs-lookup"><span data-stu-id="00e37-113">Bitmap.</span></span><br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <span data-ttu-id="00e37-114"><dt>**\_cursore immagine**</dt></span><span class="sxs-lookup"><span data-stu-id="00e37-114"><dt>**IMAGE\_CURSOR**</dt></span></span> </dl>                | <span data-ttu-id="00e37-115">Cursore.</span><span class="sxs-lookup"><span data-stu-id="00e37-115">Cursor.</span></span><br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <span data-ttu-id="00e37-116"><dt>**\_ENHMETAFILE immagine**</dt></span><span class="sxs-lookup"><span data-stu-id="00e37-116"><dt>**IMAGE\_ENHMETAFILE**</dt></span></span> </dl> | <span data-ttu-id="00e37-117">Enhanced Metafile.</span><span class="sxs-lookup"><span data-stu-id="00e37-117">Enhanced metafile.</span></span><br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <span data-ttu-id="00e37-118"><dt>**\_icona immagine**</dt></span><span class="sxs-lookup"><span data-stu-id="00e37-118"><dt>**IMAGE\_ICON**</dt></span></span> </dl>                      | <span data-ttu-id="00e37-119">Icona.</span><span class="sxs-lookup"><span data-stu-id="00e37-119">Icon.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="00e37-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00e37-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00e37-121">Handle per l'immagine da associare al controllo statico.</span><span class="sxs-lookup"><span data-stu-id="00e37-121">Handle to the image to associate with the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00e37-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00e37-122">Return value</span></span>

<span data-ttu-id="00e37-123">Il valore restituito è un handle per l'immagine associata in precedenza al controllo statico, se disponibile. in caso contrario, è **null**.</span><span class="sxs-lookup"><span data-stu-id="00e37-123">The return value is a handle to the image previously associated with the static control, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="00e37-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="00e37-124">Remarks</span></span>

<span data-ttu-id="00e37-125">Per associare un'immagine a un controllo statico, il controllo deve avere lo stile appropriato.</span><span class="sxs-lookup"><span data-stu-id="00e37-125">To associate an image with a static control, the control must have the proper style.</span></span> <span data-ttu-id="00e37-126">La tabella seguente illustra lo stile necessario per ogni tipo di immagine.</span><span class="sxs-lookup"><span data-stu-id="00e37-126">The following table shows the style needed for each image type.</span></span>



| <span data-ttu-id="00e37-127">Tipo di immagine</span><span class="sxs-lookup"><span data-stu-id="00e37-127">Image type</span></span>         | <span data-ttu-id="00e37-128">Stile del controllo statico</span><span class="sxs-lookup"><span data-stu-id="00e37-128">Static control style</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="00e37-129">\_bitmap immagine</span><span class="sxs-lookup"><span data-stu-id="00e37-129">IMAGE\_BITMAP</span></span>      | <span data-ttu-id="00e37-130">\_bitmap SS</span><span class="sxs-lookup"><span data-stu-id="00e37-130">SS\_BITMAP</span></span>           |
| <span data-ttu-id="00e37-131">\_cursore immagine</span><span class="sxs-lookup"><span data-stu-id="00e37-131">IMAGE\_CURSOR</span></span>      | <span data-ttu-id="00e37-132">\_icona SS</span><span class="sxs-lookup"><span data-stu-id="00e37-132">SS\_ICON</span></span>             |
| <span data-ttu-id="00e37-133">\_ENHMETAFILE immagine</span><span class="sxs-lookup"><span data-stu-id="00e37-133">IMAGE\_ENHMETAFILE</span></span> | <span data-ttu-id="00e37-134">\_ENHMETAFILE SS</span><span class="sxs-lookup"><span data-stu-id="00e37-134">SS\_ENHMETAFILE</span></span>      |
| <span data-ttu-id="00e37-135">\_icona immagine</span><span class="sxs-lookup"><span data-stu-id="00e37-135">IMAGE\_ICON</span></span>        | <span data-ttu-id="00e37-136">\_icona SS</span><span class="sxs-lookup"><span data-stu-id="00e37-136">SS\_ICON</span></span>             |



 

> [!IMPORTANT]
>
> <span data-ttu-id="00e37-137">Nella versione 6 dei controlli Microsoft Win32, una bitmap passata a un controllo statico che utilizza il messaggio di **\_ Immagine STM** è la stessa bitmap restituita da un successivo messaggio di **\_ Immagine STM** .</span><span class="sxs-lookup"><span data-stu-id="00e37-137">In version 6 of the Microsoft Win32 controls, a bitmap passed to a static control using the **STM\_SETIMAGE** message was the same bitmap returned by a subsequent **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="00e37-138">Il client è responsabile dell'eliminazione di tutte le bitmap inviate a un controllo statico.</span><span class="sxs-lookup"><span data-stu-id="00e37-138">The client is responsible to delete any bitmap sent to a static control.</span></span>
>
> <span data-ttu-id="00e37-139">Con Windows XP, se la bitmap passata nel messaggio **di \_ Immagine STM** contiene pixel con un valore alfa diverso da zero, il controllo statico acquisisce una copia della bitmap.</span><span class="sxs-lookup"><span data-stu-id="00e37-139">With Windows XP, if the bitmap passed in the **STM\_SETIMAGE** message contains pixels with nonzero alpha, the static control takes a copy of the bitmap.</span></span> <span data-ttu-id="00e37-140">Questa bitmap copiata viene restituita dal successivo messaggio dell' **\_ Immagine STM** .</span><span class="sxs-lookup"><span data-stu-id="00e37-140">This copied bitmap is returned by the next **STM\_SETIMAGE** message.</span></span> <span data-ttu-id="00e37-141">Il codice client può rilevare in modo indipendente le bitmap passate al controllo statico, ma se non controlla e rilascia le bitmap restituite da messaggi di **\_ Immagine STM** , le bitmap vengono perse.</span><span class="sxs-lookup"><span data-stu-id="00e37-141">The client code may independently track the bitmaps passed to the static control, but if it does not check and release the bitmaps returned from **STM\_SETIMAGE** messages, the bitmaps are leaked.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00e37-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00e37-142">Requirements</span></span>



| <span data-ttu-id="00e37-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="00e37-143">Requirement</span></span> | <span data-ttu-id="00e37-144">Valore</span><span class="sxs-lookup"><span data-stu-id="00e37-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00e37-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00e37-145">Minimum supported client</span></span><br/> | <span data-ttu-id="00e37-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00e37-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="00e37-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00e37-147">Minimum supported server</span></span><br/> | <span data-ttu-id="00e37-148">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="00e37-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="00e37-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00e37-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="00e37-150"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00e37-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00e37-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00e37-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e37-152">**GetImage STM \_**</span><span class="sxs-lookup"><span data-stu-id="00e37-152">**STM\_GETIMAGE**</span></span>](stm-getimage.md)
</dt> </dl>

 

 





