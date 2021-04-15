---
title: Messaggio TBN_DELETINGBUTTON (COMmctrl. h)
description: Inviato da un controllo Toolbar quando un pulsante sta per essere eliminato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- Controlli di Windows Message TBN_DELETINGBUTTON
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26337fd1abc6c67351fe2b38e83ee7d90a11f6e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517511"
---
# <a name="tbn_deletingbutton-message"></a><span data-ttu-id="e154b-105">\_Messaggio TBN DELETINGBUTTON</span><span class="sxs-lookup"><span data-stu-id="e154b-105">TBN\_DELETINGBUTTON message</span></span>

<span data-ttu-id="e154b-106">Inviato da un controllo Toolbar quando un pulsante sta per essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="e154b-106">Sent by a toolbar control when a button is about to be deleted.</span></span> <span data-ttu-id="e154b-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e154b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e154b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e154b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e154b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e154b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e154b-110">Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) contenente informazioni sul pulsante da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e154b-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about the button being deleted.</span></span> <span data-ttu-id="e154b-111">Per questo codice di notifica, sono validi solo i membri **HDR** e **iItem** di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="e154b-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="e154b-112">Il membro **iItem** della struttura contiene l'identificatore di comando del pulsante da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e154b-112">The **iItem** member of this structure contains the command identifier of the button being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e154b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e154b-113">Return value</span></span>

<span data-ttu-id="e154b-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e154b-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e154b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e154b-115">Requirements</span></span>



| <span data-ttu-id="e154b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e154b-116">Requirement</span></span> | <span data-ttu-id="e154b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e154b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e154b-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e154b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e154b-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e154b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e154b-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e154b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e154b-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e154b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e154b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e154b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e154b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e154b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





