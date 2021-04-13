---
title: Codice di notifica EN_LOWFIRTF (RichEdit. h)
description: Notifica alla finestra padre di un controllo Microsoft Rich Edit che è stata ricevuta una parola chiave RTF (Rich Text Format) non supportata. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- Controlli di Windows per il codice di notifica EN_LOWFIRTF
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74a6e5dada471fdd8364b34bf2ed1b4da7f2314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518663"
---
# <a name="en_lowfirtf-notification-code"></a><span data-ttu-id="e26c1-105">\_Codice di notifica en LOWFIRTF</span><span class="sxs-lookup"><span data-stu-id="e26c1-105">EN\_LOWFIRTF notification code</span></span>

<span data-ttu-id="e26c1-106">Notifica alla finestra padre di un controllo Microsoft Rich Edit che è stata ricevuta una parola chiave RTF (Rich Text Format) non supportata.</span><span class="sxs-lookup"><span data-stu-id="e26c1-106">Notifies the parent window of a Microsoft Rich Edit control that an unsupported Rich Text Format (RTF) keyword was received.</span></span> <span data-ttu-id="e26c1-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e26c1-107">A Rich Edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e26c1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e26c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e26c1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e26c1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e26c1-110">Struttura [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) .</span><span class="sxs-lookup"><span data-stu-id="e26c1-110">The [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e26c1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e26c1-111">Return value</span></span>

<span data-ttu-id="e26c1-112">Questo codice di notifica non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="e26c1-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e26c1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e26c1-113">Remarks</span></span>

<span data-ttu-id="e26c1-114">Per ricevere una \_ notifica en LOWFIRTF, specificare il \_ flag ENM LOWFIRTF nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="e26c1-114">To receive an EN\_LOWFIRTF notification, specify the ENM\_LOWFIRTF flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e26c1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e26c1-115">Requirements</span></span>



| <span data-ttu-id="e26c1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e26c1-116">Requirement</span></span> | <span data-ttu-id="e26c1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e26c1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e26c1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e26c1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e26c1-119">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="e26c1-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e26c1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e26c1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e26c1-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e26c1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e26c1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e26c1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e26c1-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e26c1-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e26c1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e26c1-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="e26c1-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e26c1-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e26c1-126">**ENLOWFIRTF**</span><span class="sxs-lookup"><span data-stu-id="e26c1-126">**ENLOWFIRTF**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[<span data-ttu-id="e26c1-127">**\_notifica WM**</span><span class="sxs-lookup"><span data-stu-id="e26c1-127">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





