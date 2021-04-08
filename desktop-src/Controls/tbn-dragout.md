---
title: Codice di notifica TBN_DRAGOUT (COMmctrl. h)
description: Inviato da un controllo Toolbar quando l'utente fa clic su un pulsante e quindi sposta il cursore dal pulsante. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- Controlli di Windows per il codice di notifica TBN_DRAGOUT
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048111"
---
# <a name="tbn_dragout-notification-code"></a><span data-ttu-id="3fe71-105">Codice di notifica per il \_ trascinamento TBN</span><span class="sxs-lookup"><span data-stu-id="3fe71-105">TBN\_DRAGOUT notification code</span></span>

<span data-ttu-id="3fe71-106">Inviato da un controllo Toolbar quando l'utente fa clic su un pulsante e quindi sposta il cursore dal pulsante.</span><span class="sxs-lookup"><span data-stu-id="3fe71-106">Sent by a toolbar control when the user clicks a button and then moves the cursor off the button.</span></span> <span data-ttu-id="3fe71-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe71-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3fe71-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fe71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fe71-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fe71-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fe71-110">Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="3fe71-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="3fe71-111">Per questo codice di notifica, sono validi solo i membri **HDR** e **iItem** di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="3fe71-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="3fe71-112">Il membro **iItem** della struttura contiene l'identificatore di comando del pulsante trascinato.</span><span class="sxs-lookup"><span data-stu-id="3fe71-112">The **iItem** member of this structure contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fe71-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fe71-113">Return value</span></span>

<span data-ttu-id="3fe71-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3fe71-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fe71-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fe71-115">Remarks</span></span>

<span data-ttu-id="3fe71-116">Questo codice di notifica consente a un'applicazione di implementare la funzionalità di trascinamento della selezione per i pulsanti della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="3fe71-116">This notification code allows an application to implement drag-and-drop functionality for toolbar buttons.</span></span> <span data-ttu-id="3fe71-117">Quando si elabora questo codice di notifica, l'applicazione avvierà l'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="3fe71-117">When processing this notification code, the application will begin the drag-and-drop operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fe71-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fe71-118">Requirements</span></span>



| <span data-ttu-id="3fe71-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fe71-119">Requirement</span></span> | <span data-ttu-id="3fe71-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3fe71-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fe71-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fe71-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3fe71-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fe71-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fe71-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fe71-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3fe71-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3fe71-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fe71-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fe71-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fe71-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fe71-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





