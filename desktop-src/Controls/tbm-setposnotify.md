---
title: Messaggio TBM_SETPOSNOTIFY (COMmctrl. h)
description: Imposta la posizione logica corrente del dispositivo di scorrimento in un TrackBar.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- Controlli di Windows Message TBM_SETPOSNOTIFY
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636a2add9f13470a89b312450f1a3dcbc185be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475911"
---
# <a name="tbm_setposnotify-message"></a><span data-ttu-id="6aa07-104">\_Messaggio SETPOSNOTIFY TBM</span><span class="sxs-lookup"><span data-stu-id="6aa07-104">TBM\_SETPOSNOTIFY message</span></span>

<span data-ttu-id="6aa07-105">Imposta la posizione logica corrente del dispositivo di scorrimento in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6aa07-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6aa07-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6aa07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aa07-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6aa07-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6aa07-108">il wParam è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="6aa07-108">wParam is unused.</span></span>

</dd> <dt>

<span data-ttu-id="6aa07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6aa07-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6aa07-110">Nuova posizione logica del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="6aa07-110">New logical position of the slider.</span></span> <span data-ttu-id="6aa07-111">Le posizioni logiche valide sono i valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="6aa07-111">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="6aa07-112">Se questo valore non è compreso nell'intervallo massimo e minimo del controllo, la posizione viene impostata sul valore massimo o minimo.</span><span class="sxs-lookup"><span data-stu-id="6aa07-112">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aa07-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6aa07-113">Return value</span></span>

<span data-ttu-id="6aa07-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="6aa07-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6aa07-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6aa07-115">Remarks</span></span>

<span data-ttu-id="6aa07-116">La chiamata a **TBM \_ SETPOSNOTIFY** imposterà la posizione del dispositivo di scorrimento TrackBar, ad esempio [**TBM \_ SETPOS**](tbm-setpos.md) , ma comporterà anche la notifica all'elemento padre di uno spostamento tramite un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="6aa07-116">Calling **TBM\_SETPOSNOTIFY** will set the trackbar slider location like [**TBM\_SETPOS**](tbm-setpos.md) would, but it will also cause the trackbar to notify its parent of a move via a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aa07-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6aa07-117">Requirements</span></span>



| <span data-ttu-id="6aa07-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aa07-118">Requirement</span></span> | <span data-ttu-id="6aa07-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6aa07-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa07-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aa07-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6aa07-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6aa07-121">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6aa07-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aa07-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6aa07-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6aa07-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6aa07-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6aa07-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6aa07-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aa07-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





