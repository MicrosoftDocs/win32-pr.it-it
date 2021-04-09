---
title: Codice di notifica HDN_BEGINTRACK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente ha iniziato il trascinamento di un divisore nel controllo, ovvero l'utente ha premuto il pulsante sinistro del mouse mentre il cursore si trova su un divisore nel controllo intestazione.
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- Controlli di Windows per il codice di notifica HDN_BEGINTRACK
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121774"
---
# <a name="hdn_begintrack-notification-code"></a><span data-ttu-id="bbae0-104">\_Codice di notifica BEGINTRACK di HDN</span><span class="sxs-lookup"><span data-stu-id="bbae0-104">HDN\_BEGINTRACK notification code</span></span>

<span data-ttu-id="bbae0-105">Notifica alla finestra padre di un controllo di intestazione che l'utente ha iniziato il trascinamento di un divisore nel controllo, ovvero l'utente ha premuto il pulsante sinistro del mouse mentre il cursore si trova su un divisore nel controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="bbae0-105">Notifies a header control's parent window that the user has begun dragging a divider in the control (that is, the user has pressed the left mouse button while the mouse cursor is on a divider in the header control).</span></span> <span data-ttu-id="bbae0-106">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bbae0-106">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bbae0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbae0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbae0-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbae0-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbae0-109">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni sul controllo intestazione e l'elemento di cui deve essere trascinato il separatore.</span><span class="sxs-lookup"><span data-stu-id="bbae0-109">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is to be dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbae0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbae0-110">Return value</span></span>

<span data-ttu-id="bbae0-111">Restituisce **false** per consentire il rilevamento del divisore o **true** per impedire il rilevamento.</span><span class="sxs-lookup"><span data-stu-id="bbae0-111">Returns **FALSE** to allow tracking of the divider, or **TRUE** to prevent tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbae0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbae0-112">Requirements</span></span>



| <span data-ttu-id="bbae0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbae0-113">Requirement</span></span> | <span data-ttu-id="bbae0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="bbae0-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbae0-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbae0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bbae0-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bbae0-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbae0-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbae0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bbae0-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bbae0-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbae0-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbae0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbae0-120"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbae0-120"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bbae0-121">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bbae0-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bbae0-122">**HDN \_ BEGINTRACKW** (Unicode) e **HDN \_ BEGINTRACKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bbae0-122">**HDN\_BEGINTRACKW** (Unicode) and **HDN\_BEGINTRACKA** (ANSI)</span></span><br/>             |



 

 





