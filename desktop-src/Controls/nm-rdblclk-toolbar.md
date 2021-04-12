---
title: Codice di notifica NM_RDBLCLK (barra degli strumenti) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0281a687-3f1c-4fc1-bf1d-19c7ac920cd3
keywords:
- Codice di notifica di NM_RDBLCLK (barra degli strumenti) controlli Windows
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec2129b6400c60bd59e441ff8af2083e781ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478256"
---
# <a name="nm_rdblclk-toolbar-notification-code"></a><span data-ttu-id="241fb-105">\_Codice di notifica RDBLCLK di Nm (barra degli strumenti)</span><span class="sxs-lookup"><span data-stu-id="241fb-105">NM\_RDBLCLK (toolbar) notification code</span></span>

<span data-ttu-id="241fb-106">Notifica alla finestra padre di un controllo che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="241fb-106">Notifies a control's parent window that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="241fb-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="241fb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="241fb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="241fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="241fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="241fb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="241fb-110">Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="241fb-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="241fb-111">Se è stato fatto clic con il mouse su un elemento della barra degli strumenti, il membro **dwItemSpec** contiene l'identificatore dell'elemento e il membro **dwItemData** contiene i dati dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="241fb-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="241fb-112">Se è stato fatto clic con il mouse su un separatore o su uno spazio vuoto sulla barra degli strumenti, il membro **dwItemSpec** conterrà-1.</span><span class="sxs-lookup"><span data-stu-id="241fb-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="241fb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="241fb-113">Return value</span></span>

<span data-ttu-id="241fb-114">Restituisce **false** per consentire al controllo Toolbar di eseguire l'elaborazione predefinita dell'evento o **true** per impedire l'elaborazione dell'evento da parte del controllo.</span><span class="sxs-lookup"><span data-stu-id="241fb-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="241fb-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="241fb-115">Requirements</span></span>



| <span data-ttu-id="241fb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="241fb-116">Requirement</span></span> | <span data-ttu-id="241fb-117">Valore</span><span class="sxs-lookup"><span data-stu-id="241fb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="241fb-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="241fb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="241fb-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="241fb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="241fb-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="241fb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="241fb-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="241fb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="241fb-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="241fb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="241fb-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="241fb-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





