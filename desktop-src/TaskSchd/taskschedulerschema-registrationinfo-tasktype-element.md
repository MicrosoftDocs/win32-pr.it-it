---
title: Elemento RegistrationInfo (taskType)
description: Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- informazioni di registrazione Utilità di pianificazione, elemento XML
- Utilità di pianificazione elemento RegistrationInfo
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477783"
---
# <a name="registrationinfo-tasktype-element"></a><span data-ttu-id="db7a6-105">Elemento RegistrationInfo (taskType)</span><span class="sxs-lookup"><span data-stu-id="db7a6-105">RegistrationInfo (taskType) Element</span></span>

<span data-ttu-id="db7a6-106">Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="db7a6-106">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

<span data-ttu-id="db7a6-107">L'elemento **RegistrationInfo** è definito dal tipo complesso [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="db7a6-107">The **RegistrationInfo** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="db7a6-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="db7a6-108">Parent element</span></span>



| <span data-ttu-id="db7a6-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="db7a6-109">Element</span></span>                                          | <span data-ttu-id="db7a6-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="db7a6-110">Derived from</span></span>                                                 | <span data-ttu-id="db7a6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db7a6-111">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="db7a6-112">**Attività**</span><span class="sxs-lookup"><span data-stu-id="db7a6-112">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="db7a6-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="db7a6-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="db7a6-114">Definisce l'attività eseguita dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="db7a6-114">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="db7a6-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="db7a6-115">Child elements</span></span>



| <span data-ttu-id="db7a6-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="db7a6-116">Element</span></span>                                                                                                                  | <span data-ttu-id="db7a6-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="db7a6-117">Type</span></span>     | <span data-ttu-id="db7a6-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db7a6-118">Description</span></span>                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db7a6-119">**Autore (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="db7a6-119">**Author (registrationInfoType)**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="db7a6-120">string</span><span class="sxs-lookup"><span data-stu-id="db7a6-120">string</span></span>   | <span data-ttu-id="db7a6-121">Specifica l'autore dell'attività.</span><span class="sxs-lookup"><span data-stu-id="db7a6-121">Specifies the author of the task.</span></span><br/>                                                                              |
| [<span data-ttu-id="db7a6-122">**Data (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="db7a6-122">**Date (registrationInfoType)**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="db7a6-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="db7a6-123">dateTime</span></span> | <span data-ttu-id="db7a6-124">Specifica la data e l'ora di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="db7a6-124">Specifies the date and time when the task is registered.</span></span><br/>                                                       |
| [<span data-ttu-id="db7a6-125">**Descrizione (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="db7a6-125">**Description (registrationInfoType)**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="db7a6-126">string</span><span class="sxs-lookup"><span data-stu-id="db7a6-126">string</span></span>   | <span data-ttu-id="db7a6-127">Specifica la descrizione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="db7a6-127">Specifies the description of the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="db7a6-128">**Documentazione (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="db7a6-128">**Documentation (registrationInfoType)**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="db7a6-129">string</span><span class="sxs-lookup"><span data-stu-id="db7a6-129">string</span></span>   | <span data-ttu-id="db7a6-130">Specifica qualsiasi documentazione aggiuntiva per l'attività.</span><span class="sxs-lookup"><span data-stu-id="db7a6-130">Specifies any additional documentation for the task.</span></span><br/>                                                           |
| [<span data-ttu-id="db7a6-131">**SecurityDescriptor (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="db7a6-131">**SecurityDescriptor (registrationInfoType)**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="db7a6-132">string</span><span class="sxs-lookup"><span data-stu-id="db7a6-132">string</span></span>   | <span data-ttu-id="db7a6-133">Specifica il descrittore di sicurezza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="db7a6-133">Specifies the security descriptor of the task.</span></span><br/>                                                                 |
| [<span data-ttu-id="db7a6-134">**Origine (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="db7a6-134">**Source (registrationInfoType)**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="db7a6-135">string</span><span class="sxs-lookup"><span data-stu-id="db7a6-135">string</span></span>   | <span data-ttu-id="db7a6-136">Specifica la posizione da cui ha avuto origine l'attività.</span><span class="sxs-lookup"><span data-stu-id="db7a6-136">Specifies where the task originated from.</span></span> <span data-ttu-id="db7a6-137">Ad esempio, da un componente, da un servizio, da un'applicazione o da un utente.</span><span class="sxs-lookup"><span data-stu-id="db7a6-137">For example, from a component, a service, an application, or a user.</span></span><br/> |
| [<span data-ttu-id="db7a6-138">**URI (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="db7a6-138">**URI (registrationInfoType)**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="db7a6-139">anyURI</span><span class="sxs-lookup"><span data-stu-id="db7a6-139">anyURI</span></span>   | <span data-ttu-id="db7a6-140">Specifica l'URI dell'attività.</span><span class="sxs-lookup"><span data-stu-id="db7a6-140">Specifies the URI of the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="db7a6-141">**Versione (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="db7a6-141">**Version (registrationInfoType)**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="db7a6-142">string</span><span class="sxs-lookup"><span data-stu-id="db7a6-142">string</span></span>   | <span data-ttu-id="db7a6-143">Specifica il numero di versione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="db7a6-143">Specifies the version number of the task.</span></span><br/>                                                                      |



## <a name="remarks"></a><span data-ttu-id="db7a6-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="db7a6-144">Remarks</span></span>

<span data-ttu-id="db7a6-145">Per lo sviluppo di script, le informazioni di registrazione di un'attività vengono specificate utilizzando la proprietà [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="db7a6-145">For scripting development, the registration information of a task is specified using the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property.</span></span>

<span data-ttu-id="db7a6-146">Per lo sviluppo in C++, le informazioni di registrazione di un'attività vengono specificate utilizzando la [**Proprietà RegistrationInfo di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span><span class="sxs-lookup"><span data-stu-id="db7a6-146">For C++ development, the registration information of a task is specified using the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="db7a6-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db7a6-147">Requirements</span></span>



| <span data-ttu-id="db7a6-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="db7a6-148">Requirement</span></span> | <span data-ttu-id="db7a6-149">Valore</span><span class="sxs-lookup"><span data-stu-id="db7a6-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="db7a6-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db7a6-150">Minimum supported client</span></span><br/> | <span data-ttu-id="db7a6-151">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db7a6-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="db7a6-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db7a6-152">Minimum supported server</span></span><br/> | <span data-ttu-id="db7a6-153">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="db7a6-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db7a6-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db7a6-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db7a6-155">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="db7a6-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="db7a6-156">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="db7a6-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





