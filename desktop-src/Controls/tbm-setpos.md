---
title: Messaggio TBM_SETPOS (COMmctrl. h)
description: Imposta la posizione logica corrente del dispositivo di scorrimento in un TrackBar.
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- Controlli di Windows Message TBM_SETPOS
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
ms.openlocfilehash: e8e8da6e8e231a26b216ca8f9314d59474384857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964967"
---
# <a name="tbm_setpos-message"></a><span data-ttu-id="718d2-104">\_Messaggio SETPOS TBM</span><span class="sxs-lookup"><span data-stu-id="718d2-104">TBM\_SETPOS message</span></span>

<span data-ttu-id="718d2-105">Imposta la posizione logica corrente del dispositivo di scorrimento in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="718d2-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="718d2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="718d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="718d2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="718d2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="718d2-108">Ridisegni flag.</span><span class="sxs-lookup"><span data-stu-id="718d2-108">Redraw flag.</span></span> <span data-ttu-id="718d2-109">Se questo parametro è **true**, il messaggio riestrae il controllo con il dispositivo di scorrimento in corrispondenza della posizione specificata da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="718d2-109">If this parameter is **TRUE**, the message redraws the control with the slider at the position given by *lParam*.</span></span> <span data-ttu-id="718d2-110">Se questo parametro è **false**, il messaggio non ridisegnato il dispositivo di scorrimento nella nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="718d2-110">If this parameter is **FALSE**, the message does not redraw the slider at the new position.</span></span> <span data-ttu-id="718d2-111">Si noti che il messaggio imposta il valore della posizione del dispositivo di scorrimento (restituito dal messaggio [**TBM \_ GETPOS**](tbm-getpos.md) ) indipendentemente dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="718d2-111">Note that the message sets the value of the slider position (as returned by the [**TBM\_GETPOS**](tbm-getpos.md) message) regardless of the *wParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="718d2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="718d2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="718d2-113">Nuova posizione logica del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="718d2-113">New logical position of the slider.</span></span> <span data-ttu-id="718d2-114">Le posizioni logiche valide sono i valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="718d2-114">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="718d2-115">Se questo valore non è compreso nell'intervallo massimo e minimo del controllo, la posizione viene impostata sul valore massimo o minimo.</span><span class="sxs-lookup"><span data-stu-id="718d2-115">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="718d2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="718d2-116">Return value</span></span>

<span data-ttu-id="718d2-117">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="718d2-117">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="718d2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="718d2-118">Requirements</span></span>



| <span data-ttu-id="718d2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="718d2-119">Requirement</span></span> | <span data-ttu-id="718d2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="718d2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="718d2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="718d2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="718d2-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="718d2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="718d2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="718d2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="718d2-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="718d2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="718d2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="718d2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="718d2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="718d2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





