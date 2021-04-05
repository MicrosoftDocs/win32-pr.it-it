---
title: Codice di notifica NM_THEMECHANGED (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che il tema è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 5e6a039e-9c35-4476-8cf1-5aea8977ed2d
keywords:
- Controlli di Windows per il codice di notifica NM_THEMECHANGED
topic_type:
- apiref
api_name:
- NM_THEMECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dab2a133da2ff1fed0949f2bc97ce294168febc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048556"
---
# <a name="nm_themechanged-notification-code"></a><span data-ttu-id="e88af-105">\_Codice di notifica THEMECHANGED Nm</span><span class="sxs-lookup"><span data-stu-id="e88af-105">NM\_THEMECHANGED notification code</span></span>

<span data-ttu-id="e88af-106">Notifica alla finestra padre di un controllo che il tema è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="e88af-106">Notifies a control's parent window that the theme has changed.</span></span> <span data-ttu-id="e88af-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e88af-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_THEMECHANGED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e88af-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e88af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e88af-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e88af-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e88af-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="e88af-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e88af-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e88af-111">Return value</span></span>

<span data-ttu-id="e88af-112">Il valore restituito viene ignorato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="e88af-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e88af-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e88af-113">Requirements</span></span>



| <span data-ttu-id="e88af-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e88af-114">Requirement</span></span> | <span data-ttu-id="e88af-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e88af-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e88af-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e88af-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e88af-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e88af-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e88af-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e88af-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e88af-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e88af-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e88af-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e88af-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e88af-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e88af-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





