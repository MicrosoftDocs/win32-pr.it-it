---
title: Codice di notifica EN_OBJECTPOSITIONS (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit quando il controllo legge negli oggetti. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- Controlli di Windows per il codice di notifica EN_OBJECTPOSITIONS
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873906"
---
# <a name="en_objectpositions-notification-code"></a><span data-ttu-id="9ea32-105">\_Codice di notifica en OBJECTPOSITIONS</span><span class="sxs-lookup"><span data-stu-id="9ea32-105">EN\_OBJECTPOSITIONS notification code</span></span>

<span data-ttu-id="9ea32-106">Notifica alla finestra padre di un controllo Rich Edit quando il controllo legge negli oggetti.</span><span class="sxs-lookup"><span data-stu-id="9ea32-106">Notifies a rich edit control's parent window when the control reads in objects.</span></span> <span data-ttu-id="9ea32-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9ea32-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9ea32-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ea32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ea32-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ea32-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ea32-110">Struttura [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) .</span><span class="sxs-lookup"><span data-stu-id="9ea32-110">An [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ea32-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ea32-111">Return value</span></span>

<span data-ttu-id="9ea32-112">Restituisce zero per continuare l'operazione di **lettura** .</span><span class="sxs-lookup"><span data-stu-id="9ea32-112">Return zero to continue the **Read** operation.</span></span>

<span data-ttu-id="9ea32-113">Restituisce un valore diverso da zero per arrestare l'operazione di **lettura** .</span><span class="sxs-lookup"><span data-stu-id="9ea32-113">Return a nonzero value to stop the **Read** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ea32-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ea32-114">Remarks</span></span>

<span data-ttu-id="9ea32-115">Per ricevere un \_ codice di notifica en OBJECTPOSITIONS, specificare il flag [**ENM \_ OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio \_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="9ea32-115">To receive an EN\_OBJECTPOSITIONS notification code, specify the [**ENM\_OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ea32-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ea32-116">Requirements</span></span>



| <span data-ttu-id="9ea32-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ea32-117">Requirement</span></span> | <span data-ttu-id="9ea32-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9ea32-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea32-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ea32-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9ea32-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ea32-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ea32-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ea32-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9ea32-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ea32-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ea32-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ea32-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ea32-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ea32-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ea32-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ea32-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ea32-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9ea32-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ea32-127">**\_SETEVENTMASK em**</span><span class="sxs-lookup"><span data-stu-id="9ea32-127">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="9ea32-128">**OBJECTPOSITIONS**</span><span class="sxs-lookup"><span data-stu-id="9ea32-128">**OBJECTPOSITIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[<span data-ttu-id="9ea32-129">**\_notifica WM**</span><span class="sxs-lookup"><span data-stu-id="9ea32-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> <dt>

<span data-ttu-id="9ea32-130">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="9ea32-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="9ea32-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ea32-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9ea32-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ea32-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

