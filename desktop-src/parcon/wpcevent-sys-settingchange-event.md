---
description: Evento a livello di sistema generato da un'impostazione di controlli padre.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: Evento WPCEVENT_SYS_SETTINGCHANGE (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318042"
---
# <a name="wpcevent_sys_settingchange-event"></a><span data-ttu-id="1777b-103">\_Evento WPCEVENT sys \_ SETTINGCHANGE</span><span class="sxs-lookup"><span data-stu-id="1777b-103">WPCEVENT\_SYS\_SETTINGCHANGE event</span></span>

<span data-ttu-id="1777b-104">Evento a livello di sistema generato da un'impostazione di controlli padre.</span><span class="sxs-lookup"><span data-stu-id="1777b-104">System-level event generated on a Parental Controls setting change.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a><span data-ttu-id="1777b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="1777b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1777b-106">*Classe*</span><span class="sxs-lookup"><span data-stu-id="1777b-106">*Class*</span></span> 
</dt> <dd>

<span data-ttu-id="1777b-107">Classe che genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="1777b-107">The class that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="1777b-108">*Impostazione*</span><span class="sxs-lookup"><span data-stu-id="1777b-108">*Setting*</span></span> 
</dt> <dd>

<span data-ttu-id="1777b-109">Valore dell'enumerazione di **\_ Impostazioni WPC** .</span><span class="sxs-lookup"><span data-stu-id="1777b-109">A value of the **WPC\_SETTINGS** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="1777b-110">*Proprietario*</span><span class="sxs-lookup"><span data-stu-id="1777b-110">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="1777b-111">Identificatore di sicurezza dell'utente che genera l'evento.</span><span class="sxs-lookup"><span data-stu-id="1777b-111">The security identifier of the user who is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="1777b-112">*OldVal*</span><span class="sxs-lookup"><span data-stu-id="1777b-112">*OldVal*</span></span> 
</dt> <dd>

<span data-ttu-id="1777b-113">Valore precedente di questa impostazione, se eliminato o modificato.</span><span class="sxs-lookup"><span data-stu-id="1777b-113">The previous value of this setting, if deleted or changed.</span></span>

</dd> <dt>

<span data-ttu-id="1777b-114">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="1777b-114">*NewVal*</span></span> 
</dt> <dd>

<span data-ttu-id="1777b-115">Nuovo valore di questa impostazione, se aggiunto o modificato.</span><span class="sxs-lookup"><span data-stu-id="1777b-115">The new value of this setting, if added or changed.</span></span>

</dd> <dt>

<span data-ttu-id="1777b-116">*Motivo*</span><span class="sxs-lookup"><span data-stu-id="1777b-116">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="1777b-117">Valore dell'enumerazione [**WPCFLAG che \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) indica le informazioni sugli eventi che vengono bloccati dall'utilizzo e sui controlli.</span><span class="sxs-lookup"><span data-stu-id="1777b-117">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="1777b-118">*Facoltativo*</span><span class="sxs-lookup"><span data-stu-id="1777b-118">*Optional*</span></span> 
</dt> <dd>

<span data-ttu-id="1777b-119">Campo facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1777b-119">An optional field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1777b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1777b-120">Requirements</span></span>



| <span data-ttu-id="1777b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1777b-121">Requirement</span></span> | <span data-ttu-id="1777b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1777b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1777b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1777b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1777b-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1777b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1777b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1777b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1777b-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1777b-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="1777b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1777b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1777b-128"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="1777b-128"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1777b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1777b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1777b-130">Uso delle API di registrazione per i controlli padre</span><span class="sxs-lookup"><span data-stu-id="1777b-130">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="1777b-131">**\_argomenti \_ CONVERSATIONINITEVENT di WPC**</span><span class="sxs-lookup"><span data-stu-id="1777b-131">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




