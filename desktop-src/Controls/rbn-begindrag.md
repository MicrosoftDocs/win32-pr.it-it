---
title: Codice di notifica RBN_BEGINDRAG (COMmctrl. h)
description: Inviato da un controllo Rebar quando l'utente inizia a trascinare un gruppo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e1565b31-7694-43cc-87ee-c9294a0612cd
keywords:
- Controlli di Windows per il codice di notifica RBN_BEGINDRAG
topic_type:
- apiref
api_name:
- RBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c797e026484b32e68408cf720a1d4681d066c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475340"
---
# <a name="rbn_begindrag-notification-code"></a><span data-ttu-id="49fdc-105">\_Codice di notifica BEGINDRAG di RBN</span><span class="sxs-lookup"><span data-stu-id="49fdc-105">RBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="49fdc-106">Inviato da un controllo Rebar quando l'utente inizia a trascinare un gruppo.</span><span class="sxs-lookup"><span data-stu-id="49fdc-106">Sent by a rebar control when the user begins dragging a band.</span></span> <span data-ttu-id="49fdc-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="49fdc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_BEGINDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="49fdc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="49fdc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49fdc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49fdc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49fdc-110">Puntatore a una struttura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="49fdc-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49fdc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49fdc-111">Return value</span></span>

<span data-ttu-id="49fdc-112">Restituisce zero per consentire al controllo Rebar di continuare l'operazione di trascinamento o un valore diverso da zero per interrompere l'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="49fdc-112">Return zero to allow the rebar to continue the drag operation, or nonzero to abort the drag operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="49fdc-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49fdc-113">Requirements</span></span>



| <span data-ttu-id="49fdc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="49fdc-114">Requirement</span></span> | <span data-ttu-id="49fdc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="49fdc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49fdc-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49fdc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="49fdc-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49fdc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49fdc-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49fdc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="49fdc-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49fdc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49fdc-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49fdc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="49fdc-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49fdc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





