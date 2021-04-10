---
title: Messaggio di WM_CAP_PAL_PASTE (VFW. h)
description: Il \_ \_ \_ messaggio per la copia con capo di WM Cap copia la tavolozza dagli Appunti e la passa a un driver di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capPalettePaste.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- WM_CAP_PAL_PASTE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3daf88c69edbb8bad6257456b95a86c8a68df328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964019"
---
# <a name="wm_cap_pal_paste-message"></a><span data-ttu-id="d0465-105">\_Messaggio incolla di WM Cap \_ PAL \_</span><span class="sxs-lookup"><span data-stu-id="d0465-105">WM\_CAP\_PAL\_PASTE message</span></span>

<span data-ttu-id="d0465-106">Il messaggio per la copia con **capo di WM \_ Cap \_ \_** copia la tavolozza dagli Appunti e la passa a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d0465-106">The **WM\_CAP\_PAL\_PASTE** message copies the palette from the clipboard and passes it to a capture driver.</span></span> <span data-ttu-id="d0465-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) .</span><span class="sxs-lookup"><span data-stu-id="d0465-107">You can send this message explicitly or by using the [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) macro.</span></span>


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="d0465-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0465-108">Return Value</span></span>

<span data-ttu-id="d0465-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d0465-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="d0465-110">Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.</span><span class="sxs-lookup"><span data-stu-id="d0465-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0465-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0465-111">Remarks</span></span>

<span data-ttu-id="d0465-112">Un driver di acquisizione utilizza una tavolozza quando richiesto dal formato video specificato.</span><span class="sxs-lookup"><span data-stu-id="d0465-112">A capture driver uses a palette when required by the specified digitized video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0465-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0465-113">Requirements</span></span>



| <span data-ttu-id="d0465-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0465-114">Requirement</span></span> | <span data-ttu-id="d0465-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d0465-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d0465-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0465-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d0465-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0465-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d0465-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0465-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d0465-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0465-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d0465-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0465-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0465-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0465-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0465-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0465-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0465-123">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d0465-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d0465-124">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d0465-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





