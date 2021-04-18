---
title: Codice di notifica NM_LDOWN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che è stato premuto il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 59546fc3-f7c5-4b2d-9fd7-2ff89d72cd9f
keywords:
- Controlli di Windows per il codice di notifica NM_LDOWN
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d62d1570fc0c10ccb64ae6c1f9af6433025ec79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301018"
---
# <a name="nm_ldown-notification-code"></a><span data-ttu-id="0a4f6-105">\_Codice di notifica LDOWN Nm</span><span class="sxs-lookup"><span data-stu-id="0a4f6-105">NM\_LDOWN notification code</span></span>

<span data-ttu-id="0a4f6-106">Notifica alla finestra padre di un controllo che è stato premuto il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-106">Notifies a control's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="0a4f6-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4f6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

   lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0a4f6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a4f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a4f6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a4f6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a4f6-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a4f6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a4f6-111">Return value</span></span>

<span data-ttu-id="0a4f6-112">Il valore restituito viene ignorato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4f6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a4f6-113">Requirements</span></span>



| <span data-ttu-id="0a4f6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a4f6-114">Requirement</span></span> | <span data-ttu-id="0a4f6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0a4f6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4f6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a4f6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0a4f6-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a4f6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a4f6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a4f6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0a4f6-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a4f6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a4f6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a4f6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a4f6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a4f6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





