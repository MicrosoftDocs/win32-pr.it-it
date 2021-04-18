---
title: Codice di notifica RBN_MINMAX (COMmctrl. h)
description: Inviato da un controllo Rebar prima di massimizzare o ridurre al minimo un gruppo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- Controlli di Windows per il codice di notifica RBN_MINMAX
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301762"
---
# <a name="rbn_minmax-notification-code"></a><span data-ttu-id="ecfbd-105">\_Codice di notifica MinMax di RBN</span><span class="sxs-lookup"><span data-stu-id="ecfbd-105">RBN\_MINMAX notification code</span></span>

<span data-ttu-id="ecfbd-106">Inviato da un controllo Rebar prima di massimizzare o ridurre al minimo un gruppo.</span><span class="sxs-lookup"><span data-stu-id="ecfbd-106">Sent by a rebar control prior to maximizing or minimizing a band.</span></span> <span data-ttu-id="ecfbd-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ecfbd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_MINMAX
```



## <a name="parameters"></a><span data-ttu-id="ecfbd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecfbd-108">Parameters</span></span>

<span data-ttu-id="ecfbd-109">Questo codice di notifica non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="ecfbd-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ecfbd-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecfbd-110">Return value</span></span>

<span data-ttu-id="ecfbd-111">Restituisce un valore diverso da zero per impedire l'esecuzione dell'operazione, ovvero zero per consentire la continuazione.</span><span class="sxs-lookup"><span data-stu-id="ecfbd-111">Return a nonzero value to prevent the operation from taking place, zero to allow it to continue.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecfbd-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecfbd-112">Requirements</span></span>



| <span data-ttu-id="ecfbd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecfbd-113">Requirement</span></span> | <span data-ttu-id="ecfbd-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ecfbd-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfbd-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecfbd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ecfbd-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ecfbd-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ecfbd-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecfbd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ecfbd-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ecfbd-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ecfbd-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecfbd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecfbd-120"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecfbd-120"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





