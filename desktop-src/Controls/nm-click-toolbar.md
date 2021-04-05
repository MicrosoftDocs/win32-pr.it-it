---
title: Codice di notifica NM_CLICK (barra degli strumenti) (COMmctrl. h)
description: Inviato da un controllo Toolbar quando l'utente fa clic su un elemento con il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- Codice di notifica di NM_CLICK (barra degli strumenti) controlli Windows
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
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874690"
---
# <a name="nm_click-toolbar-notification-code"></a><span data-ttu-id="a85dd-105">Codice di notifica di NM \_ (barra degli strumenti)</span><span class="sxs-lookup"><span data-stu-id="a85dd-105">NM\_CLICK (toolbar) notification code</span></span>

<span data-ttu-id="a85dd-106">Inviato da un controllo Toolbar quando l'utente fa clic su un elemento con il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="a85dd-106">Sent by a toolbar control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="a85dd-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a85dd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a85dd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a85dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a85dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a85dd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a85dd-110">Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="a85dd-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="a85dd-111">Il membro **dwItemSpec** contiene l'indice della sezione su cui è stato fatto clic.</span><span class="sxs-lookup"><span data-stu-id="a85dd-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a85dd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a85dd-112">Return value</span></span>

<span data-ttu-id="a85dd-113">Restituisce **true** per indicare che il clic del mouse è stato gestito ed Elimina l'elaborazione predefinita dal sistema.</span><span class="sxs-lookup"><span data-stu-id="a85dd-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="a85dd-114">Restituisce **false** per consentire l'elaborazione predefinita del clic.</span><span class="sxs-lookup"><span data-stu-id="a85dd-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="remarks"></a><span data-ttu-id="a85dd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a85dd-115">Remarks</span></span>

<span data-ttu-id="a85dd-116">Quando si fa clic su un elemento con il pulsante sinistro del mouse, la barra degli strumenti Invia un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) con il codice di notifica [ \_ selezionato BN](bn-clicked.md) alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="a85dd-116">Clicking an item with the left mouse button causes the toolbar to send a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with the [BN\_CLICKED](bn-clicked.md) notification code to the parent window.</span></span> <span data-ttu-id="a85dd-117">La \_ notifica di clic su Nm viene inviata dopo il messaggio del **\_ comando WM** .</span><span class="sxs-lookup"><span data-stu-id="a85dd-117">The NM\_CLICK notification is sent after the **WM\_COMMAND** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a85dd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a85dd-118">Requirements</span></span>



| <span data-ttu-id="a85dd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a85dd-119">Requirement</span></span> | <span data-ttu-id="a85dd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a85dd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a85dd-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a85dd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a85dd-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a85dd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a85dd-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a85dd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a85dd-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a85dd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a85dd-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a85dd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a85dd-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a85dd-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

