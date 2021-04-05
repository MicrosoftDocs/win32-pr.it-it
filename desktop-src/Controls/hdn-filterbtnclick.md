---
title: Codice di notifica HDN_FILTERBTNCLICK (COMmctrl. h)
description: Notifica alla finestra padre del controllo intestazione quando viene fatto clic sul pulsante del filtro o in risposta a un \_ messaggio HDM. Questo codice di notifica è stato inviato sotto forma di \_ messaggio di notifica WM.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- Controlli di Windows per il codice di notifica HDN_FILTERBTNCLICK
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873378"
---
# <a name="hdn_filterbtnclick-notification-code"></a><span data-ttu-id="c8751-105">\_Codice di notifica FILTERBTNCLICK di HDN</span><span class="sxs-lookup"><span data-stu-id="c8751-105">HDN\_FILTERBTNCLICK notification code</span></span>

<span data-ttu-id="c8751-106">Notifica alla finestra padre del controllo intestazione quando viene fatto clic sul pulsante del filtro o in risposta a un [**messaggio \_ HDM**](hdm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c8751-106">Notifies the header control's parent window when the filter button is clicked or in response to an [**HDM\_SETITEM**](hdm-setitem.md) message.</span></span> <span data-ttu-id="c8751-107">Questo codice di notifica è stato inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c8751-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c8751-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8751-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8751-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8751-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8751-110">Puntatore a una struttura [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) contenente informazioni sul controllo intestazione e sul pulsante filtro intestazione.</span><span class="sxs-lookup"><span data-stu-id="c8751-110">A pointer to an [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) structure that contains information about the header control and the header filter button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8751-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8751-111">Return value</span></span>

<span data-ttu-id="c8751-112">Se si restituisce **true**, verrà inviato un codice di notifica [ \_ FILTERCHANGE HDN](hdn-filterchange.md) alla finestra padre del controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="c8751-112">If you return **TRUE**, an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification code will be sent to the header control's parent window.</span></span> <span data-ttu-id="c8751-113">Questo codice di notifica fornisce alla finestra padre la possibilità di sincronizzare gli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c8751-113">This notification code gives the parent window an opportunity to synchronize its user interface elements.</span></span> <span data-ttu-id="c8751-114">Restituisce **false** se non si desidera che venga inviata la notifica.</span><span class="sxs-lookup"><span data-stu-id="c8751-114">Return **FALSE** if you do not want the notification sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8751-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8751-115">Requirements</span></span>



| <span data-ttu-id="c8751-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8751-116">Requirement</span></span> | <span data-ttu-id="c8751-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c8751-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8751-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8751-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c8751-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8751-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8751-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8751-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c8751-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c8751-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8751-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8751-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8751-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8751-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8751-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8751-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8751-125">**NMHDFILTERBTNCLICK**</span><span class="sxs-lookup"><span data-stu-id="c8751-125">**NMHDFILTERBTNCLICK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





