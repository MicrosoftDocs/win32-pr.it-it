---
title: Codice di notifica TRBN_THUMBPOSCHANGING (COMmctrl. h)
description: Notifica che la posizione del cursore in un controllo TrackBar sta cambiando. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- Controlli di Windows per il codice di notifica TRBN_THUMBPOSCHANGING
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969157"
---
# <a name="trbn_thumbposchanging-notification-code"></a><span data-ttu-id="71ea2-105">\_Codice di notifica THUMBPOSCHANGING di Trbn</span><span class="sxs-lookup"><span data-stu-id="71ea2-105">TRBN\_THUMBPOSCHANGING notification code</span></span>

<span data-ttu-id="71ea2-106">Notifica che la posizione del cursore in un controllo TrackBar sta cambiando.</span><span class="sxs-lookup"><span data-stu-id="71ea2-106">Notifies that the thumb position on a trackbar is changing.</span></span> <span data-ttu-id="71ea2-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="71ea2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="71ea2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="71ea2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ea2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71ea2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71ea2-110">Puntatore a una struttura [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) .</span><span class="sxs-lookup"><span data-stu-id="71ea2-110">Pointer to a [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) structure.</span></span> <span data-ttu-id="71ea2-111">Il chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei relativi membri, inclusi i membri della struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenuta.</span><span class="sxs-lookup"><span data-stu-id="71ea2-111">The caller is responsible for allocating this structure and setting its members, including the members of the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ea2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71ea2-112">Return value</span></span>

<span data-ttu-id="71ea2-113">Restituisce **true** per impedire che il controllo Thumb venga spostato nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="71ea2-113">Return **TRUE** to prevent the thumb from moving to the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="71ea2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="71ea2-114">Remarks</span></span>

<span data-ttu-id="71ea2-115">Inviare questa notifica ai client che non sono in ascolto dei messaggi [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="71ea2-115">Send this notification to clients that do not listen for [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ea2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71ea2-116">Requirements</span></span>



| <span data-ttu-id="71ea2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="71ea2-117">Requirement</span></span> | <span data-ttu-id="71ea2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="71ea2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71ea2-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71ea2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="71ea2-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71ea2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="71ea2-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71ea2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="71ea2-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71ea2-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="71ea2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71ea2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="71ea2-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="71ea2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





