---
title: TBM_SETPOSNOTIFY messaggio (Commctrl.h)
description: 'TBM_SETPOSNOTIFY messaggio: imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar.'
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY messaggio Controlli Windows
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
ms.openlocfilehash: 7201f3056ed05e6321ab9d9bd726edc3b4470f0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104079"
---
# <a name="tbm_setposnotify-message"></a><span data-ttu-id="9185b-104">Messaggio \_ TBM SETPOSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="9185b-104">TBM\_SETPOSNOTIFY message</span></span>

<span data-ttu-id="9185b-105">Imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar.</span><span class="sxs-lookup"><span data-stu-id="9185b-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9185b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9185b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9185b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9185b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9185b-108">wParam non viene usato.</span><span class="sxs-lookup"><span data-stu-id="9185b-108">wParam is unused.</span></span>

</dd> <dt>

<span data-ttu-id="9185b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9185b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9185b-110">Nuova posizione logica del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9185b-110">New logical position of the slider.</span></span> <span data-ttu-id="9185b-111">Le posizioni logiche valide sono i valori interi nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento del trackbar.</span><span class="sxs-lookup"><span data-stu-id="9185b-111">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="9185b-112">Se questo valore non rientra nell'intervallo massimo e minimo del controllo, la posizione viene impostata sul valore massimo o minimo.</span><span class="sxs-lookup"><span data-stu-id="9185b-112">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9185b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9185b-113">Return value</span></span>

<span data-ttu-id="9185b-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="9185b-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9185b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9185b-115">Remarks</span></span>

<span data-ttu-id="9185b-116">La chiamata a **TBM \_ SETPOSNOTIFY** imposta la posizione del dispositivo di scorrimento del trackbar come farebbe [**TBM \_ SETPOS,**](tbm-setpos.md) ma determina anche la notifica del trackbar all'elemento padre di uno spostamento tramite un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL.**](wm-vscroll.md)</span><span class="sxs-lookup"><span data-stu-id="9185b-116">Calling **TBM\_SETPOSNOTIFY** will set the trackbar slider location like [**TBM\_SETPOS**](tbm-setpos.md) would, but it will also cause the trackbar to notify its parent of a move via a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9185b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9185b-117">Requirements</span></span>



| <span data-ttu-id="9185b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9185b-118">Requirement</span></span> | <span data-ttu-id="9185b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9185b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9185b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9185b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9185b-121">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9185b-121">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9185b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9185b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9185b-123">Solo app desktop di Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9185b-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9185b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9185b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9185b-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="9185b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





