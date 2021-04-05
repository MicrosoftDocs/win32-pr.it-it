---
title: Codice di notifica NM_LDOWN (barra degli strumenti) (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che è stato premuto il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- Codice di notifica di NM_LDOWN (barra degli strumenti) controlli Windows
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
ms.openlocfilehash: e60f1f05d85aa8885acf31a36098056d68612ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873294"
---
# <a name="nm_ldown-toolbar-notification-code"></a><span data-ttu-id="f56dd-105">\_Codice di notifica LDOWN di Nm (barra degli strumenti)</span><span class="sxs-lookup"><span data-stu-id="f56dd-105">NM\_LDOWN (toolbar) notification code</span></span>

<span data-ttu-id="f56dd-106">Notifica alla finestra padre di una barra degli strumenti che è stato premuto il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="f56dd-106">Notifies a toolbar's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="f56dd-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f56dd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f56dd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f56dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f56dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f56dd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f56dd-110">Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="f56dd-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="f56dd-111">Se è stato fatto clic con il mouse su un elemento della barra degli strumenti, il membro **dwItemSpec** contiene l'identificatore dell'elemento e il membro **dwItemData** contiene i dati dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f56dd-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="f56dd-112">Se è stato fatto clic con il mouse su un separatore o su uno spazio vuoto sulla barra degli strumenti, il membro **dwItemSpec** conterrà-1.</span><span class="sxs-lookup"><span data-stu-id="f56dd-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f56dd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f56dd-113">Return value</span></span>

<span data-ttu-id="f56dd-114">Restituisce **false** per consentire al controllo Toolbar di eseguire l'elaborazione predefinita dell'evento o **true** per impedire l'elaborazione dell'evento da parte del controllo.</span><span class="sxs-lookup"><span data-stu-id="f56dd-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="remarks"></a><span data-ttu-id="f56dd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f56dd-115">Remarks</span></span>

<span data-ttu-id="f56dd-116">Questa notifica viene inviata dopo l'invio del codice di notifica a [ \_ discesa TBN](tbn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="f56dd-116">This notification is sent after the [TBN\_DROPDOWN](tbn-dropdown.md) notification code has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="f56dd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f56dd-117">Requirements</span></span>



| <span data-ttu-id="f56dd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f56dd-118">Requirement</span></span> | <span data-ttu-id="f56dd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f56dd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f56dd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f56dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f56dd-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f56dd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f56dd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f56dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f56dd-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f56dd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f56dd-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f56dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f56dd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f56dd-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





