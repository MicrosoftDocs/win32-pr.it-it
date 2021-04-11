---
title: Codice di notifica DTN_WMKEYDOWN (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) quando l'utente digita in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- Controlli di Windows per il codice di notifica DTN_WMKEYDOWN
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119167"
---
# <a name="dtn_wmkeydown-notification-code"></a><span data-ttu-id="db1b4-105">\_Codice di notifica WMKEYDOWN di DTN</span><span class="sxs-lookup"><span data-stu-id="db1b4-105">DTN\_WMKEYDOWN notification code</span></span>

<span data-ttu-id="db1b4-106">Inviato da un controllo di selezione data e ora (DTP) quando l'utente digita in un campo di callback.</span><span class="sxs-lookup"><span data-stu-id="db1b4-106">Sent by a date and time picker (DTP) control when the user types in a callback field.</span></span> <span data-ttu-id="db1b4-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="db1b4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a><span data-ttu-id="db1b4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="db1b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db1b4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db1b4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db1b4-110">Puntatore a una struttura [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) contenente informazioni su questa istanza del codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="db1b4-110">A pointer to an [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) structure containing information about this instance of the notification code.</span></span> <span data-ttu-id="db1b4-111">La struttura include informazioni sulla chiave digitata dall'utente, la sottostringa che definisce il campo di callback e la data e l'ora di sistema correnti.</span><span class="sxs-lookup"><span data-stu-id="db1b4-111">The structure includes information about the key that the user typed, the substring that defines the callback field, and the current system date and time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db1b4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db1b4-112">Return value</span></span>

<span data-ttu-id="db1b4-113">Il proprietario del controllo deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="db1b4-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="db1b4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="db1b4-114">Remarks</span></span>

<span data-ttu-id="db1b4-115">La gestione di questo codice di notifica consente al proprietario del controllo di fornire risposte specifiche alle sequenze di tasti all'interno dei campi di callback del controllo.</span><span class="sxs-lookup"><span data-stu-id="db1b4-115">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="db1b4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db1b4-116">Requirements</span></span>



| <span data-ttu-id="db1b4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="db1b4-117">Requirement</span></span> | <span data-ttu-id="db1b4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="db1b4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db1b4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db1b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="db1b4-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db1b4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db1b4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db1b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="db1b4-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db1b4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db1b4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db1b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="db1b4-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db1b4-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="db1b4-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="db1b4-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="db1b4-126">**DTN \_ WMKEYDOWNW** (Unicode) e **DTN \_ WMKEYDOWNA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="db1b4-126">**DTN\_WMKEYDOWNW** (Unicode) and **DTN\_WMKEYDOWNA** (ANSI)</span></span><br/>               |



 

 





