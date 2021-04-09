---
title: Codice di notifica NM_CLICK (visualizzazione elenco) (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente fa clic su un elemento con il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 7921bc27-54ca-4bb2-ac88-8267776661ab
keywords:
- Codice di notifica NM_CLICK (visualizzazione elenco) controlli Windows
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d766767bfb742e5d7ea7c22a1266540a40d65b9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121750"
---
# <a name="nm_click-list-view-notification-code"></a><span data-ttu-id="ad25a-105">\_Codice di notifica (visualizzazione elenco) Nm</span><span class="sxs-lookup"><span data-stu-id="ad25a-105">NM\_CLICK (list view) notification code</span></span>

<span data-ttu-id="ad25a-106">Inviato da un controllo di visualizzazione elenco quando l'utente fa clic su un elemento con il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="ad25a-106">Sent by a list-view control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="ad25a-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ad25a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ad25a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad25a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad25a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad25a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad25a-110">[Versione 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ad25a-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="ad25a-111">Puntatore a una struttura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="ad25a-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="ad25a-112">I membri **iItem**, **iSubItem** e **ptAction** di questa struttura contengono informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="ad25a-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad25a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad25a-113">Return value</span></span>

<span data-ttu-id="ad25a-114">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ad25a-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad25a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad25a-115">Remarks</span></span>

<span data-ttu-id="ad25a-116">Il membro **iItem** di *lParam* è valido solo se è stato fatto clic sull'etichetta dell'icona o della prima colonna.</span><span class="sxs-lookup"><span data-stu-id="ad25a-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="ad25a-117">Per determinare quale elemento è selezionato quando si fa clic su un punto qualsiasi in una riga, inviare un messaggio [**LVM \_ SUBITEMHITTEST**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="ad25a-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad25a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad25a-118">Requirements</span></span>



| <span data-ttu-id="ad25a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad25a-119">Requirement</span></span> | <span data-ttu-id="ad25a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ad25a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad25a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad25a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ad25a-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ad25a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad25a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad25a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ad25a-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ad25a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad25a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad25a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad25a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad25a-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





