---
title: Codice di notifica LVN_INCREMENTALSEARCH (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata avviata una ricerca incrementale. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- Controlli di Windows per il codice di notifica LVN_INCREMENTALSEARCH
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302801"
---
# <a name="lvn_incrementalsearch-notification-code"></a><span data-ttu-id="55208-105">\_Codice di notifica INCREMENTALSEARCH di LVN</span><span class="sxs-lookup"><span data-stu-id="55208-105">LVN\_INCREMENTALSEARCH notification code</span></span>

<span data-ttu-id="55208-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata avviata una ricerca incrementale.</span><span class="sxs-lookup"><span data-stu-id="55208-106">Notifies a list-view control's parent window that an incremental search has started.</span></span> <span data-ttu-id="55208-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="55208-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="55208-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="55208-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55208-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55208-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55208-110">Puntatore a una struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) che descrive il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="55208-110">Pointer to a [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that describes the notification code.</span></span> <span data-ttu-id="55208-111">Il chiamante è responsabile dell'allocazione di questa struttura, incluse le strutture [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) e [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenute.</span><span class="sxs-lookup"><span data-stu-id="55208-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) and [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structures.</span></span> <span data-ttu-id="55208-112">Impostare i membri della struttura **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="55208-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="55208-113">Il membro del **codice** deve essere impostato su LVN \_ INCREMENTALSEARCH.</span><span class="sxs-lookup"><span data-stu-id="55208-113">The **code** member must be set to LVN\_INCREMENTALSEARCH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55208-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55208-114">Return value</span></span>

<span data-ttu-id="55208-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="55208-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55208-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="55208-116">Remarks</span></span>

<span data-ttu-id="55208-117">Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .</span><span class="sxs-lookup"><span data-stu-id="55208-117">The notification receiver casts *lParam* to retrieve the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span> <span data-ttu-id="55208-118">Il parametro *wParam* contiene l'ID del controllo che invia il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="55208-118">The *wParam* parameter contains the ID of the control that sends this notification code.</span></span>

<span data-ttu-id="55208-119">Questo codice di notifica fornisce a un'applicazione (o al ricevitore di notifiche) la possibilità di personalizzare una ricerca incrementale.</span><span class="sxs-lookup"><span data-stu-id="55208-119">This notification code gives an application (or the notification receiver) the opportunity to customize an incremental search.</span></span> <span data-ttu-id="55208-120">Se, ad esempio, gli elementi di ricerca sono numerici, l'applicazione può eseguire una ricerca numerica anziché una stringa.</span><span class="sxs-lookup"><span data-stu-id="55208-120">For example, if the search items are numeric, the application can perform a numerical search instead of a string search.</span></span>

<span data-ttu-id="55208-121">L'applicazione imposta il membro **lParam** della struttura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenuto nella struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) sul risultato della ricerca o su un altro valore definito dall'applicazione per interrompere la ricerca e indicare al controllo come continuare.</span><span class="sxs-lookup"><span data-stu-id="55208-121">The application sets the **lParam** member of the [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure contained in [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure  to the result of the search, or to another application defined value to fail the search and indicate to the control how to proceed.</span></span>

## <a name="requirements"></a><span data-ttu-id="55208-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55208-122">Requirements</span></span>



| <span data-ttu-id="55208-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="55208-123">Requirement</span></span> | <span data-ttu-id="55208-124">Valore</span><span class="sxs-lookup"><span data-stu-id="55208-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55208-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55208-125">Minimum supported client</span></span><br/> | <span data-ttu-id="55208-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55208-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="55208-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55208-127">Minimum supported server</span></span><br/> | <span data-ttu-id="55208-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55208-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55208-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55208-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="55208-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55208-130"><dt>Commctrl.h</dt></span></span> </dl>   |
| <span data-ttu-id="55208-131">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="55208-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="55208-132">**LVN \_ INCREMENTALSEARCHW** (Unicode) e **LVN \_ INCREMENTALSEARCHA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="55208-132">**LVN\_INCREMENTALSEARCHW** (Unicode) and **LVN\_INCREMENTALSEARCHA** (ANSI)</span></span><br/> |



 

 





