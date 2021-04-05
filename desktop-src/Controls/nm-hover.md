---
title: Codice di notifica NM_HOVER (COMmctrl. h)
description: Inviato da un controllo quando il mouse viene spostato su un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0eef3e88-c1f0-4f9c-9ccf-580d8e464157
keywords:
- Controlli di Windows per il codice di notifica NM_HOVER
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69344b1aae78ebee99b86c78f4442df20f66187a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739927"
---
# <a name="nm_hover-notification-code"></a><span data-ttu-id="61f0a-105">\_Codice di notifica del passaggio del puntatore a Nm</span><span class="sxs-lookup"><span data-stu-id="61f0a-105">NM\_HOVER notification code</span></span>

<span data-ttu-id="61f0a-106">Inviato da un controllo quando il mouse viene spostato su un elemento.</span><span class="sxs-lookup"><span data-stu-id="61f0a-106">Sent by a control when the mouse hovers over an item.</span></span> <span data-ttu-id="61f0a-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="61f0a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="61f0a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="61f0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61f0a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61f0a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61f0a-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="61f0a-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61f0a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61f0a-111">Return value</span></span>

<span data-ttu-id="61f0a-112">Se non diversamente specificato, restituisce zero per consentire al controllo di elaborare normalmente il passaggio del mouse o un valore diverso da zero per impedire l'elaborazione del passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="61f0a-112">Unless otherwise specified, return zero to allow the control to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="61f0a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61f0a-113">Requirements</span></span>



| <span data-ttu-id="61f0a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="61f0a-114">Requirement</span></span> | <span data-ttu-id="61f0a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="61f0a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61f0a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61f0a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61f0a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61f0a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61f0a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61f0a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61f0a-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="61f0a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61f0a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61f0a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61f0a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61f0a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





