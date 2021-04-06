---
title: Codice di notifica NM_HOVER (visualizzazione elenco) (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando il mouse viene spostato su un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0d4a2eee-9c98-43d1-bc05-226d91c0480a
keywords:
- Codice di notifica NM_HOVER (visualizzazione elenco) controlli Windows
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60606dfac73e13b0439ce861f37cb4ec941fda3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873305"
---
# <a name="nm_hover-list-view-notification-code"></a><span data-ttu-id="6aeec-105">Codice di notifica del passaggio del mouse su NM \_ (visualizzazione elenco)</span><span class="sxs-lookup"><span data-stu-id="6aeec-105">NM\_HOVER (list view) notification code</span></span>

<span data-ttu-id="6aeec-106">Inviato da un controllo di visualizzazione elenco quando il mouse viene spostato su un elemento.</span><span class="sxs-lookup"><span data-stu-id="6aeec-106">Sent by a list-view control when the mouse hovers over an item.</span></span> <span data-ttu-id="6aeec-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6aeec-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6aeec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6aeec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aeec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6aeec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6aeec-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="6aeec-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aeec-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6aeec-111">Return value</span></span>

<span data-ttu-id="6aeec-112">Restituisce zero per consentire alla visualizzazione elenco di elaborare normalmente il passaggio del mouse o un valore diverso da zero per impedire l'elaborazione del passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="6aeec-112">Return zero to allow the list view to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aeec-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6aeec-113">Requirements</span></span>



| <span data-ttu-id="6aeec-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aeec-114">Requirement</span></span> | <span data-ttu-id="6aeec-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6aeec-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6aeec-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aeec-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6aeec-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6aeec-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6aeec-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aeec-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6aeec-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6aeec-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6aeec-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6aeec-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6aeec-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aeec-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





