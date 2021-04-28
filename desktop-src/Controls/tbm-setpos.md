---
title: TBM_SETPOS messaggio (Commctrl.h)
description: 'TBM_SETPOS: imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar.'
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS di windows del messaggio
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f10e05a677119f18489d0eb9eebc4528d3ad115
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085869"
---
# <a name="tbm_setpos-message"></a><span data-ttu-id="142d3-104">Messaggio \_ SETPOS TBM</span><span class="sxs-lookup"><span data-stu-id="142d3-104">TBM\_SETPOS message</span></span>

<span data-ttu-id="142d3-105">Imposta la posizione logica corrente del dispositivo di scorrimento in un trackbar.</span><span class="sxs-lookup"><span data-stu-id="142d3-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="142d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="142d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="142d3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="142d3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="142d3-108">Flag di ridisegno.</span><span class="sxs-lookup"><span data-stu-id="142d3-108">Redraw flag.</span></span> <span data-ttu-id="142d3-109">Se questo parametro è **TRUE,** il messaggio ridisegna il controllo con il dispositivo di scorrimento nella posizione specificata da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="142d3-109">If this parameter is **TRUE**, the message redraws the control with the slider at the position given by *lParam*.</span></span> <span data-ttu-id="142d3-110">Se questo parametro è **FALSE,** il messaggio non ridisegna il dispositivo di scorrimento nella nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="142d3-110">If this parameter is **FALSE**, the message does not redraw the slider at the new position.</span></span> <span data-ttu-id="142d3-111">Si noti che il messaggio imposta il valore della posizione del dispositivo di scorrimento (come restituito dal messaggio [**\_ GETPOS TBM)**](tbm-getpos.md) indipendentemente dal *parametro wParam.*</span><span class="sxs-lookup"><span data-stu-id="142d3-111">Note that the message sets the value of the slider position (as returned by the [**TBM\_GETPOS**](tbm-getpos.md) message) regardless of the *wParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="142d3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="142d3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="142d3-113">Nuova posizione logica del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="142d3-113">New logical position of the slider.</span></span> <span data-ttu-id="142d3-114">Le posizioni logiche valide sono i valori interi nell'intervallo di posizioni del dispositivo di scorrimento minimo e massimo del trackbar.</span><span class="sxs-lookup"><span data-stu-id="142d3-114">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="142d3-115">Se questo valore non rientra nell'intervallo massimo e minimo del controllo, la posizione viene impostata sul valore massimo o minimo.</span><span class="sxs-lookup"><span data-stu-id="142d3-115">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="142d3-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="142d3-116">Return value</span></span>

<span data-ttu-id="142d3-117">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="142d3-117">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="142d3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="142d3-118">Requirements</span></span>



| <span data-ttu-id="142d3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="142d3-119">Requirement</span></span> | <span data-ttu-id="142d3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="142d3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="142d3-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="142d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="142d3-122">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="142d3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="142d3-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="142d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="142d3-124">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="142d3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="142d3-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="142d3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="142d3-126"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="142d3-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





