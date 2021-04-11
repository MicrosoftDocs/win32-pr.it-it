---
title: Messaggio BM_SETIMAGE (winuser. h)
description: Associa una nuova immagine (icona o bitmap) a un pulsante.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- Controlli di Windows Message BM_SETIMAGE
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d083c4fb509d51eb017bb7d3d38fab07b4c006
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119239"
---
# <a name="bm_setimage-message"></a><span data-ttu-id="3e685-104">Messaggio di immagine di BM \_</span><span class="sxs-lookup"><span data-stu-id="3e685-104">BM\_SETIMAGE message</span></span>

<span data-ttu-id="3e685-105">Associa una nuova immagine (icona o bitmap) a un pulsante.</span><span class="sxs-lookup"><span data-stu-id="3e685-105">Associates a new image (icon or bitmap) with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e685-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e685-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e685-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e685-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e685-108">Tipo di immagine da associare al pulsante.</span><span class="sxs-lookup"><span data-stu-id="3e685-108">The type of image to associate with the button.</span></span> <span data-ttu-id="3e685-109">Questo parametro può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e685-109">This parameter can be one of the following values:</span></span>

-   <span data-ttu-id="3e685-110">\_bitmap immagine</span><span class="sxs-lookup"><span data-stu-id="3e685-110">IMAGE\_BITMAP</span></span>
-   <span data-ttu-id="3e685-111">\_icona immagine</span><span class="sxs-lookup"><span data-stu-id="3e685-111">IMAGE\_ICON</span></span>

</dd> <dt>

<span data-ttu-id="3e685-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e685-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e685-113">Handle (**HICON** o **HBITMAP**) per l'immagine da associare al pulsante.</span><span class="sxs-lookup"><span data-stu-id="3e685-113">A handle (**HICON** or **HBITMAP**) to the image to associate with the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e685-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e685-114">Return value</span></span>

<span data-ttu-id="3e685-115">Il valore restituito è un handle per l'immagine precedentemente associata al pulsante, se disponibile. in caso contrario, è **null**.</span><span class="sxs-lookup"><span data-stu-id="3e685-115">The return value is a handle to the image previously associated with the button, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e685-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e685-116">Remarks</span></span>

<span data-ttu-id="3e685-117">L'aspetto del testo, di un'icona o di entrambi su un controllo Button dipende dall' [**\_ icona BS**](button-styles.md) e dagli stili di [**\_ bitmap BS**](button-styles.md) e dal fatto che il messaggio **BM \_ diImage** venga chiamato.</span><span class="sxs-lookup"><span data-stu-id="3e685-117">The appearance of text, an icon, or both on a button control depends on the [**BS\_ICON**](button-styles.md) and [**BS\_BITMAP**](button-styles.md) styles, and whether the **BM\_SETIMAGE** message is called.</span></span> <span data-ttu-id="3e685-118">I risultati possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e685-118">The possible results are as follows:</span></span>



| <span data-ttu-id="3e685-119">\_Icona BS o \_ set di bitmap BS?</span><span class="sxs-lookup"><span data-stu-id="3e685-119">BS\_ICON or BS\_BITMAP Set?</span></span> | <span data-ttu-id="3e685-120">\_Nome dell'immagine BM</span><span class="sxs-lookup"><span data-stu-id="3e685-120">BM\_SETIMAGE Called?</span></span> | <span data-ttu-id="3e685-121">Risultato</span><span class="sxs-lookup"><span data-stu-id="3e685-121">Result</span></span>              |
|-----------------------------|----------------------|---------------------|
| <span data-ttu-id="3e685-122">Sì</span><span class="sxs-lookup"><span data-stu-id="3e685-122">Yes</span></span>                         | <span data-ttu-id="3e685-123">Sì</span><span class="sxs-lookup"><span data-stu-id="3e685-123">Yes</span></span>                  | <span data-ttu-id="3e685-124">Mostra solo l'icona.</span><span class="sxs-lookup"><span data-stu-id="3e685-124">Show icon only.</span></span>     |
| <span data-ttu-id="3e685-125">No</span><span class="sxs-lookup"><span data-stu-id="3e685-125">No</span></span>                          | <span data-ttu-id="3e685-126">Sì</span><span class="sxs-lookup"><span data-stu-id="3e685-126">Yes</span></span>                  | <span data-ttu-id="3e685-127">Mostra icona e testo.</span><span class="sxs-lookup"><span data-stu-id="3e685-127">Show icon and text.</span></span> |
| <span data-ttu-id="3e685-128">Sì</span><span class="sxs-lookup"><span data-stu-id="3e685-128">Yes</span></span>                         | <span data-ttu-id="3e685-129">No</span><span class="sxs-lookup"><span data-stu-id="3e685-129">No</span></span>                   | <span data-ttu-id="3e685-130">Mostra solo testo.</span><span class="sxs-lookup"><span data-stu-id="3e685-130">Show text only.</span></span>     |
| <span data-ttu-id="3e685-131">No</span><span class="sxs-lookup"><span data-stu-id="3e685-131">No</span></span>                          | <span data-ttu-id="3e685-132">No</span><span class="sxs-lookup"><span data-stu-id="3e685-132">No</span></span>                   | <span data-ttu-id="3e685-133">Mostra solo testo</span><span class="sxs-lookup"><span data-stu-id="3e685-133">Show text only</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="3e685-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e685-134">Requirements</span></span>



| <span data-ttu-id="3e685-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e685-135">Requirement</span></span> | <span data-ttu-id="3e685-136">Valore</span><span class="sxs-lookup"><span data-stu-id="3e685-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e685-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e685-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3e685-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e685-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3e685-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e685-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3e685-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e685-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3e685-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e685-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e685-142"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e685-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e685-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e685-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e685-144">**BM \_ GETimage**</span><span class="sxs-lookup"><span data-stu-id="3e685-144">**BM\_GETIMAGE**</span></span>](bm-getimage.md)
</dt> </dl>

 

 





