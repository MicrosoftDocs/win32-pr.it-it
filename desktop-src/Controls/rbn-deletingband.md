---
title: Codice di notifica RBN_DELETINGBAND (COMmctrl. h)
description: Inviato da un controllo Rebar quando un gruppo sta per essere eliminato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 92840cb1-375e-4c37-bde4-7ba02a1ff4f1
keywords:
- Controlli di Windows per il codice di notifica RBN_DELETINGBAND
topic_type:
- apiref
api_name:
- RBN_DELETINGBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf810fd8800d7774a0dbf9a65cdf08c2d53d92ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964547"
---
# <a name="rbn_deletingband-notification-code"></a><span data-ttu-id="47062-105">\_Codice di notifica DELETINGBAND di RBN</span><span class="sxs-lookup"><span data-stu-id="47062-105">RBN\_DELETINGBAND notification code</span></span>

<span data-ttu-id="47062-106">Inviato da un controllo Rebar quando un gruppo sta per essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="47062-106">Sent by a rebar control when a band is about to be deleted.</span></span> <span data-ttu-id="47062-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="47062-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETINGBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="47062-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="47062-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47062-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47062-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47062-110">Puntatore a una struttura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="47062-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47062-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47062-111">Return value</span></span>

<span data-ttu-id="47062-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="47062-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="47062-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47062-113">Requirements</span></span>



| <span data-ttu-id="47062-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="47062-114">Requirement</span></span> | <span data-ttu-id="47062-115">Valore</span><span class="sxs-lookup"><span data-stu-id="47062-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47062-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47062-116">Minimum supported client</span></span><br/> | <span data-ttu-id="47062-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47062-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47062-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47062-118">Minimum supported server</span></span><br/> | <span data-ttu-id="47062-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="47062-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47062-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47062-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="47062-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="47062-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





