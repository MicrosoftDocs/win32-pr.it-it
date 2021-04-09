---
title: Codice di notifica del NM_CLICK (scheda) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo struttura a schede che l'utente ha fatto clic con il pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b892aded-d6b8-4a04-bfdd-0153b65eaccc
keywords:
- Codice di notifica di NM_CLICK (tabulazione) controlli di Windows
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e451a7a87d1b02140f59797c7485b8eb250dad13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121743"
---
# <a name="nm_click-tab-notification-code"></a><span data-ttu-id="b3050-105">Codice di notifica di NM \_ (scheda)</span><span class="sxs-lookup"><span data-stu-id="b3050-105">NM\_CLICK (tab) notification code</span></span>

<span data-ttu-id="b3050-106">Notifica alla finestra padre di un controllo struttura a schede che l'utente ha fatto clic con il pulsante sinistro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="b3050-106">Notifies the parent window of a tab control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="b3050-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b3050-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b3050-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3050-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3050-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3050-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3050-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="b3050-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3050-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3050-111">Return value</span></span>

<span data-ttu-id="b3050-112">Il valore restituito viene ignorato dal controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="b3050-112">The return value is ignored by the tab control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3050-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3050-113">Requirements</span></span>



| <span data-ttu-id="b3050-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3050-114">Requirement</span></span> | <span data-ttu-id="b3050-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b3050-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3050-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3050-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b3050-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3050-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3050-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3050-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b3050-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b3050-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3050-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3050-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3050-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3050-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





