---
description: Evento per utente fornito per la registrazione dell'avvio delle conversazioni da parte dei client di messaggistica immediata.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: Evento WPCEVENT_IM_INVITATION (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316430"
---
# <a name="wpcevent_im_invitation-event"></a><span data-ttu-id="62132-103">\_ \_ Evento invito WPCEVENT im</span><span class="sxs-lookup"><span data-stu-id="62132-103">WPCEVENT\_IM\_INVITATION event</span></span>

<span data-ttu-id="62132-104">Evento per utente fornito per la registrazione dell'avvio delle conversazioni da parte dei client di messaggistica immediata.</span><span class="sxs-lookup"><span data-stu-id="62132-104">Per-user event provided for logging initiation of conversations by Instant Messaging clients.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="62132-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="62132-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62132-106">*AppName*</span><span class="sxs-lookup"><span data-stu-id="62132-106">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="62132-107">Nome dell'applicazione che genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="62132-107">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="62132-108">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="62132-108">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="62132-109">Stringa di versione per l'applicazione che genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="62132-109">The version string for the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="62132-110">*AccountName*</span><span class="sxs-lookup"><span data-stu-id="62132-110">*AccountName*</span></span> 
</dt> <dd>

<span data-ttu-id="62132-111">Stringa di identità dell'account di messaggistica immediata.</span><span class="sxs-lookup"><span data-stu-id="62132-111">The instant messaging account identity string.</span></span>

</dd> <dt>

<span data-ttu-id="62132-112">*ConvID*</span><span class="sxs-lookup"><span data-stu-id="62132-112">*ConvID*</span></span> 
</dt> <dd>

<span data-ttu-id="62132-113">Identificatore per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="62132-113">The identifier for the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="62132-114">*RequestingIP*</span><span class="sxs-lookup"><span data-stu-id="62132-114">*RequestingIP*</span></span> 
</dt> <dd>

<span data-ttu-id="62132-115">Stringa contenente l'indirizzo IP del computer che invia l'invito.</span><span class="sxs-lookup"><span data-stu-id="62132-115">A string that contains the IP address of the computer that is sending the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="62132-116">*Mittente*</span><span class="sxs-lookup"><span data-stu-id="62132-116">*Sender*</span></span> 
</dt> <dd>

<span data-ttu-id="62132-117">Stringa di identità dell'account di messaggistica immediata per l'account che ha emesso l'invito.</span><span class="sxs-lookup"><span data-stu-id="62132-117">The instant messaging account identity string for the account that is issuing the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="62132-118">*Motivo*</span><span class="sxs-lookup"><span data-stu-id="62132-118">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="62132-119">Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.</span><span class="sxs-lookup"><span data-stu-id="62132-119">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="62132-120">*RecipCount*</span><span class="sxs-lookup"><span data-stu-id="62132-120">*RecipCount*</span></span> 
</dt> <dd>

<span data-ttu-id="62132-121">Numero di destinatari che ricevono l'invito e che hanno identità definite nel campo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="62132-121">The count of recipients who are receiving the invitation and who have identities defined in the recipient field.</span></span>

</dd> <dt>

<span data-ttu-id="62132-122">*Recipient*</span><span class="sxs-lookup"><span data-stu-id="62132-122">*Recipient*</span></span> 
</dt> <dd>

<span data-ttu-id="62132-123">Stringa delimitata che contiene le stringhe di identità dell'account di messaggistica immediata per i destinatari dell'invito.</span><span class="sxs-lookup"><span data-stu-id="62132-123">A delimited string that contains instant messaging account identity strings for the recipients of the invitation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62132-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62132-124">Requirements</span></span>



| <span data-ttu-id="62132-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="62132-125">Requirement</span></span> | <span data-ttu-id="62132-126">Valore</span><span class="sxs-lookup"><span data-stu-id="62132-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62132-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62132-127">Minimum supported client</span></span><br/> | <span data-ttu-id="62132-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62132-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62132-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62132-129">Minimum supported server</span></span><br/> | <span data-ttu-id="62132-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="62132-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="62132-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62132-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="62132-132"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="62132-132"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62132-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62132-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62132-134">Uso delle API di registrazione per i controlli padre</span><span class="sxs-lookup"><span data-stu-id="62132-134">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="62132-135">**\_argomenti \_ CONVERSATIONINITEVENT di WPC**</span><span class="sxs-lookup"><span data-stu-id="62132-135">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




