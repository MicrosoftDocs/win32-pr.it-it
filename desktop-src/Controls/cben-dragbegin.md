---
title: Codice di notifica CBEN_DRAGBEGIN (COMmctrl. h)
description: Inviato quando l'utente inizia a trascinare l'immagine dell'elemento visualizzato nella parte di modifica del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- Controlli di Windows per il codice di notifica CBEN_DRAGBEGIN
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121155"
---
# <a name="cben_dragbegin-notification-code"></a><span data-ttu-id="53e67-105">\_Codice di notifica DRAGBEGIN di CBEN</span><span class="sxs-lookup"><span data-stu-id="53e67-105">CBEN\_DRAGBEGIN notification code</span></span>

<span data-ttu-id="53e67-106">Inviato quando l'utente inizia a trascinare l'immagine dell'elemento visualizzato nella parte di modifica del controllo.</span><span class="sxs-lookup"><span data-stu-id="53e67-106">Sent when the user begins dragging the image of the item displayed in the edit portion of the control.</span></span> <span data-ttu-id="53e67-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="53e67-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="53e67-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="53e67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53e67-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53e67-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53e67-110">Puntatore a una struttura [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) che contiene informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="53e67-110">A pointer to a [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53e67-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53e67-111">Return value</span></span>

<span data-ttu-id="53e67-112">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="53e67-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="53e67-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="53e67-113">Remarks</span></span>

<span data-ttu-id="53e67-114">Se l'applicazione ricevente implementa la funzionalità di trascinamento della selezione dal controllo, l'applicazione inizierà l'operazione di trascinamento della selezione in risposta a questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="53e67-114">If the receiving application implements drag-and-drop functionality from the control, the application will begin the drag-and-drop operation in response to this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53e67-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53e67-115">Requirements</span></span>



| <span data-ttu-id="53e67-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="53e67-116">Requirement</span></span> | <span data-ttu-id="53e67-117">Valore</span><span class="sxs-lookup"><span data-stu-id="53e67-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53e67-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53e67-118">Minimum supported client</span></span><br/> | <span data-ttu-id="53e67-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53e67-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53e67-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53e67-120">Minimum supported server</span></span><br/> | <span data-ttu-id="53e67-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53e67-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53e67-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53e67-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="53e67-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53e67-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="53e67-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="53e67-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="53e67-125">**CBEN \_ DRAGBEGINW** (Unicode) e **CBEN \_ DRAGBEGINA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="53e67-125">**CBEN\_DRAGBEGINW** (Unicode) and **CBEN\_DRAGBEGINA** (ANSI)</span></span><br/>             |



 

 





