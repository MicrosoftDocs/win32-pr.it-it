---
title: Codice di notifica di NM_RCLICK (barra di stato) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- Codice di notifica di NM_RCLICK (barra di stato) controlli Windows
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326ac6600716419648ecfacf25cd8423551fd03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341372"
---
# <a name="nm_rclick-status-bar-notification-code"></a><span data-ttu-id="69c6e-105">\_Codice di notifica di RCLICK Nm (barra di stato)</span><span class="sxs-lookup"><span data-stu-id="69c6e-105">NM\_RCLICK (status bar) notification code</span></span>

<span data-ttu-id="69c6e-106">Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="69c6e-106">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="69c6e-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="69c6e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="69c6e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="69c6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69c6e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69c6e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69c6e-110">Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="69c6e-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69c6e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69c6e-111">Return value</span></span>

<span data-ttu-id="69c6e-112">Restituisce **true** per indicare che il clic del mouse è stato gestito ed Elimina l'elaborazione predefinita dal sistema.</span><span class="sxs-lookup"><span data-stu-id="69c6e-112">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="69c6e-113">Restituisce **false** per consentire l'elaborazione predefinita del clic.</span><span class="sxs-lookup"><span data-stu-id="69c6e-113">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="69c6e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69c6e-114">Requirements</span></span>



| <span data-ttu-id="69c6e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="69c6e-115">Requirement</span></span> | <span data-ttu-id="69c6e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="69c6e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69c6e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69c6e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="69c6e-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69c6e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69c6e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69c6e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="69c6e-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="69c6e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69c6e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69c6e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="69c6e-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69c6e-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





