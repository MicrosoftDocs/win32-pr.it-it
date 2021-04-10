---
title: Messaggio PBM_SETMARQUEE (COMmctrl. h)
description: Imposta l'indicatore di stato sulla modalità marquee. Questo fa sì che l'indicatore di stato si sposti come un Marquee.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- Controlli di Windows Message PBM_SETMARQUEE
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964563"
---
# <a name="pbm_setmarquee-message"></a><span data-ttu-id="5ca32-105">\_Messaggio di RISELEZIONE PBM</span><span class="sxs-lookup"><span data-stu-id="5ca32-105">PBM\_SETMARQUEE message</span></span>

<span data-ttu-id="5ca32-106">Imposta l'indicatore di stato sulla modalità marquee.</span><span class="sxs-lookup"><span data-stu-id="5ca32-106">Sets the progress bar to marquee mode.</span></span> <span data-ttu-id="5ca32-107">Questo fa sì che l'indicatore di stato si sposti come un Marquee.</span><span class="sxs-lookup"><span data-stu-id="5ca32-107">This causes the progress bar to move like a marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ca32-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ca32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca32-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ca32-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ca32-110">Indica se attivare o disattivare la modalità marquee.</span><span class="sxs-lookup"><span data-stu-id="5ca32-110">Indicates whether to turn the marquee mode on or off.</span></span>

</dd> <dt>

<span data-ttu-id="5ca32-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ca32-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5ca32-112">Tempo, in millisecondi, tra gli aggiornamenti di animazione Marquee.</span><span class="sxs-lookup"><span data-stu-id="5ca32-112">Time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="5ca32-113">Se questo parametro è zero, l'animazione Marquee viene aggiornata ogni 30 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="5ca32-113">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca32-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ca32-114">Return value</span></span>

<span data-ttu-id="5ca32-115">Restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="5ca32-115">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ca32-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ca32-116">Remarks</span></span>

<span data-ttu-id="5ca32-117">Utilizzare questo messaggio quando non si conosce la quantità di avanzamento verso il completamento, ma si desidera indicare che lo stato di avanzamento è stato eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ca32-117">Use this message when you do not know the amount of progress toward completion but wish to indicate that progress is being made.</span></span>

<span data-ttu-id="5ca32-118">Inviare il **messaggio \_ per** l'avvio o l'arresto dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="5ca32-118">Send the **PBM\_SETMARQUEE** message to start or stop the animation.</span></span>

> [!Note]  
> <span data-ttu-id="5ca32-119">È necessario impostare lo stile del controllo su [**PBS \_ Marquee**](progress-bar-control-styles.md) prima di provare ad avviare l'animazione.</span><span class="sxs-lookup"><span data-stu-id="5ca32-119">You must set the control style to [**PBS\_MARQUEE**](progress-bar-control-styles.md) before attempting to start the animation.</span></span>

 

> [!Note]  
> <span data-ttu-id="5ca32-120">Per questo messaggio è necessario ComCtl32.dll versione 6,00 o successiva.</span><span class="sxs-lookup"><span data-stu-id="5ca32-120">This message requires ComCtl32.dll version 6.00 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ca32-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ca32-121">Requirements</span></span>



| <span data-ttu-id="5ca32-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ca32-122">Requirement</span></span> | <span data-ttu-id="5ca32-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5ca32-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca32-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ca32-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca32-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ca32-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5ca32-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ca32-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca32-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5ca32-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5ca32-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ca32-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ca32-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ca32-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





