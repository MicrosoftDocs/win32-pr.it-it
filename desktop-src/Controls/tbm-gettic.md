---
title: Messaggio TBM_GETTIC (COMmctrl. h)
description: Recupera la posizione logica di un segno di graduazione in un TrackBar. La posizione logica può essere uno qualsiasi dei valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- Controlli di Windows Message TBM_GETTIC
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d534d5100e20cc544c31fca2fc9e49cda3bd976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476798"
---
# <a name="tbm_gettic-message"></a><span data-ttu-id="b9710-105">\_Messaggio Getter TBM</span><span class="sxs-lookup"><span data-stu-id="b9710-105">TBM\_GETTIC message</span></span>

<span data-ttu-id="b9710-106">Recupera la posizione logica di un segno di graduazione in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b9710-106">Retrieves the logical position of a tick mark in a trackbar.</span></span> <span data-ttu-id="b9710-107">La posizione logica può essere uno qualsiasi dei valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="b9710-107">The logical position can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9710-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9710-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9710-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9710-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9710-110">Indice in base zero che identifica un segno di graduazione.</span><span class="sxs-lookup"><span data-stu-id="b9710-110">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="b9710-111">Gli indici validi sono compresi nell'intervallo da zero a due minori rispetto al conteggio restituito dal messaggio [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) .</span><span class="sxs-lookup"><span data-stu-id="b9710-111">Valid indexes are in the range from zero to two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="b9710-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9710-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b9710-113">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b9710-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9710-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9710-114">Return value</span></span>

<span data-ttu-id="b9710-115">Restituisce la posizione logica del segno di graduazione specificato oppure-1 se *wParam* non specifica un indice valido.</span><span class="sxs-lookup"><span data-stu-id="b9710-115">Returns the logical position of the specified tick mark, or -1 if *wParam* does not specify a valid index.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9710-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9710-116">Requirements</span></span>



| <span data-ttu-id="b9710-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9710-117">Requirement</span></span> | <span data-ttu-id="b9710-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b9710-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b9710-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9710-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b9710-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9710-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b9710-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9710-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b9710-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b9710-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b9710-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9710-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9710-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9710-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





