---
title: Codice di notifica EN_SEARCHWEB (CommCtrl. h)
description: Inviato quando un controllo di modifica perde lo stato attivo della tastiera. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un \_ messaggio di notifica WM.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- Controlli di Windows per il codice di notifica EN_SEARCHWEB
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475388"
---
# <a name="en_searchweb-notification-code"></a><span data-ttu-id="78065-105">\_Codice di notifica en SEARCHWEB</span><span class="sxs-lookup"><span data-stu-id="78065-105">EN\_SEARCHWEB notification code</span></span>

<span data-ttu-id="78065-106">Inviato dopo che un controllo di modifica ha eseguito una ricerca Web quando è abilitata la funzionalità "Cerca sul Web", vedere [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span><span class="sxs-lookup"><span data-stu-id="78065-106">Sent after an edit control performed a web search when the "Search the web" feature is enabled, see [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span></span> <span data-ttu-id="78065-107">La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="78065-107">The parent window of the edit control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="78065-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="78065-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78065-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78065-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78065-110">Handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="78065-110">Handle to the edit control.</span></span>

</dd> <dt>

<span data-ttu-id="78065-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78065-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78065-112">Puntatore a una struttura [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) .</span><span class="sxs-lookup"><span data-stu-id="78065-112">A pointer to a [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78065-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78065-113">Requirements</span></span>



| <span data-ttu-id="78065-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="78065-114">Requirement</span></span> | <span data-ttu-id="78065-115">Valore</span><span class="sxs-lookup"><span data-stu-id="78065-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78065-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78065-116">Minimum supported client</span></span><br/> | <span data-ttu-id="78065-117">Solo app desktop Windows 10, 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="78065-117">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="78065-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78065-118">Minimum supported server</span></span><br/> | <span data-ttu-id="78065-119">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="78065-119">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="78065-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78065-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="78065-121"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="78065-121"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78065-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78065-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="78065-123">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="78065-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78065-124">**\_ENABLESEARCHWEB em**</span><span class="sxs-lookup"><span data-stu-id="78065-124">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> <dt>

<span data-ttu-id="78065-125">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="78065-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="78065-126">**\_notifica WM**</span><span class="sxs-lookup"><span data-stu-id="78065-126">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





