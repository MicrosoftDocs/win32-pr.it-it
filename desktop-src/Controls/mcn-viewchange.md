---
title: Codice di notifica MCN_VIEWCHANGE (COMmctrl. h)
description: Inviato da un controllo di calendario mensile quando cambia la visualizzazione corrente. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- Controlli di Windows per il codice di notifica MCN_VIEWCHANGE
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbcad3fdda355ac2795dbe49a89fa4e7c2c5cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475550"
---
# <a name="mcn_viewchange-notification-code"></a><span data-ttu-id="f8a52-105">\_Codice di notifica VIEWCHANGE di MCN</span><span class="sxs-lookup"><span data-stu-id="f8a52-105">MCN\_VIEWCHANGE notification code</span></span>

<span data-ttu-id="f8a52-106">Inviato da un controllo di calendario mensile quando cambia la visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f8a52-106">Sent by a month calendar control when the current view changes.</span></span> <span data-ttu-id="f8a52-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f8a52-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f8a52-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8a52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8a52-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8a52-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8a52-110">Puntatore a una struttura [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) contenente informazioni sulla visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f8a52-110">Pointer to an [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) structure that contains information about the current view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8a52-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8a52-111">Return value</span></span>

<span data-ttu-id="f8a52-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f8a52-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a52-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8a52-113">Requirements</span></span>



| <span data-ttu-id="f8a52-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8a52-114">Requirement</span></span> | <span data-ttu-id="f8a52-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f8a52-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a52-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8a52-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a52-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8a52-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8a52-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8a52-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a52-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8a52-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8a52-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8a52-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8a52-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8a52-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





