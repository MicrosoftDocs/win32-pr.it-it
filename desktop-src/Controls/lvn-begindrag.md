---
title: Codice di notifica LVN_BEGINDRAG (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che viene avviata un'operazione di trascinamento della selezione che interessa il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2b9bbff8-f5f7-47ac-b662-a327ff49caf7
keywords:
- Controlli di Windows per il codice di notifica LVN_BEGINDRAG
topic_type:
- apiref
api_name:
- LVN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69166cd38242db915f70772b5dfbd3bab6ba56df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047928"
---
# <a name="lvn_begindrag-notification-code"></a><span data-ttu-id="6a254-105">\_Codice di notifica BEGINDRAG di LVN</span><span class="sxs-lookup"><span data-stu-id="6a254-105">LVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="6a254-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che viene avviata un'operazione di trascinamento della selezione che interessa il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="6a254-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="6a254-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6a254-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6a254-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a254-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a254-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a254-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a254-110">Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="6a254-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="6a254-111">Il membro **iItem** identifica l'elemento trascinato e gli altri membri sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="6a254-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a254-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a254-112">Return value</span></span>

<span data-ttu-id="6a254-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="6a254-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a254-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a254-114">Requirements</span></span>



| <span data-ttu-id="6a254-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a254-115">Requirement</span></span> | <span data-ttu-id="6a254-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6a254-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a254-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a254-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6a254-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a254-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a254-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a254-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6a254-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6a254-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a254-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a254-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a254-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a254-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





