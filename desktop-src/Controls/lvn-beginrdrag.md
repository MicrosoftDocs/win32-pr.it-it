---
title: Codice di notifica LVN_BEGINRDRAG (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che viene avviata un'operazione di trascinamento della selezione che interessa il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 93feba3b-8e3e-4a04-bf2c-7ff67a85d4fb
keywords:
- Controlli di Windows per il codice di notifica LVN_BEGINRDRAG
topic_type:
- apiref
api_name:
- LVN_BEGINRDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b4f55c01ca2b5e43419ea926401ac3393d9a9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963801"
---
# <a name="lvn_beginrdrag-notification-code"></a><span data-ttu-id="452ae-105">\_Codice di notifica BEGINRDRAG di LVN</span><span class="sxs-lookup"><span data-stu-id="452ae-105">LVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="452ae-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che viene avviata un'operazione di trascinamento della selezione che interessa il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="452ae-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the right mouse button is being initiated.</span></span> <span data-ttu-id="452ae-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="452ae-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINRDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="452ae-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="452ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="452ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="452ae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="452ae-110">Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="452ae-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="452ae-111">Il membro **iItem** identifica l'elemento trascinato e gli altri membri sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="452ae-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="452ae-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="452ae-112">Return value</span></span>

<span data-ttu-id="452ae-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="452ae-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="452ae-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="452ae-114">Requirements</span></span>



| <span data-ttu-id="452ae-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="452ae-115">Requirement</span></span> | <span data-ttu-id="452ae-116">Valore</span><span class="sxs-lookup"><span data-stu-id="452ae-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="452ae-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="452ae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="452ae-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="452ae-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="452ae-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="452ae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="452ae-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="452ae-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="452ae-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="452ae-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="452ae-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="452ae-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





