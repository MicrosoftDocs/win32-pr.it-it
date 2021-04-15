---
title: Messaggio TBM_GETPOS (COMmctrl. h)
description: Recupera la posizione logica corrente del dispositivo di scorrimento in un TrackBar. Le posizioni logiche sono i valori integer nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- Controlli di Windows Message TBM_GETPOS
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ff9b8a107fe19afb1fee6107a2f05bad36025
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476805"
---
# <a name="tbm_getpos-message"></a><span data-ttu-id="033bd-105">\_Messaggio GETPOS TBM</span><span class="sxs-lookup"><span data-stu-id="033bd-105">TBM\_GETPOS message</span></span>

<span data-ttu-id="033bd-106">Recupera la posizione logica corrente del dispositivo di scorrimento in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="033bd-106">Retrieves the current logical position of the slider in a trackbar.</span></span> <span data-ttu-id="033bd-107">Le posizioni logiche sono i valori integer nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="033bd-107">The logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="033bd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="033bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="033bd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="033bd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="033bd-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="033bd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="033bd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="033bd-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="033bd-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="033bd-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="033bd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="033bd-113">Return value</span></span>

<span data-ttu-id="033bd-114">Restituisce un valore a 32 bit che specifica la posizione logica corrente del dispositivo di scorrimento del TrackBar.</span><span class="sxs-lookup"><span data-stu-id="033bd-114">Returns a 32-bit value that specifies the current logical position of the trackbar's slider.</span></span>

## <a name="requirements"></a><span data-ttu-id="033bd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="033bd-115">Requirements</span></span>



| <span data-ttu-id="033bd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="033bd-116">Requirement</span></span> | <span data-ttu-id="033bd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="033bd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="033bd-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="033bd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="033bd-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="033bd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="033bd-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="033bd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="033bd-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="033bd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="033bd-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="033bd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="033bd-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="033bd-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="033bd-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="033bd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="033bd-125">**TBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="033bd-125">**TBM\_SETPOS**</span></span>](tbm-setpos.md)
</dt> </dl>

 

 





