---
title: Messaggio TBM_SETTIPSIDE (COMmctrl. h)
description: Posiziona un controllo ToolTip utilizzato da un controllo TrackBar. I controlli TrackBar che usano le descrizioni comandi di TBS \_ visualizzano le descrizioni comandi.
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- Controlli di Windows Message TBM_SETTIPSIDE
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400426"
---
# <a name="tbm_settipside-message"></a><span data-ttu-id="c194c-105">\_Messaggio SETTIPSIDE TBM</span><span class="sxs-lookup"><span data-stu-id="c194c-105">TBM\_SETTIPSIDE message</span></span>

<span data-ttu-id="c194c-106">Posiziona un controllo ToolTip utilizzato da un controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c194c-106">Positions a tooltip control used by a trackbar control.</span></span> <span data-ttu-id="c194c-107">I controlli TrackBar che usano le descrizioni comandi di [**TBS \_**](trackbar-control-styles.md) visualizzano le descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="c194c-107">Trackbar controls that use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style display tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="c194c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c194c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c194c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c194c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c194c-110">Valore che rappresenta la posizione in cui visualizzare il controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="c194c-110">Value representing the location at which to display the tooltip control.</span></span> <span data-ttu-id="c194c-111">I valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c194c-111">This value can be one of the following:</span></span>



| <span data-ttu-id="c194c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c194c-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="c194c-113">Significato</span><span class="sxs-lookup"><span data-stu-id="c194c-113">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <span data-ttu-id="c194c-114"><dt>**TBTS \_ Top**</dt></span><span class="sxs-lookup"><span data-stu-id="c194c-114"><dt>**TBTS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="c194c-115">Il controllo ToolTip verrà posizionato sopra l'oggetto TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c194c-115">The tooltip control will be positioned above the trackbar.</span></span> <span data-ttu-id="c194c-116">Questo flag viene utilizzato con gli TrackBar orizzontali.</span><span class="sxs-lookup"><span data-stu-id="c194c-116">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <span data-ttu-id="c194c-117"><dt>**TBTS a \_ sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="c194c-117"><dt>**TBTS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="c194c-118">Il controllo ToolTip verrà posizionato a sinistra del controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c194c-118">The tooltip control will be positioned to the left of the trackbar.</span></span> <span data-ttu-id="c194c-119">Questo flag viene utilizzato con gli TrackBar verticali.</span><span class="sxs-lookup"><span data-stu-id="c194c-119">This flag is for use with vertical trackbars.</span></span><br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <span data-ttu-id="c194c-120"><dt>**TBTS in \_ basso**</dt></span><span class="sxs-lookup"><span data-stu-id="c194c-120"><dt>**TBTS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="c194c-121">Il controllo ToolTip verrà posizionato al di sotto del TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c194c-121">The tooltip control will be positioned below the trackbar.</span></span> <span data-ttu-id="c194c-122">Questo flag viene utilizzato con gli TrackBar orizzontali.</span><span class="sxs-lookup"><span data-stu-id="c194c-122">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <span data-ttu-id="c194c-123"><dt>**TBTS a \_ destra**</dt></span><span class="sxs-lookup"><span data-stu-id="c194c-123"><dt>**TBTS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="c194c-124">Il controllo ToolTip verrà posizionato a destra dell'oggetto TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c194c-124">The tooltip control will be positioned to the right of the trackbar.</span></span> <span data-ttu-id="c194c-125">Questo flag viene utilizzato con gli TrackBar verticali.</span><span class="sxs-lookup"><span data-stu-id="c194c-125">This flag is for use with vertical trackbars.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c194c-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c194c-126">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c194c-127">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c194c-127">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c194c-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c194c-128">Return value</span></span>

<span data-ttu-id="c194c-129">Restituisce un valore che rappresenta la posizione precedente del controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="c194c-129">Returns a value that represents the tooltip control's previous location.</span></span> <span data-ttu-id="c194c-130">Il valore restituito è uguale a uno dei valori possibili per *wParam*.</span><span class="sxs-lookup"><span data-stu-id="c194c-130">The return value equals one of the possible values for *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="c194c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c194c-131">Requirements</span></span>



| <span data-ttu-id="c194c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c194c-132">Requirement</span></span> | <span data-ttu-id="c194c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c194c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c194c-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c194c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c194c-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c194c-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c194c-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c194c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c194c-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c194c-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c194c-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c194c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c194c-139"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c194c-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





