---
title: Messaggio TBM_SETBUDDY (COMmctrl. h)
description: Assegna una finestra come finestra di Buddy per un controllo TrackBar. Le finestre del contatto TrackBar vengono visualizzate automaticamente in un percorso relativo all'orientamento del controllo (orizzontale o verticale).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- Controlli di Windows Message TBM_SETBUDDY
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33e53117933390d7a34ec75a49724003255108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048064"
---
# <a name="tbm_setbuddy-message"></a><span data-ttu-id="e5ce7-105">\_Messaggio SEBUDDY TBM</span><span class="sxs-lookup"><span data-stu-id="e5ce7-105">TBM\_SETBUDDY message</span></span>

<span data-ttu-id="e5ce7-106">Assegna una finestra come finestra di Buddy per un controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e5ce7-106">Assigns a window as the buddy window for a trackbar control.</span></span> <span data-ttu-id="e5ce7-107">Le finestre del contatto TrackBar vengono visualizzate automaticamente in un percorso relativo all'orientamento del controllo (orizzontale o verticale).</span><span class="sxs-lookup"><span data-stu-id="e5ce7-107">Trackbar buddy windows are automatically displayed in a location relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="e5ce7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5ce7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5ce7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5ce7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5ce7-110">Valore che specifica la posizione in cui visualizzare la finestra di Buddy.</span><span class="sxs-lookup"><span data-stu-id="e5ce7-110">Value specifying the location at which to display the buddy window.</span></span> <span data-ttu-id="e5ce7-111">I valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5ce7-111">This value can be one of the following:</span></span>



| <span data-ttu-id="e5ce7-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e5ce7-112">Value</span></span>                                                                                                                                | <span data-ttu-id="e5ce7-113">Significato</span><span class="sxs-lookup"><span data-stu-id="e5ce7-113">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="e5ce7-114"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ce7-114"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="e5ce7-115">L'oggetto Buddy verrà visualizzato a sinistra del controllo TrackBar se il controllo TrackBar usa lo [**stile \_ orizzontalmente di TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e5ce7-115">The buddy will appear to the left of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="e5ce7-116">Se il controllo TrackBar usa lo stile di [**TBS \_ Vert**](trackbar-control-styles.md) , il contatto viene visualizzato sopra il controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e5ce7-116">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears above the trackbar control.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="e5ce7-117"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ce7-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="e5ce7-118">L'oggetto Buddy verrà visualizzato a destra del controllo TrackBar se il controllo TrackBar usa lo [**stile \_ orizzontalmente di TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e5ce7-118">The buddy will appear to the right of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="e5ce7-119">Se il controllo TrackBar utilizza lo stile di [**TBS \_ Vert**](trackbar-control-styles.md) , l'oggetto Buddy viene visualizzato sotto il controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e5ce7-119">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears below the trackbar control.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e5ce7-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5ce7-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5ce7-121">Handle per la finestra che verrà impostata come Buddy del controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e5ce7-121">Handle to the window that will be set as the trackbar control's buddy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5ce7-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5ce7-122">Return value</span></span>

<span data-ttu-id="e5ce7-123">Restituisce l'handle alla finestra precedentemente assegnata al controllo in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="e5ce7-123">Returns the handle to the window that was previously assigned to the control at that location.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5ce7-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5ce7-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e5ce7-125">I controlli TrackBar supportano fino a due finestre di contatto.</span><span class="sxs-lookup"><span data-stu-id="e5ce7-125">Trackbar controls support up to two buddy windows.</span></span> <span data-ttu-id="e5ce7-126">Questa operazione può essere utile quando è necessario visualizzare testo o immagini a ogni estremità del controllo.</span><span class="sxs-lookup"><span data-stu-id="e5ce7-126">This can be useful when you must display text or images at each end of the control.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5ce7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5ce7-127">Requirements</span></span>



| <span data-ttu-id="e5ce7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5ce7-128">Requirement</span></span> | <span data-ttu-id="e5ce7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e5ce7-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ce7-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5ce7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e5ce7-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5ce7-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e5ce7-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5ce7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e5ce7-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e5ce7-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5ce7-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5ce7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5ce7-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ce7-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





