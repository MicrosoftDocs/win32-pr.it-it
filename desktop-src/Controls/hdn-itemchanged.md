---
title: Codice di notifica HDN_ITEMCHANGED (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che gli attributi di un elemento di intestazione sono stati modificati. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ab707010-8ed2-4575-8233-8a1f5656e498
keywords:
- Controlli di Windows per il codice di notifica HDN_ITEMCHANGED
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGED
- HDN_ITEMCHANGEDA
- HDN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67157ff7f775c124236b7a77a1051b7644758c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047936"
---
# <a name="hdn_itemchanged-notification-code"></a><span data-ttu-id="8911d-105">\_Codice di notifica ITEMCHANGED di HDN</span><span class="sxs-lookup"><span data-stu-id="8911d-105">HDN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="8911d-106">Notifica alla finestra padre di un controllo di intestazione che gli attributi di un elemento di intestazione sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="8911d-106">Notifies a header control's parent window that the attributes of a header item have changed.</span></span> <span data-ttu-id="8911d-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8911d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGED

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8911d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8911d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8911d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8911d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8911d-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni sul controllo intestazione, inclusi gli attributi che sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="8911d-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control, including the attributes that have changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8911d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8911d-111">Return value</span></span>

<span data-ttu-id="8911d-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="8911d-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8911d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8911d-113">Requirements</span></span>



| <span data-ttu-id="8911d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8911d-114">Requirement</span></span> | <span data-ttu-id="8911d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8911d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8911d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8911d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8911d-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8911d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8911d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8911d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8911d-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8911d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8911d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8911d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8911d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8911d-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8911d-122">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8911d-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8911d-123">**HDN \_ ITEMCHANGEDW** (Unicode) e **HDN \_ ITEMCHANGEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8911d-123">**HDN\_ITEMCHANGEDW** (Unicode) and **HDN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



 

 





