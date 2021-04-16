---
title: Messaggio TB_LOADIMAGES (COMmctrl. h)
description: Carica le immagini dei pulsanti definite dal sistema nell'elenco immagini di un controllo Toolbar.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- Controlli di Windows Message TB_LOADIMAGES
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478089"
---
# <a name="tb_loadimages-message"></a><span data-ttu-id="1b208-104">TB \_ LOADIMAGES messaggio</span><span class="sxs-lookup"><span data-stu-id="1b208-104">TB\_LOADIMAGES message</span></span>

<span data-ttu-id="1b208-105">Carica le immagini dei pulsanti definite dal sistema nell'elenco immagini di un controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="1b208-105">Loads system-defined button images into a toolbar control's image list.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b208-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b208-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b208-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b208-108">Identificatore di un elenco di immagini di un pulsante definito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1b208-108">Identifier of a system-defined button image list.</span></span> <span data-ttu-id="1b208-109">Questo parametro può essere impostato su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1b208-109">This parameter can be set to one of the following values.</span></span>



| <span data-ttu-id="1b208-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1b208-110">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="1b208-111">Significato</span><span class="sxs-lookup"><span data-stu-id="1b208-111">Meaning</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <span data-ttu-id="1b208-112"><dt>**\_colore di \_ grandi dimensioni \_ di IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="1b208-112"><dt>**IDB\_HIST\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="1b208-113">Bitmap di Esplora risorse di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="1b208-113">Windows Explorer bitmaps in large size.</span></span><br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <span data-ttu-id="1b208-114"><dt>**colore di un \_ piccolo cron di IDB \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b208-114"><dt>**IDB\_HIST\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="1b208-115">Bitmap di Esplora risorse di dimensioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="1b208-115">Windows Explorer bitmaps in small size.</span></span><br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <span data-ttu-id="1b208-116"><dt>**\_ \_ colore large standard \_ IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="1b208-116"><dt>**IDB\_STD\_LARGE\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="1b208-117">Bitmap standard di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="1b208-117">Standard bitmaps in large size.</span></span><br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <span data-ttu-id="1b208-118"><dt>**\_ \_ piccolo colore STD \_ IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="1b208-118"><dt>**IDB\_STD\_SMALL\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="1b208-119">Bitmap standard in dimensioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="1b208-119">Standard bitmaps in small size.</span></span><br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <span data-ttu-id="1b208-120"><dt>**\_visualizzazione IDB \_ - \_ colore grande**</dt></span><span class="sxs-lookup"><span data-stu-id="1b208-120"><dt>**IDB\_VIEW\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="1b208-121">Visualizza le bitmap in grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="1b208-121">View bitmaps in large size.</span></span><br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <span data-ttu-id="1b208-122"><dt>**\_ \_ colore piccolo visualizzazione \_ IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="1b208-122"><dt>**IDB\_VIEW\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="1b208-123">Visualizzare bitmap di dimensioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="1b208-123">View bitmaps in small size.</span></span><br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <span data-ttu-id="1b208-124"><dt>**normale di IDB \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b208-124"><dt>**IDB\_HIST\_NORMAL**</dt></span></span> </dl>                 | <span data-ttu-id="1b208-125">Pulsanti di spostamento di Esplora risorse e bitmap preferiti nello stato normale.</span><span class="sxs-lookup"><span data-stu-id="1b208-125">Windows Explorer travel buttons and favorites bitmaps in normal state.</span></span><br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <span data-ttu-id="1b208-126"><dt>**accesso frequente \_ a IDB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b208-126"><dt>**IDB\_HIST\_HOT**</dt></span></span> </dl>                          | <span data-ttu-id="1b208-127">Pulsanti di spostamento di Esplora risorse e bitmap preferiti nello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="1b208-127">Windows Explorer travel buttons and favorites bitmaps in hot state.</span></span><br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <span data-ttu-id="1b208-128"><dt>**IDB \_ è \_ disabilitato**</dt></span><span class="sxs-lookup"><span data-stu-id="1b208-128"><dt>**IDB\_HIST\_DISABLED**</dt></span></span> </dl>           | <span data-ttu-id="1b208-129">Pulsanti di spostamento di Esplora risorse e bitmap preferiti nello stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="1b208-129">Windows Explorer travel buttons and favorites bitmaps in disabled state.</span></span><br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <span data-ttu-id="1b208-130"><dt>**stato di IDB \_ \_ premuto**</dt></span><span class="sxs-lookup"><span data-stu-id="1b208-130"><dt>**IDB\_HIST\_PRESSED**</dt></span></span> </dl>              | <span data-ttu-id="1b208-131">Pulsanti di spostamento di Esplora risorse e bitmap preferiti nello stato premuto.</span><span class="sxs-lookup"><span data-stu-id="1b208-131">Windows Explorer travel buttons and favorites bitmaps in pressed state.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="1b208-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b208-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b208-133">Handle di istanza.</span><span class="sxs-lookup"><span data-stu-id="1b208-133">Instance handle.</span></span> <span data-ttu-id="1b208-134">Questo parametro deve essere impostato su HINST \_ COMmctrl.</span><span class="sxs-lookup"><span data-stu-id="1b208-134">This parameter must be set to HINST\_COMMCTRL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b208-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b208-135">Return value</span></span>

<span data-ttu-id="1b208-136">Numero di immagini nell'elenco immagini.</span><span class="sxs-lookup"><span data-stu-id="1b208-136">The count of images in the image list.</span></span> <span data-ttu-id="1b208-137">Restituisce zero se la barra degli strumenti non dispone di un elenco di immagini o se l'elenco di immagini esistente è vuoto.</span><span class="sxs-lookup"><span data-stu-id="1b208-137">Returns zero if the toolbar has no image list or if the existing image list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b208-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b208-138">Remarks</span></span>

<span data-ttu-id="1b208-139">Quando si preparano le strutture [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) prima di inviare il messaggio [**TB \_ ADDBUTTONS**](tb-addbuttons.md) , è necessario usare i valori di indice immagine appropriati.</span><span class="sxs-lookup"><span data-stu-id="1b208-139">You must use the proper image index values when you prepare [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures prior to sending the [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="1b208-140">Per un elenco dei valori di indice immagine per le bitmap predefinite, vedere [valori di indice dell'immagine del pulsante standard della barra degli strumenti](toolbar-standard-button-image-index-values.md).</span><span class="sxs-lookup"><span data-stu-id="1b208-140">For a list of image index values for these preset bitmaps, see [Toolbar Standard Button Image Index Values](toolbar-standard-button-image-index-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1b208-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="1b208-141">Examples</span></span>

<span data-ttu-id="1b208-142">Il codice di esempio seguente carica le immagini a colori standard di sistema Small.</span><span class="sxs-lookup"><span data-stu-id="1b208-142">The following sample code loads the system standard small color images.</span></span>


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a><span data-ttu-id="1b208-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b208-143">Requirements</span></span>



| <span data-ttu-id="1b208-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b208-144">Requirement</span></span> | <span data-ttu-id="1b208-145">Valore</span><span class="sxs-lookup"><span data-stu-id="1b208-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b208-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b208-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1b208-147">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b208-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b208-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b208-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1b208-149">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b208-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b208-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b208-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b208-151"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b208-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b208-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b208-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b208-153">**TB \_ ADDBITMAP**</span><span class="sxs-lookup"><span data-stu-id="1b208-153">**TB\_ADDBITMAP**</span></span>](tb-addbitmap.md)
</dt> </dl>

 

 





