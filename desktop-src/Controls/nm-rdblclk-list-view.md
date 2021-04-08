---
title: Codice di notifica NM_RDBLCLK (visualizzazione elenco) (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente fa doppio clic su un elemento con il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- Codice di notifica NM_RDBLCLK (visualizzazione elenco) controlli Windows
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41832b228fe40b212c0aba809b15022c6f7b39ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965008"
---
# <a name="nm_rdblclk-list-view-notification-code"></a><span data-ttu-id="393c2-105">\_Codice di notifica di RDBLCLK Nm (visualizzazione elenco)</span><span class="sxs-lookup"><span data-stu-id="393c2-105">NM\_RDBLCLK (list view) notification code</span></span>

<span data-ttu-id="393c2-106">Inviato da un controllo di visualizzazione elenco quando l'utente fa doppio clic su un elemento con il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="393c2-106">Sent by a list-view control when the user double-clicks an item with the right mouse button.</span></span> <span data-ttu-id="393c2-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="393c2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="393c2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="393c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="393c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="393c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="393c2-110">[Versione 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="393c2-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="393c2-111">Puntatore a una struttura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="393c2-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="393c2-112">I membri **iItem**, **iSubItem** e **ptAction** di questa struttura contengono informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="393c2-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="393c2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="393c2-113">Return value</span></span>

<span data-ttu-id="393c2-114">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="393c2-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="393c2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="393c2-115">Remarks</span></span>

<span data-ttu-id="393c2-116">Il membro **iItem** di *lParam* è valido solo se è stato fatto clic sull'etichetta dell'icona o della prima colonna.</span><span class="sxs-lookup"><span data-stu-id="393c2-116">The **iItem** member of *lParam* is valid only if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="393c2-117">Per determinare quale elemento è selezionato quando si fa clic su un punto qualsiasi in una riga, inviare un messaggio [**LVM \_ SUBITEMHITTEST**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="393c2-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="393c2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="393c2-118">Requirements</span></span>



| <span data-ttu-id="393c2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="393c2-119">Requirement</span></span> | <span data-ttu-id="393c2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="393c2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="393c2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="393c2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="393c2-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="393c2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="393c2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="393c2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="393c2-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="393c2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="393c2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="393c2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="393c2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="393c2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





