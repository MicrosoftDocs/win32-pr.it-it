---
title: Codice di notifica HDN_ITEMCLICK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto clic sul controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- Controlli di Windows per il codice di notifica HDN_ITEMCLICK
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874350"
---
# <a name="hdn_itemclick-notification-code"></a><span data-ttu-id="7c380-105">\_Codice di notifica ITEMCLICK di HDN</span><span class="sxs-lookup"><span data-stu-id="7c380-105">HDN\_ITEMCLICK notification code</span></span>

<span data-ttu-id="7c380-106">Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto clic sul controllo.</span><span class="sxs-lookup"><span data-stu-id="7c380-106">Notifies a header control's parent window that the user clicked the control.</span></span> <span data-ttu-id="7c380-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7c380-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7c380-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c380-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c380-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c380-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c380-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che identifica il controllo intestazione e specifica l'indice dell'elemento dell'intestazione su cui è stato fatto clic e il pulsante del mouse utilizzato per fare clic sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="7c380-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that identifies the header control and specifies the index of the header item that was clicked and the mouse button used to click the item.</span></span> <span data-ttu-id="7c380-111">Il membro **pItem** è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="7c380-111">The **pItem** member is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c380-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c380-112">Return value</span></span>

<span data-ttu-id="7c380-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7c380-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c380-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c380-114">Remarks</span></span>

<span data-ttu-id="7c380-115">Un controllo intestazione Invia questo codice di notifica dopo che l'utente rilascia il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="7c380-115">A header control sends this notification code after the user releases the left mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c380-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c380-116">Requirements</span></span>



| <span data-ttu-id="7c380-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c380-117">Requirement</span></span> | <span data-ttu-id="7c380-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7c380-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c380-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c380-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7c380-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c380-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c380-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c380-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7c380-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c380-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c380-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c380-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c380-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c380-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7c380-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7c380-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7c380-126">**HDN \_ ITEMCLICKW** (Unicode) e **HDN \_ ITEMCLICKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7c380-126">**HDN\_ITEMCLICKW** (Unicode) and **HDN\_ITEMCLICKA** (ANSI)</span></span><br/>               |



 

 





