---
title: Elemento Principal (principalType)
description: Specifica le credenziali di sicurezza per un'entità.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Utilità di pianificazione elemento principale
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301150"
---
# <a name="principal-principaltype-element"></a><span data-ttu-id="48a86-104">Elemento Principal (principalType)</span><span class="sxs-lookup"><span data-stu-id="48a86-104">Principal (principalType) Element</span></span>

<span data-ttu-id="48a86-105">Specifica le credenziali di sicurezza per un'entità.</span><span class="sxs-lookup"><span data-stu-id="48a86-105">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="48a86-106">Queste credenziali definiscono il contesto di sicurezza in cui viene eseguita un'attività.</span><span class="sxs-lookup"><span data-stu-id="48a86-106">These credentials define the security context that a task runs under.</span></span>

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

<span data-ttu-id="48a86-107">L'elemento **Principal** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="48a86-107">The **Principal** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="48a86-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="48a86-108">Parent element</span></span>



| <span data-ttu-id="48a86-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="48a86-109">Element</span></span>                                                               | <span data-ttu-id="48a86-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="48a86-110">Derived from</span></span>                                                             | <span data-ttu-id="48a86-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48a86-111">Description</span></span>                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="48a86-112">**Entità**</span><span class="sxs-lookup"><span data-stu-id="48a86-112">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md) | [<span data-ttu-id="48a86-113">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="48a86-113">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md) | <span data-ttu-id="48a86-114">Specifica le entità di sicurezza associate all'attività.</span><span class="sxs-lookup"><span data-stu-id="48a86-114">Specifies the security principals associated with the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="48a86-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="48a86-115">Child elements</span></span>



| <span data-ttu-id="48a86-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="48a86-116">Element</span></span>                                                                      | <span data-ttu-id="48a86-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="48a86-117">Type</span></span>                                                          | <span data-ttu-id="48a86-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48a86-118">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48a86-119">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="48a86-119">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md) | <span data-ttu-id="48a86-120">**string**</span><span class="sxs-lookup"><span data-stu-id="48a86-120">**string**</span></span>                                                    | <span data-ttu-id="48a86-121">Specifica il nome dell'entità visualizzata nell'interfaccia utente di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="48a86-121">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                 |
| [<span data-ttu-id="48a86-122">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="48a86-122">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)         | <span data-ttu-id="48a86-123">**string**</span><span class="sxs-lookup"><span data-stu-id="48a86-123">**string**</span></span>                                                    | <span data-ttu-id="48a86-124">Specifica l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="48a86-124">Specifies the identifier of the user group required to run tasks associated with the principal.</span></span><br/> |
| [<span data-ttu-id="48a86-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="48a86-125">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)     | [<span data-ttu-id="48a86-126">**logonType**</span><span class="sxs-lookup"><span data-stu-id="48a86-126">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md) | <span data-ttu-id="48a86-127">Specifica il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="48a86-127">Specifies the security logon method required to run those tasks associated with the principal.</span></span><br/>  |
| [<span data-ttu-id="48a86-128">**UserId**</span><span class="sxs-lookup"><span data-stu-id="48a86-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)           | <span data-ttu-id="48a86-129">**string**</span><span class="sxs-lookup"><span data-stu-id="48a86-129">**string**</span></span>                                                    | <span data-ttu-id="48a86-130">Specifica l'identificatore utente necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="48a86-130">Specifies the user identifier required to run tasks associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="48a86-131">Attributi</span><span class="sxs-lookup"><span data-stu-id="48a86-131">Attributes</span></span>



| <span data-ttu-id="48a86-132">Nome</span><span class="sxs-lookup"><span data-stu-id="48a86-132">Name</span></span> | <span data-ttu-id="48a86-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="48a86-133">Type</span></span> | <span data-ttu-id="48a86-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48a86-134">Description</span></span>                                        |
|------|------|----------------------------------------------------|
| <span data-ttu-id="48a86-135">Id</span><span class="sxs-lookup"><span data-stu-id="48a86-135">Id</span></span>   | <span data-ttu-id="48a86-136">ID</span><span class="sxs-lookup"><span data-stu-id="48a86-136">ID</span></span>   | <span data-ttu-id="48a86-137">Identificatore della definizione dell'entità.</span><span class="sxs-lookup"><span data-stu-id="48a86-137">Identifier of the principal definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="48a86-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="48a86-138">Remarks</span></span>

<span data-ttu-id="48a86-139">Per lo sviluppo di script, le credenziali di sicurezza per un'entità vengono specificate utilizzando l'oggetto [**Principal**](principal.md) .</span><span class="sxs-lookup"><span data-stu-id="48a86-139">For scripting development, the security credentials for a principal are specified using the [**Principal**](principal.md) object.</span></span>

<span data-ttu-id="48a86-140">Per lo sviluppo in C++, le credenziali di sicurezza per un'entità vengono specificate tramite l'interfaccia [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) .</span><span class="sxs-lookup"><span data-stu-id="48a86-140">For C++ development, the security credentials for a principal are specified using the [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) interface.</span></span>

<span data-ttu-id="48a86-141">Gli elementi figlio elencati sopra sono definiti dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="48a86-141">The child elements listed above are defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span> <span data-ttu-id="48a86-142">Per informazioni sulla sequenziazione di questi elementi figlio, vedere [**PrincipalType**](taskschedulerschema-principaltype-complextype.md).</span><span class="sxs-lookup"><span data-stu-id="48a86-142">For sequencing information for these child elements, see [**principalType**](taskschedulerschema-principaltype-complextype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="48a86-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="48a86-143">Examples</span></span>

<span data-ttu-id="48a86-144">Il codice XML seguente definisce un'entità con un identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="48a86-144">The following XML defines a principal with a user identifier.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



<span data-ttu-id="48a86-145">Il codice XML seguente definisce un'entità con un identificatore di gruppo.</span><span class="sxs-lookup"><span data-stu-id="48a86-145">The following XML defines a principal with a group identifier.</span></span>


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="48a86-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48a86-146">Requirements</span></span>



| <span data-ttu-id="48a86-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a86-147">Requirement</span></span> | <span data-ttu-id="48a86-148">Valore</span><span class="sxs-lookup"><span data-stu-id="48a86-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48a86-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48a86-149">Minimum supported client</span></span><br/> | <span data-ttu-id="48a86-150">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48a86-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="48a86-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48a86-151">Minimum supported server</span></span><br/> | <span data-ttu-id="48a86-152">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48a86-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48a86-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48a86-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a86-154">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="48a86-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





