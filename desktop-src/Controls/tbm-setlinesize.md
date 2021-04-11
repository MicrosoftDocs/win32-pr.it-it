---
title: Messaggio TBM_SETLINESIZE (COMmctrl. h)
description: Imposta il numero di posizioni logiche spostate dal dispositivo di scorrimento di TrackBar in risposta all'input da tastiera dei tasti di direzione, ad esempio i tasti o. Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento.
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- Controlli di Windows Message TBM_SETLINESIZE
topic_type:
- apiref
api_name:
- TBM_SETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec898ed09b20f15023ef04a399f5644df746e495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963887"
---
# <a name="tbm_setlinesize-message"></a><span data-ttu-id="0c010-105">\_Messaggio SETLINESIZE TBM</span><span class="sxs-lookup"><span data-stu-id="0c010-105">TBM\_SETLINESIZE message</span></span>

<span data-ttu-id="0c010-106">Imposta il numero di posizioni logiche spostate dal dispositivo di scorrimento di TrackBar in risposta all'input da tastiera dei tasti di direzione, ad esempio i tasti o.</span><span class="sxs-lookup"><span data-stu-id="0c010-106">Sets the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="0c010-107">Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="0c010-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c010-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c010-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c010-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c010-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0c010-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0c010-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0c010-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c010-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c010-112">Nuove dimensioni della riga.</span><span class="sxs-lookup"><span data-stu-id="0c010-112">New line size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c010-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c010-113">Return value</span></span>

<span data-ttu-id="0c010-114">Restituisce un valore a 32 bit che specifica la dimensione della riga precedente.</span><span class="sxs-lookup"><span data-stu-id="0c010-114">Returns a 32-bit value that specifies the previous line size.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c010-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c010-115">Remarks</span></span>

<span data-ttu-id="0c010-116">L'impostazione predefinita per le dimensioni della riga è 1.</span><span class="sxs-lookup"><span data-stu-id="0c010-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="0c010-117">TrackBar invia anche un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con i \_ \_ codici di notifica TB e TB LINEDOWN alla finestra padre quando l'utente preme i tasti di direzione.</span><span class="sxs-lookup"><span data-stu-id="0c010-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c010-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c010-118">Requirements</span></span>



| <span data-ttu-id="0c010-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c010-119">Requirement</span></span> | <span data-ttu-id="0c010-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0c010-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c010-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c010-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0c010-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c010-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c010-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c010-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0c010-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0c010-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c010-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c010-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c010-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c010-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c010-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c010-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c010-128">**TBM \_ GETLINESIZE**</span><span class="sxs-lookup"><span data-stu-id="0c010-128">**TBM\_GETLINESIZE**</span></span>](tbm-getlinesize.md)
</dt> </dl>

 

 





