---
title: Messaggio ACM_PLAY (COMmctrl. h)
description: Riproduce un clip AVI in un controllo dell'animazione. Il controllo riproduce il clip in background mentre il thread continua l'esecuzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro animazione.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- Controlli di Windows Message ACM_PLAY
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475760"
---
# <a name="acm_play-message"></a><span data-ttu-id="cc057-106">\_Messaggio di riproduzione ACM</span><span class="sxs-lookup"><span data-stu-id="cc057-106">ACM\_PLAY message</span></span>

<span data-ttu-id="cc057-107">Riproduce un clip AVI in un controllo dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="cc057-107">Plays an AVI clip in an animation control.</span></span> <span data-ttu-id="cc057-108">Il controllo riproduce il clip in background mentre il thread continua l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cc057-108">The control plays the clip in the background while the thread continues executing.</span></span> <span data-ttu-id="cc057-109">È possibile inviare questo messaggio in modo esplicito o utilizzando [**\_ la macro animazione**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .</span><span class="sxs-lookup"><span data-stu-id="cc057-109">You can send this message explicitly or by using the [**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc057-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc057-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc057-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc057-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc057-112">**Uint** che specifica il numero di volte in cui riprodurre il clip AVI.</span><span class="sxs-lookup"><span data-stu-id="cc057-112">A **UINT** that specifies the number of times to replay the AVI clip.</span></span> <span data-ttu-id="cc057-113">Il valore-1 indica la riproduzione illimitata del clip.</span><span class="sxs-lookup"><span data-stu-id="cc057-113">A value of -1 means replay the clip indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="cc057-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc057-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc057-115">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è l'indice in base zero del frame in cui inizia la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="cc057-115">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the zero-based index of the frame where playing begins.</span></span> <span data-ttu-id="cc057-116">Il valore deve essere minore di 65.536.</span><span class="sxs-lookup"><span data-stu-id="cc057-116">The value must be less than 65,536.</span></span> <span data-ttu-id="cc057-117">Il valore zero indica che iniziano con il primo fotogramma del clip AVI.</span><span class="sxs-lookup"><span data-stu-id="cc057-117">A value of zero means begin with the first frame in the AVI clip.</span></span>

<span data-ttu-id="cc057-118">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è l'indice in base zero del frame in cui termina la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="cc057-118">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the zero-based index of the frame where playing ends.</span></span> <span data-ttu-id="cc057-119">Il valore deve essere minore di 65.536.</span><span class="sxs-lookup"><span data-stu-id="cc057-119">The value must be less than 65,536.</span></span> <span data-ttu-id="cc057-120">Il valore-1 indica che termina con l'ultimo frame del clip AVI.</span><span class="sxs-lookup"><span data-stu-id="cc057-120">A value of -1 means end with the last frame in the AVI clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc057-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc057-121">Return value</span></span>

<span data-ttu-id="cc057-122">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cc057-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc057-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc057-123">Remarks</span></span>

<span data-ttu-id="cc057-124">È possibile usare [**animate \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) per indirizzare il controllo dell'animazione in modo da visualizzare un particolare frame del clip AVI.</span><span class="sxs-lookup"><span data-stu-id="cc057-124">You can use [**Animate\_Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) to direct the animation control to display a particular frame of the AVI clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc057-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc057-125">Requirements</span></span>



| <span data-ttu-id="cc057-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc057-126">Requirement</span></span> | <span data-ttu-id="cc057-127">Valore</span><span class="sxs-lookup"><span data-stu-id="cc057-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc057-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc057-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cc057-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc057-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc057-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc057-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cc057-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cc057-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc057-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc057-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc057-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc057-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

