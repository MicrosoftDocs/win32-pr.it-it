---
title: Messaggio TBM_GETTICPOS (COMmctrl. h)
description: Recupera la posizione fisica corrente di un segno di graduazione in un TrackBar.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- Controlli di Windows Message TBM_GETTICPOS
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301664"
---
# <a name="tbm_getticpos-message"></a><span data-ttu-id="9bc29-104">\_Messaggio GETTICPOS TBM</span><span class="sxs-lookup"><span data-stu-id="9bc29-104">TBM\_GETTICPOS message</span></span>

<span data-ttu-id="9bc29-105">Recupera la posizione fisica corrente di un segno di graduazione in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="9bc29-105">Retrieves the current physical position of a tick mark in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9bc29-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bc29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bc29-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9bc29-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bc29-108">Indice in base zero che identifica un segno di graduazione.</span><span class="sxs-lookup"><span data-stu-id="9bc29-108">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="9bc29-109">Le posizioni del primo e dell'ultimo segno di graduazione non sono direttamente disponibili tramite questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="9bc29-109">The positions of the first and last tick marks are not directly available via this message.</span></span>

</dd> <dt>

<span data-ttu-id="9bc29-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9bc29-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bc29-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9bc29-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bc29-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bc29-112">Return value</span></span>

<span data-ttu-id="9bc29-113">Restituisce la distanza, espressa in coordinate client, dal lato sinistro o superiore dell'area client del TrackBar al segno di graduazione specificato.</span><span class="sxs-lookup"><span data-stu-id="9bc29-113">Returns the distance, in client coordinates, from the left or top of the trackbar's client area to the specified tick mark.</span></span> <span data-ttu-id="9bc29-114">Il valore restituito è la coordinata x del segno di graduazione per un TrackBar orizzontale o la coordinata y di un TrackBar verticale.</span><span class="sxs-lookup"><span data-stu-id="9bc29-114">The return value is the x-coordinate of the tick mark for a horizontal trackbar or the y-coordinate for a vertical trackbar.</span></span> <span data-ttu-id="9bc29-115">Se *wParam* non è un indice valido, il valore restituito è-1.</span><span class="sxs-lookup"><span data-stu-id="9bc29-115">If *wParam* is not a valid index, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bc29-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bc29-116">Remarks</span></span>

<span data-ttu-id="9bc29-117">Poiché il primo e l'ultimo segno di graduazione non sono disponibili tramite questo messaggio, gli indici validi vengono spostati rispetto alla relativa posizione di graduazione nel TrackBar.</span><span class="sxs-lookup"><span data-stu-id="9bc29-117">Because the first and last tick marks are not available through this message, valid indexes are offset from their tick position on the trackbar.</span></span> <span data-ttu-id="9bc29-118">Se la differenza tra [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md) e [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) è minore di due, non esiste alcun indice valido e questo messaggio avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9bc29-118">If the difference between [**TBM\_GETRANGEMIN**](tbm-getrangemin.md) and [**TBM\_GETRANGEMAX**](tbm-getrangemax.md) is less than two, then there is no valid index and this message will fail.</span></span>

<span data-ttu-id="9bc29-119">Nell'esempio seguente viene illustrata la relazione tra i cicli di un TrackBar, i segni di avanzamento disponibili tramite questo messaggio e gli indici in base zero.</span><span class="sxs-lookup"><span data-stu-id="9bc29-119">The following illustrates the relation between the ticks on a trackbar, the ticks available through this message, and their zero-based indexes.</span></span>

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a><span data-ttu-id="9bc29-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bc29-120">Requirements</span></span>



| <span data-ttu-id="9bc29-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bc29-121">Requirement</span></span> | <span data-ttu-id="9bc29-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9bc29-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc29-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bc29-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9bc29-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9bc29-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9bc29-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bc29-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9bc29-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9bc29-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9bc29-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bc29-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bc29-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bc29-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





