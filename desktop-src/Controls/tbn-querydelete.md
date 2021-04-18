---
title: Codice di notifica TBN_QUERYDELETE (COMmctrl. h)
description: Notifica alla finestra padre della barra degli strumenti se un pulsante può essere eliminato da una barra degli strumenti mentre l'utente personalizza la barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- Controlli di Windows per il codice di notifica TBN_QUERYDELETE
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517361"
---
# <a name="tbn_querydelete-notification-code"></a><span data-ttu-id="83837-105">\_Codice di notifica QUERYDELETE di TBN</span><span class="sxs-lookup"><span data-stu-id="83837-105">TBN\_QUERYDELETE notification code</span></span>

<span data-ttu-id="83837-106">Notifica alla finestra padre della barra degli strumenti se un pulsante può essere eliminato da una barra degli strumenti mentre l'utente personalizza la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="83837-106">Notifies the toolbar's parent window whether a button may be deleted from a toolbar while the user is customizing the toolbar.</span></span> <span data-ttu-id="83837-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="83837-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="83837-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="83837-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83837-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83837-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83837-110">Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="83837-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="83837-111">Il membro **iItem** contiene l'indice in base zero del pulsante da eliminare.</span><span class="sxs-lookup"><span data-stu-id="83837-111">The **iItem** member contains the zero-based index of the button to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83837-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83837-112">Return value</span></span>

<span data-ttu-id="83837-113">Restituisce **true** per consentire l'eliminazione del pulsante o **false** per impedire che il pulsante venga eliminato.</span><span class="sxs-lookup"><span data-stu-id="83837-113">Returns **TRUE** to allow the button to be deleted, or **FALSE** to prevent the button from being deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="83837-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83837-114">Requirements</span></span>



| <span data-ttu-id="83837-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="83837-115">Requirement</span></span> | <span data-ttu-id="83837-116">Valore</span><span class="sxs-lookup"><span data-stu-id="83837-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83837-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83837-117">Minimum supported client</span></span><br/> | <span data-ttu-id="83837-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83837-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83837-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83837-119">Minimum supported server</span></span><br/> | <span data-ttu-id="83837-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83837-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83837-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83837-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="83837-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83837-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





