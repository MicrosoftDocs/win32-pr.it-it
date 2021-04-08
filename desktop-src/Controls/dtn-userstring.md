---
title: Codice di notifica DTN_USERSTRING (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) quando un utente completa la modifica di una stringa nel controllo.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- Controlli di Windows per il codice di notifica DTN_USERSTRING
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873437"
---
# <a name="dtn_userstring-notification-code"></a><span data-ttu-id="120d1-104">\_Codice di notifica USERSTRING di DTN</span><span class="sxs-lookup"><span data-stu-id="120d1-104">DTN\_USERSTRING notification code</span></span>

<span data-ttu-id="120d1-105">Inviato da un controllo di selezione data e ora (DTP) quando un utente completa la modifica di una stringa nel controllo.</span><span class="sxs-lookup"><span data-stu-id="120d1-105">Sent by a date and time picker (DTP) control when a user finishes editing a string in the control.</span></span> <span data-ttu-id="120d1-106">Questo codice di notifica viene inviato solo dai controlli DTP impostati sullo stile [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="120d1-106">This notification code is only sent by DTP controls that are set to the [**DTS\_APPCANPARSE**](date-and-time-picker-control-styles.md) style.</span></span> <span data-ttu-id="120d1-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="120d1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="120d1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="120d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="120d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="120d1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="120d1-110">Puntatore a una struttura [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) che contiene informazioni sull'istanza del codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="120d1-110">A pointer to an [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) structure that contains information about the instance of the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="120d1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="120d1-111">Return value</span></span>

<span data-ttu-id="120d1-112">Il proprietario del controllo deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="120d1-112">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="120d1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="120d1-113">Remarks</span></span>

<span data-ttu-id="120d1-114">La gestione di questo codice di notifica consente al proprietario di fornire risposte personalizzate alle stringhe immesse nel controllo dall'utente.</span><span class="sxs-lookup"><span data-stu-id="120d1-114">Handling this notification code allows the owner to provide custom responses to strings entered into the control by the user.</span></span> <span data-ttu-id="120d1-115">Il proprietario deve essere preparato per analizzare la stringa di input ed eseguire l'azione, se necessario.</span><span class="sxs-lookup"><span data-stu-id="120d1-115">The owner must be prepared to parse the input string and take action if necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="120d1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="120d1-116">Requirements</span></span>



| <span data-ttu-id="120d1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="120d1-117">Requirement</span></span> | <span data-ttu-id="120d1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="120d1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="120d1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="120d1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="120d1-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="120d1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="120d1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="120d1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="120d1-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="120d1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="120d1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="120d1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="120d1-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="120d1-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="120d1-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="120d1-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="120d1-126">**DTN \_ USERSTRINGW** (Unicode) e **DTN \_ USERSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="120d1-126">**DTN\_USERSTRINGW** (Unicode) and **DTN\_USERSTRINGA** (ANSI)</span></span><br/>             |



 

 





