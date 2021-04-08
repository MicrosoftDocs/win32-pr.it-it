---
title: Messaggio TBM_SETPAGESIZE (COMmctrl. h)
description: Imposta il numero di posizioni logiche spostate dal dispositivo di scorrimento di TrackBar in risposta all'input da tastiera, ad esempio le chiavi o o l'input del mouse, ad esempio i clic nel canale del TrackBar.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- Controlli di Windows Message TBM_SETPAGESIZE
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5d8a396bb605b4276346e84e7b46bfbefe0657
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048594"
---
# <a name="tbm_setpagesize-message"></a><span data-ttu-id="49c08-104">\_Messaggio di SEPAGESIZE TBM</span><span class="sxs-lookup"><span data-stu-id="49c08-104">TBM\_SETPAGESIZE message</span></span>

<span data-ttu-id="49c08-105">Imposta il numero di posizioni logiche spostate dal dispositivo di scorrimento di TrackBar in risposta all'input da tastiera, ad esempio le chiavi o o l'input del mouse, ad esempio i clic nel canale del TrackBar.</span><span class="sxs-lookup"><span data-stu-id="49c08-105">Sets the number of logical positions the trackbar's slider moves in response to keyboard input, such as the or keys, or mouse input, such as clicks in the trackbar's channel.</span></span> <span data-ttu-id="49c08-106">Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="49c08-106">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="49c08-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="49c08-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49c08-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49c08-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="49c08-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="49c08-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="49c08-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49c08-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49c08-111">Nuove dimensioni della pagina.</span><span class="sxs-lookup"><span data-stu-id="49c08-111">New page size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49c08-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49c08-112">Return value</span></span>

<span data-ttu-id="49c08-113">Restituisce un valore a 32 bit che specifica le dimensioni di pagina precedenti.</span><span class="sxs-lookup"><span data-stu-id="49c08-113">Returns a 32-bit value that specifies the previous page size.</span></span>

## <a name="remarks"></a><span data-ttu-id="49c08-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="49c08-114">Remarks</span></span>

<span data-ttu-id="49c08-115">TrackBar invia anche un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con i \_ codici di notifica TB PAGEUP e TB \_ PGGIÙ alla finestra padre quando riceve l'input della tastiera o del mouse che scorre la pagina.</span><span class="sxs-lookup"><span data-stu-id="49c08-115">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_PAGEUP and TB\_PAGEDOWN notification codes to its parent window when it receives keyboard or mouse input that scrolls the page.</span></span>

## <a name="requirements"></a><span data-ttu-id="49c08-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49c08-116">Requirements</span></span>



| <span data-ttu-id="49c08-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="49c08-117">Requirement</span></span> | <span data-ttu-id="49c08-118">Valore</span><span class="sxs-lookup"><span data-stu-id="49c08-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49c08-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49c08-119">Minimum supported client</span></span><br/> | <span data-ttu-id="49c08-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49c08-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49c08-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49c08-121">Minimum supported server</span></span><br/> | <span data-ttu-id="49c08-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49c08-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49c08-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49c08-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="49c08-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49c08-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49c08-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49c08-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c08-126">**TBM \_ GETpagesize**</span><span class="sxs-lookup"><span data-stu-id="49c08-126">**TBM\_GETPAGESIZE**</span></span>](tbm-getpagesize.md)
</dt> </dl>

 

 





