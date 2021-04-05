---
title: Codice di notifica RBN_ENDDRAG (COMmctrl. h)
description: Inviato da un controllo Rebar quando l'utente smette di trascinare un gruppo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 24b06144-6a4c-46a4-bef1-d6592f72a2c0
keywords:
- Controlli di Windows per il codice di notifica RBN_ENDDRAG
topic_type:
- apiref
api_name:
- RBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb6c538679d793ed2407775b4238cea475ba4ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048547"
---
# <a name="rbn_enddrag-notification-code"></a><span data-ttu-id="d3ff0-105">\_Codice di notifica ENDDRAG di RBN</span><span class="sxs-lookup"><span data-stu-id="d3ff0-105">RBN\_ENDDRAG notification code</span></span>

<span data-ttu-id="d3ff0-106">Inviato da un controllo Rebar quando l'utente smette di trascinare un gruppo.</span><span class="sxs-lookup"><span data-stu-id="d3ff0-106">Sent by a rebar control when the user stops dragging a band.</span></span> <span data-ttu-id="d3ff0-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d3ff0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_ENDDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d3ff0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3ff0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3ff0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3ff0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3ff0-110">Puntatore a una struttura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="d3ff0-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3ff0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3ff0-111">Return value</span></span>

<span data-ttu-id="d3ff0-112">Il valore restituito per questo codice di notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d3ff0-112">The return value for this notification code is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ff0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3ff0-113">Requirements</span></span>



| <span data-ttu-id="d3ff0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3ff0-114">Requirement</span></span> | <span data-ttu-id="d3ff0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d3ff0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ff0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3ff0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ff0-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3ff0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3ff0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3ff0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ff0-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3ff0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3ff0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3ff0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3ff0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3ff0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





