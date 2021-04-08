---
title: Oggetto RegistrationInfo
description: Oggetto di scripting che fornisce le informazioni amministrative che possono essere utilizzate per descrivere l'attività.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- informazioni di registrazione Utilità di pianificazione, oggetto
- Utilità di pianificazione oggetto RegistrationInfo
- Oggetto RegistrationInfo Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048094"
---
# <a name="registrationinfo-object"></a><span data-ttu-id="4036d-106">Oggetto RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="4036d-106">RegistrationInfo object</span></span>

<span data-ttu-id="4036d-107">Oggetto di scripting che fornisce le informazioni amministrative che possono essere utilizzate per descrivere l'attività.</span><span class="sxs-lookup"><span data-stu-id="4036d-107">Scripting object that provides the administrative information that can be used to describe the task.</span></span> <span data-ttu-id="4036d-108">Queste informazioni includono dettagli quali una descrizione dell'attività, l'autore dell'attività, la data di registrazione dell'attività e il descrittore di sicurezza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4036d-108">This information includes details such as a description of the task, the author of the task, the date the task is registered, and the security descriptor of the task.</span></span>

## <a name="members"></a><span data-ttu-id="4036d-109">Membri</span><span class="sxs-lookup"><span data-stu-id="4036d-109">Members</span></span>

<span data-ttu-id="4036d-110">L'oggetto **RegistrationInfo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4036d-110">The **RegistrationInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="4036d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4036d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4036d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4036d-112">Properties</span></span>

<span data-ttu-id="4036d-113">L'oggetto **RegistrationInfo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4036d-113">The **RegistrationInfo** object has these properties.</span></span>



| <span data-ttu-id="4036d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4036d-114">Property</span></span>                                                                     | <span data-ttu-id="4036d-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="4036d-115">Access type</span></span>           | <span data-ttu-id="4036d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4036d-116">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4036d-117">**Autore**</span><span class="sxs-lookup"><span data-stu-id="4036d-117">**Author**</span></span>](registrationinfo-author.md)<br/>                         | <span data-ttu-id="4036d-118">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4036d-118">Read/write</span></span><br/> | <span data-ttu-id="4036d-119">Ottiene o imposta l'autore dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4036d-119">Gets or sets the author of the task.</span></span><br/>                                                                                            |
| [<span data-ttu-id="4036d-120">**Data**</span><span class="sxs-lookup"><span data-stu-id="4036d-120">**Date**</span></span>](registrationinfo-date.md)<br/>                             | <span data-ttu-id="4036d-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4036d-121">Read/write</span></span><br/> | <span data-ttu-id="4036d-122">Ottiene o imposta la data e l'ora di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4036d-122">Gets or sets the date and time when the task is registered.</span></span><br/>                                                                     |
| [<span data-ttu-id="4036d-123">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="4036d-123">**Description**</span></span>](registrationinfo-description.md)<br/>               | <span data-ttu-id="4036d-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4036d-124">Read/write</span></span><br/> | <span data-ttu-id="4036d-125">Ottiene o imposta la descrizione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4036d-125">Gets or sets the description of the task.</span></span><br/>                                                                                       |
| [<span data-ttu-id="4036d-126">**Documentazione**</span><span class="sxs-lookup"><span data-stu-id="4036d-126">**Documentation**</span></span>](registrationinfo-documentation.md)<br/>           | <span data-ttu-id="4036d-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4036d-127">Read/write</span></span><br/> | <span data-ttu-id="4036d-128">Ottiene o imposta qualsiasi documentazione aggiuntiva per l'attività.</span><span class="sxs-lookup"><span data-stu-id="4036d-128">Gets or sets any additional documentation for the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="4036d-129">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4036d-129">**SecurityDescriptor**</span></span>](registrationinfo-securitydescriptor.md)<br/> |                       | <span data-ttu-id="4036d-130">Ottiene o imposta il descrittore di sicurezza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4036d-130">Gets or sets the security descriptor of the task.</span></span><br/>                                                                               |
| [<span data-ttu-id="4036d-131">**Source (Sorgente)**</span><span class="sxs-lookup"><span data-stu-id="4036d-131">**Source**</span></span>](registrationinfo-source.md)<br/>                         | <span data-ttu-id="4036d-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4036d-132">Read/write</span></span><br/> | <span data-ttu-id="4036d-133">Ottiene o imposta il punto da cui ha origine l'attività.</span><span class="sxs-lookup"><span data-stu-id="4036d-133">Gets or sets where the task originated from.</span></span> <span data-ttu-id="4036d-134">Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.</span><span class="sxs-lookup"><span data-stu-id="4036d-134">For example, a task may originate from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="4036d-135">**URI**</span><span class="sxs-lookup"><span data-stu-id="4036d-135">**URI**</span></span>](registrationinfo-uri.md)<br/>                               | <span data-ttu-id="4036d-136">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4036d-136">Read/write</span></span><br/> | <span data-ttu-id="4036d-137">Ottiene o imposta l'URI dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4036d-137">Gets or sets the URI of the task.</span></span><br/>                                                                                               |
| [<span data-ttu-id="4036d-138">**Versione**</span><span class="sxs-lookup"><span data-stu-id="4036d-138">**Version**</span></span>](registrationinfo-version.md)<br/>                       | <span data-ttu-id="4036d-139">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4036d-139">Read/write</span></span><br/> | <span data-ttu-id="4036d-140">Ottiene o imposta il numero di versione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4036d-140">Gets or sets the version number of the task.</span></span><br/>                                                                                    |
| [<span data-ttu-id="4036d-141">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="4036d-141">**XmlText**</span></span>](registrationinfo-xmltext.md)<br/>                       | <span data-ttu-id="4036d-142">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4036d-142">Read/write</span></span><br/> | <span data-ttu-id="4036d-143">Ottiene o imposta una versione in formato XML delle informazioni di registrazione per l'attività.</span><span class="sxs-lookup"><span data-stu-id="4036d-143">Gets or sets an XML-formatted version of the registration information for the task.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="4036d-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="4036d-144">Remarks</span></span>

<span data-ttu-id="4036d-145">È possibile utilizzare le informazioni di registrazione per identificare un'attività tramite l'interfaccia utente di Utilità di pianificazione o come criterio di ricerca durante l'enumerazione delle attività registrate.</span><span class="sxs-lookup"><span data-stu-id="4036d-145">Registration information can be used to identify a task through the Task Scheduler UI, or as search criteria when enumerating over the registered tasks.</span></span>

<span data-ttu-id="4036d-146">Durante la lettura o la scrittura di codice XML per un'attività, le informazioni di registrazione per l'attività vengono specificate nell'elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4036d-146">When reading or writing XML for a task, registration information for the task is specified in the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="4036d-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="4036d-147">Examples</span></span>

<span data-ttu-id="4036d-148">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="4036d-148">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4036d-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4036d-149">Requirements</span></span>



| <span data-ttu-id="4036d-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="4036d-150">Requirement</span></span> | <span data-ttu-id="4036d-151">Valore</span><span class="sxs-lookup"><span data-stu-id="4036d-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4036d-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4036d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4036d-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4036d-153">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4036d-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4036d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4036d-155">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4036d-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4036d-156">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4036d-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="4036d-157"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4036d-157"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4036d-158">DLL</span><span class="sxs-lookup"><span data-stu-id="4036d-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4036d-159"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4036d-159"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





