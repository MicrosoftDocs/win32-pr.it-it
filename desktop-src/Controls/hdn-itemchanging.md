---
title: Codice di notifica HDN_ITEMCHANGING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che gli attributi di un elemento di intestazione stanno per essere modificati. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- Controlli di Windows per il codice di notifica HDN_ITEMCHANGING
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873377"
---
# <a name="hdn_itemchanging-notification-code"></a><span data-ttu-id="fe035-105">\_Codice di notifica ITEMCHANGING di HDN</span><span class="sxs-lookup"><span data-stu-id="fe035-105">HDN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="fe035-106">Notifica alla finestra padre di un controllo di intestazione che gli attributi di un elemento di intestazione stanno per essere modificati.</span><span class="sxs-lookup"><span data-stu-id="fe035-106">Notifies a header control's parent window that the attributes of a header item are about to change.</span></span> <span data-ttu-id="fe035-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fe035-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fe035-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe035-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe035-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe035-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe035-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sul controllo intestazione e sull'elemento intestazione, inclusi gli attributi che stanno per essere modificati.</span><span class="sxs-lookup"><span data-stu-id="fe035-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe035-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe035-111">Return value</span></span>

<span data-ttu-id="fe035-112">Restituisce **false** per consentire le modifiche o **true** per impedirne l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fe035-112">Returns **FALSE** to allow the changes, or **TRUE** to prevent them.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe035-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe035-113">Requirements</span></span>



| <span data-ttu-id="fe035-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe035-114">Requirement</span></span> | <span data-ttu-id="fe035-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fe035-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe035-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe035-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe035-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe035-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe035-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe035-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe035-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe035-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe035-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe035-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe035-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe035-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fe035-122">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="fe035-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fe035-123">**HDN \_ ITEMCHANGINGW** (Unicode) e **HDN \_ ITEMCHANGINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fe035-123">**HDN\_ITEMCHANGINGW** (Unicode) and **HDN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



 

 





