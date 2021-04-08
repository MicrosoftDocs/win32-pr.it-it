---
title: Codice di notifica RBN_CHILDSIZE (COMmctrl. h)
description: Inviato da un controllo Rebar quando la finestra figlio di una banda viene ridimensionata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ba64d21a-e568-4894-8007-be644ae4f54a
keywords:
- Controlli di Windows per il codice di notifica RBN_CHILDSIZE
topic_type:
- apiref
api_name:
- RBN_CHILDSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d505d13048d96783d53b9b1a821d80712597da4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874017"
---
# <a name="rbn_childsize-notification-code"></a><span data-ttu-id="2eebd-105">\_Codice di notifica CHILDSIZE di RBN</span><span class="sxs-lookup"><span data-stu-id="2eebd-105">RBN\_CHILDSIZE notification code</span></span>

<span data-ttu-id="2eebd-106">Inviato da un controllo Rebar quando la finestra figlio di una banda viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="2eebd-106">Sent by a rebar control when a band's child window is resized.</span></span> <span data-ttu-id="2eebd-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2eebd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHILDSIZE

    lprbcs = (LPNMREBARCHILDSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2eebd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2eebd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eebd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2eebd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2eebd-110">Puntatore a una struttura [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="2eebd-110">Pointer to an [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eebd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2eebd-111">Return value</span></span>

<span data-ttu-id="2eebd-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2eebd-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eebd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2eebd-113">Requirements</span></span>



| <span data-ttu-id="2eebd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eebd-114">Requirement</span></span> | <span data-ttu-id="2eebd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2eebd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2eebd-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2eebd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2eebd-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2eebd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2eebd-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2eebd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2eebd-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2eebd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2eebd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2eebd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eebd-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eebd-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





