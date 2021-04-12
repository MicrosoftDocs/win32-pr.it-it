---
title: Elemento UserId (logonTriggerType)
description: Identificatore dell'utente. L'attività viene avviata quando l'utente accede al computer.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
keywords:
- Elemento UserId Utilità di pianificazione
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519109"
---
# <a name="userid-logontriggertype-element"></a><span data-ttu-id="5c8ed-105">Elemento UserId (logonTriggerType)</span><span class="sxs-lookup"><span data-stu-id="5c8ed-105">UserId (logonTriggerType) Element</span></span>

<span data-ttu-id="5c8ed-106">Identificatore dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5c8ed-106">Identifier of the user.</span></span> <span data-ttu-id="5c8ed-107">L'attività viene avviata quando l'utente accede al computer.</span><span class="sxs-lookup"><span data-stu-id="5c8ed-107">The task is started when this user logs on to the computer.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="5c8ed-108">L'elemento **userid** è definito dal tipo complesso [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5c8ed-108">The **UserId** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5c8ed-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="5c8ed-109">Parent element</span></span>



| <span data-ttu-id="5c8ed-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="5c8ed-110">Element</span></span>                                                                       | <span data-ttu-id="5c8ed-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="5c8ed-111">Derived from</span></span>                                                                 | <span data-ttu-id="5c8ed-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c8ed-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="5c8ed-113">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="5c8ed-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="5c8ed-114">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5c8ed-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="5c8ed-115">Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="5c8ed-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5c8ed-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c8ed-116">Remarks</span></span>

<span data-ttu-id="5c8ed-117">Per lo sviluppo di script, l'identificatore utente per il trigger LOGON viene specificato mediante la proprietà [**LogonTrigger. UserID**](logontrigger-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="5c8ed-117">For scripting development, the user identifier for the logon trigger is specified using the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span>

<span data-ttu-id="5c8ed-118">Per lo sviluppo in C++, l'identificatore utente per il trigger LOGON viene specificato tramite la proprietà [**ILogonTrigger:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="5c8ed-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="5c8ed-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c8ed-119">Examples</span></span>

<span data-ttu-id="5c8ed-120">Per un esempio completo del codice XML per un'attività che specifica un trigger LOGON, vedere [esempio di trigger LOGON (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="5c8ed-120">For a complete example of the XML for a task that specifies a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c8ed-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c8ed-121">Requirements</span></span>



| <span data-ttu-id="5c8ed-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c8ed-122">Requirement</span></span> | <span data-ttu-id="5c8ed-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5c8ed-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c8ed-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c8ed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5c8ed-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c8ed-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c8ed-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c8ed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5c8ed-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c8ed-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c8ed-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c8ed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c8ed-129">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5c8ed-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5c8ed-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5c8ed-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





