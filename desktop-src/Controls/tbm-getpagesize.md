---
title: Messaggio TBM_GETPAGESIZE (COMmctrl. h)
description: Recupera il numero di posizioni logiche spostate dal dispositivo di scorrimento di TrackBar in risposta all'input da tastiera, ad esempio le chiavi o o l'input del mouse, ad esempio i clic nel canale del TrackBar.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- Controlli di Windows Message TBM_GETPAGESIZE
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac58c0b935b468cf8af565fba2db67c88418ee4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119822"
---
# <a name="tbm_getpagesize-message"></a><span data-ttu-id="86fb2-104">\_Messaggio GETPAGESIZE TBM</span><span class="sxs-lookup"><span data-stu-id="86fb2-104">TBM\_GETPAGESIZE message</span></span>

<span data-ttu-id="86fb2-105">Recupera il numero di posizioni logiche spostate dal dispositivo di scorrimento di TrackBar in risposta all'input da tastiera, ad esempio le chiavi o o l'input del mouse, ad esempio i clic nel canale del TrackBar.</span><span class="sxs-lookup"><span data-stu-id="86fb2-105">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input, such as the or keys, or mouse input, such as clicks in the trackbar's channel.</span></span> <span data-ttu-id="86fb2-106">Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="86fb2-106">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="86fb2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="86fb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86fb2-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86fb2-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="86fb2-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="86fb2-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="86fb2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86fb2-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="86fb2-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="86fb2-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86fb2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86fb2-112">Return value</span></span>

<span data-ttu-id="86fb2-113">Restituisce un valore a 32 bit che specifica le dimensioni di pagina per il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="86fb2-113">Returns a 32-bit value that specifies the page size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="86fb2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="86fb2-114">Remarks</span></span>

<span data-ttu-id="86fb2-115">TrackBar invia anche un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con i \_ codici di notifica TB PAGEUP e TB \_ PGGIÙ alla finestra padre quando riceve l'input della tastiera o del mouse che scorre la pagina.</span><span class="sxs-lookup"><span data-stu-id="86fb2-115">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_PAGEUP and TB\_PAGEDOWN notification codes to its parent window when it receives keyboard or mouse input that scrolls the page.</span></span>

## <a name="requirements"></a><span data-ttu-id="86fb2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86fb2-116">Requirements</span></span>



| <span data-ttu-id="86fb2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="86fb2-117">Requirement</span></span> | <span data-ttu-id="86fb2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="86fb2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86fb2-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86fb2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="86fb2-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86fb2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86fb2-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86fb2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="86fb2-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="86fb2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86fb2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86fb2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="86fb2-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="86fb2-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86fb2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86fb2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86fb2-126">**sepagesize TBM \_**</span><span class="sxs-lookup"><span data-stu-id="86fb2-126">**TBM\_SETPAGESIZE**</span></span>](tbm-setpagesize.md)
</dt> </dl>

 

 





