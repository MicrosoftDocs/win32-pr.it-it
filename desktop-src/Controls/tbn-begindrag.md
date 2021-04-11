---
title: Codice di notifica TBN_BEGINDRAG (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che l'utente ha iniziato a trascinare un pulsante in una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 244406e5-e13d-4c80-81fa-81b018b29ec1
keywords:
- Controlli di Windows per il codice di notifica TBN_BEGINDRAG
topic_type:
- apiref
api_name:
- TBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cfa7325d1a8e1eab27383d7df918c8896933bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119323"
---
# <a name="tbn_begindrag-notification-code"></a><span data-ttu-id="e96bf-105">\_Codice di notifica BEGINDRAG di TBN</span><span class="sxs-lookup"><span data-stu-id="e96bf-105">TBN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="e96bf-106">Notifica alla finestra padre di una barra degli strumenti che l'utente ha iniziato a trascinare un pulsante in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="e96bf-106">Notifies a toolbar's parent window that the user has begun dragging a button in a toolbar.</span></span> <span data-ttu-id="e96bf-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e96bf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_BEGINDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e96bf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e96bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e96bf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e96bf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e96bf-110">Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="e96bf-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="e96bf-111">Il membro **iItem** contiene l'identificatore di comando del pulsante trascinato.</span><span class="sxs-lookup"><span data-stu-id="e96bf-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e96bf-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e96bf-112">Return value</span></span>

<span data-ttu-id="e96bf-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e96bf-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e96bf-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e96bf-114">Requirements</span></span>



| <span data-ttu-id="e96bf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e96bf-115">Requirement</span></span> | <span data-ttu-id="e96bf-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e96bf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e96bf-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e96bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e96bf-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e96bf-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e96bf-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e96bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e96bf-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e96bf-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e96bf-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e96bf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e96bf-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e96bf-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





