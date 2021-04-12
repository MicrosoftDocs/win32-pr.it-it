---
title: Codice di notifica HDN_ITEMDBLCLICK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto doppio clic sul controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM. Solo i controlli header impostati sullo \_ stile dei pulsanti HDS inviano il codice di notifica.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- Controlli di Windows per il codice di notifica HDN_ITEMDBLCLICK
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e61117303ecc478a998da8799867988dbc1ca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225235"
---
# <a name="hdn_itemdblclick-notification-code"></a><span data-ttu-id="b4eb8-106">\_Codice di notifica ITEMDBLCLICK di HDN</span><span class="sxs-lookup"><span data-stu-id="b4eb8-106">HDN\_ITEMDBLCLICK notification code</span></span>

<span data-ttu-id="b4eb8-107">Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto doppio clic sul controllo.</span><span class="sxs-lookup"><span data-stu-id="b4eb8-107">Notifies a header control's parent window that the user double-clicked the control.</span></span> <span data-ttu-id="b4eb8-108">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b4eb8-108">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="b4eb8-109">Solo i controlli header impostati sullo stile dei [**\_ pulsanti HDS**](header-control-styles.md) inviano il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="b4eb8-109">Only header controls that are set to the [**HDS\_BUTTONS**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b4eb8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4eb8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4eb8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4eb8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4eb8-112">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="b4eb8-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4eb8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4eb8-113">Return value</span></span>

<span data-ttu-id="b4eb8-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b4eb8-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4eb8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4eb8-115">Requirements</span></span>



| <span data-ttu-id="b4eb8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4eb8-116">Requirement</span></span> | <span data-ttu-id="b4eb8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b4eb8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4eb8-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4eb8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b4eb8-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4eb8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4eb8-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4eb8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b4eb8-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4eb8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4eb8-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4eb8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4eb8-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4eb8-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b4eb8-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b4eb8-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b4eb8-125">**HDN \_ ITEMDBLCLICKW** (Unicode) e **HDN \_ ITEMDBLCLICKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b4eb8-125">**HDN\_ITEMDBLCLICKW** (Unicode) and **HDN\_ITEMDBLCLICKA** (ANSI)</span></span><br/>         |



 

 





