---
title: Codice di notifica RBN_LAYOUTCHANGED (COMmctrl. h)
description: Inviato da un controllo Rebar quando l'utente modifica il layout delle bande del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e937d151-bfaa-41c0-a134-e70ff2f75d07
keywords:
- Controlli di Windows per il codice di notifica RBN_LAYOUTCHANGED
topic_type:
- apiref
api_name:
- RBN_LAYOUTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1fc14578435fc786ecc5496cec96eb2224b4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120498"
---
# <a name="rbn_layoutchanged-notification-code"></a><span data-ttu-id="8e835-105">\_Codice di notifica LAYOUTCHANGED di RBN</span><span class="sxs-lookup"><span data-stu-id="8e835-105">RBN\_LAYOUTCHANGED notification code</span></span>

<span data-ttu-id="8e835-106">Inviato da un controllo Rebar quando l'utente modifica il layout delle bande del controllo.</span><span class="sxs-lookup"><span data-stu-id="8e835-106">Sent by a rebar control when the user changes the layout of the control's bands.</span></span> <span data-ttu-id="8e835-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8e835-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_LAYOUTCHANGED 

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8e835-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e835-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e835-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e835-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e835-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="8e835-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e835-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e835-111">Return value</span></span>

<span data-ttu-id="8e835-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8e835-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e835-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e835-113">Requirements</span></span>



| <span data-ttu-id="8e835-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e835-114">Requirement</span></span> | <span data-ttu-id="8e835-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8e835-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e835-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e835-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8e835-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e835-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e835-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e835-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8e835-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e835-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e835-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e835-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e835-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e835-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





