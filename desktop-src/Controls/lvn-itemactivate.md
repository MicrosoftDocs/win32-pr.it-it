---
title: Codice di notifica LVN_ITEMACTIVATE (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente attiva un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- Controlli di Windows per il codice di notifica LVN_ITEMACTIVATE
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121762"
---
# <a name="lvn_itemactivate-notification-code"></a><span data-ttu-id="f286c-105">\_Codice di notifica ITEMACTIVATE di LVN</span><span class="sxs-lookup"><span data-stu-id="f286c-105">LVN\_ITEMACTIVATE notification code</span></span>

<span data-ttu-id="f286c-106">Inviato da un controllo di visualizzazione elenco quando l'utente attiva un elemento.</span><span class="sxs-lookup"><span data-stu-id="f286c-106">Sent by a list-view control when the user activates an item.</span></span> <span data-ttu-id="f286c-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f286c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a><span data-ttu-id="f286c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f286c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f286c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f286c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f286c-110">[Versione 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="f286c-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="f286c-111">Puntatore a una struttura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="f286c-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains information about this notification code.</span></span>

<span data-ttu-id="f286c-112">[Versione 4,70](common-control-versions.md) e precedenti.</span><span class="sxs-lookup"><span data-stu-id="f286c-112">[Version 4.70](common-control-versions.md) and earlier.</span></span> <span data-ttu-id="f286c-113">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="f286c-113">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f286c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f286c-114">Return value</span></span>

<span data-ttu-id="f286c-115">L'applicazione che riceve il codice di notifica deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="f286c-115">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f286c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f286c-116">Remarks</span></span>

<span data-ttu-id="f286c-117">Per ottenere gli elementi attivati, l'applicazione ricevente deve usare il messaggio [**LVM \_ GETSELECTEDCOUNT**](lvm-getselectedcount.md) per recuperare il numero di elementi selezionati e quindi inviare il messaggio [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) con **LVNI \_ selezionato** fino a quando non sono stati recuperati tutti gli elementi.</span><span class="sxs-lookup"><span data-stu-id="f286c-117">To obtain the items being activated, the receiving application should use the [**LVM\_GETSELECTEDCOUNT**](lvm-getselectedcount.md) message to retrieve the number of items that are selected and then send the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message with **LVNI\_SELECTED** until all of the items have been retrieved.</span></span>

## <a name="requirements"></a><span data-ttu-id="f286c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f286c-118">Requirements</span></span>



| <span data-ttu-id="f286c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f286c-119">Requirement</span></span> | <span data-ttu-id="f286c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f286c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f286c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f286c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f286c-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f286c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f286c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f286c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f286c-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f286c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f286c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f286c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f286c-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f286c-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





