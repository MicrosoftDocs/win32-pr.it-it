---
title: Messaggio LVN_ODFINDITEM (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco virtuale quando è necessario che il proprietario trovi un particolare elemento di callback.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- Controlli di Windows Message LVN_ODFINDITEM
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120526"
---
# <a name="lvn_odfinditem-message"></a><span data-ttu-id="e4305-104">\_Messaggio LVN ODFINDITEM</span><span class="sxs-lookup"><span data-stu-id="e4305-104">LVN\_ODFINDITEM message</span></span>

<span data-ttu-id="e4305-105">Inviato da un controllo di [visualizzazione elenco virtuale](list-view-controls-overview.md) quando è necessario che il proprietario trovi un particolare elemento di callback.</span><span class="sxs-lookup"><span data-stu-id="e4305-105">Sent by a [virtual list-view](list-view-controls-overview.md) control when it needs the owner to find a particular callback item.</span></span> <span data-ttu-id="e4305-106">Ad esempio, il controllo invierà questo codice di notifica quando riceverà un input da tastiera di scelta rapida o quando riceve un messaggio [**\_ FINDITEM LVM**](lvm-finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="e4305-106">For example, the control will send this notification code when it receives shortcut keyboard input or when it receives an [**LVM\_FINDITEM**](lvm-finditem.md) message.</span></span> <span data-ttu-id="e4305-107">Il \_ codice di notifica ODFINDITEM di LVN viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e4305-107">The LVN\_ODFINDITEM notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e4305-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4305-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4305-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4305-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4305-110">Puntatore a una struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) che include le informazioni da utilizzare per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="e4305-110">Pointer to an [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that includes information to be used for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4305-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4305-111">Return value</span></span>

<span data-ttu-id="e4305-112">Restituisce l'indice dell'elemento trovato oppure-1 se non viene trovato alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="e4305-112">Return the index of the item found, or -1 if no item is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4305-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4305-113">Remarks</span></span>

<span data-ttu-id="e4305-114">Le informazioni di ricerca vengono inviate sotto forma di una struttura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , che è un membro della struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .</span><span class="sxs-lookup"><span data-stu-id="e4305-114">Search information is sent in the form of an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure, which is a member of the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4305-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4305-115">Requirements</span></span>



| <span data-ttu-id="e4305-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4305-116">Requirement</span></span> | <span data-ttu-id="e4305-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e4305-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4305-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4305-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e4305-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4305-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4305-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4305-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e4305-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4305-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4305-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4305-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4305-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4305-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e4305-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e4305-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e4305-125">**LVN \_ ODFINDITEMW** (Unicode) e **LVN \_ ODFINDITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e4305-125">**LVN\_ODFINDITEMW** (Unicode) and **LVN\_ODFINDITEMA** (ANSI)</span></span><br/>             |



 

 





