---
title: Codice di notifica RBN_DELETEDBAND (COMmctrl. h)
description: Inviato da un controllo Rebar dopo l'eliminazione di una banda. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ef4aca07-de08-47de-b236-321e84e6e81c
keywords:
- Controlli di Windows per il codice di notifica RBN_DELETEDBAND
topic_type:
- apiref
api_name:
- RBN_DELETEDBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af4e107ccb1a42b82335255f48d0328e03019a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874145"
---
# <a name="rbn_deletedband-notification-code"></a><span data-ttu-id="46094-105">\_Codice di notifica DELETEDBAND di RBN</span><span class="sxs-lookup"><span data-stu-id="46094-105">RBN\_DELETEDBAND notification code</span></span>

<span data-ttu-id="46094-106">Inviato da un controllo Rebar dopo l'eliminazione di una banda.</span><span class="sxs-lookup"><span data-stu-id="46094-106">Sent by a rebar control after a band has been deleted.</span></span> <span data-ttu-id="46094-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="46094-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETEDBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="46094-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46094-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46094-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46094-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46094-110">Puntatore a una struttura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="46094-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46094-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46094-111">Return value</span></span>

<span data-ttu-id="46094-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="46094-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="46094-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46094-113">Requirements</span></span>



| <span data-ttu-id="46094-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="46094-114">Requirement</span></span> | <span data-ttu-id="46094-115">Valore</span><span class="sxs-lookup"><span data-stu-id="46094-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46094-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46094-116">Minimum supported client</span></span><br/> | <span data-ttu-id="46094-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46094-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46094-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46094-118">Minimum supported server</span></span><br/> | <span data-ttu-id="46094-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="46094-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46094-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46094-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="46094-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46094-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





