---
title: Elemento LogonType (principalType)
description: Specifica il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Utilità di pianificazione elemento LogonType
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a382225f526f18731b8b9f0541e617cb31dfb4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301239"
---
# <a name="logontype-principaltype-element"></a><span data-ttu-id="27fea-104">Elemento LogonType (principalType)</span><span class="sxs-lookup"><span data-stu-id="27fea-104">LogonType (principalType) Element</span></span>

<span data-ttu-id="27fea-105">Specifica il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="27fea-105">Specifies the security logon method required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

<span data-ttu-id="27fea-106">L'elemento **LogonType** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="27fea-106">The **LogonType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="27fea-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="27fea-107">Parent element</span></span>



| <span data-ttu-id="27fea-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="27fea-108">Element</span></span>                                                                  | <span data-ttu-id="27fea-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="27fea-109">Derived from</span></span>                                                           | <span data-ttu-id="27fea-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27fea-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="27fea-111">**Principale**</span><span class="sxs-lookup"><span data-stu-id="27fea-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="27fea-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="27fea-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="27fea-113">Specifica le credenziali di sicurezza per un'entità.</span><span class="sxs-lookup"><span data-stu-id="27fea-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="27fea-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="27fea-114">Remarks</span></span>

<span data-ttu-id="27fea-115">L'elemento **LogonType** e l'elemento [**userid**](taskschedulerschema-userid-principaltype-element.md) vengono utilizzati insieme per definire l'utente necessario per eseguire le attività che utilizzano questa entità.</span><span class="sxs-lookup"><span data-stu-id="27fea-115">The **LogonType** element and the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="27fea-116">Per lo sviluppo di script, il tipo di accesso per l'entità viene specificato dalla proprietà [**Principal. LogonType**](principal-logontype.md) .</span><span class="sxs-lookup"><span data-stu-id="27fea-116">For scripting development, the logon type for the principal is specified by the [**Principal.LogonType**](principal-logontype.md) property.</span></span>

<span data-ttu-id="27fea-117">Per lo sviluppo in C++, il tipo di accesso per l'entità viene specificato dalla proprietà [**IPrincipal:: LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) .</span><span class="sxs-lookup"><span data-stu-id="27fea-117">For C++ development, the logon type for the principal is specified by the [**IPrincipal::LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) property.</span></span>

<span data-ttu-id="27fea-118">Questo elemento (definito dal tipo semplice [**LogonType**](taskschedulerschema-logontype-simpletype.md) ) deve avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="27fea-118">This element (defined by the [**logonType**](taskschedulerschema-logontype-simpletype.md) simple type) must have one of the following values.</span></span>

-   <span data-ttu-id="27fea-119">S4U: l'utente deve accedere utilizzando un servizio per l'accesso utente (S4U).</span><span class="sxs-lookup"><span data-stu-id="27fea-119">S4U: User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="27fea-120">Quando si usa un accesso S4U, nessuna password viene archiviata dal sistema e non è possibile accedere alla rete o ai file crittografati.</span><span class="sxs-lookup"><span data-stu-id="27fea-120">When an S4U logon is used, no password is stored by the system and there is no access to the network or encrypted files.</span></span>
-   <span data-ttu-id="27fea-121">Password: l'utente deve accedere usando una password.</span><span class="sxs-lookup"><span data-stu-id="27fea-121">Password: User must log on using a password.</span></span>
-   <span data-ttu-id="27fea-122">InteractiveToken: l'utente deve essere già connesso.</span><span class="sxs-lookup"><span data-stu-id="27fea-122">InteractiveToken: User must already be logged on.</span></span> <span data-ttu-id="27fea-123">L'attività verrà eseguita solo in una sessione interattiva esistente.</span><span class="sxs-lookup"><span data-stu-id="27fea-123">The task will be run only in an existing interactive session.</span></span>

<span data-ttu-id="27fea-124">Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività dispone di un tipo di accesso interattivo.</span><span class="sxs-lookup"><span data-stu-id="27fea-124">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="27fea-125">Per impostare il tipo di accesso dell'attività in modo che sia interattivo, specificare **InteractiveToken** nell' **<LogonType>** elemento dell'entità attività.</span><span class="sxs-lookup"><span data-stu-id="27fea-125">To set the task logon type to be interactive, specify **InteractiveToken** in the **<LogonType>** element of the task principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="27fea-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27fea-126">Requirements</span></span>



| <span data-ttu-id="27fea-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="27fea-127">Requirement</span></span> | <span data-ttu-id="27fea-128">Valore</span><span class="sxs-lookup"><span data-stu-id="27fea-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="27fea-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27fea-129">Minimum supported client</span></span><br/> | <span data-ttu-id="27fea-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27fea-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="27fea-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27fea-131">Minimum supported server</span></span><br/> | <span data-ttu-id="27fea-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27fea-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27fea-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27fea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27fea-134">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="27fea-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





