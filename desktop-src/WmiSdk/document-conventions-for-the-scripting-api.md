---
description: Descrive le convenzioni dei documenti per la lettura degli argomenti dell'API di scripting WMI.
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: Convenzioni dei documenti per l'API di scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346741"
---
# <a name="document-conventions-for-the-scripting-api"></a><span data-ttu-id="c7b9d-103">Convenzioni dei documenti per l'API di scripting</span><span class="sxs-lookup"><span data-stu-id="c7b9d-103">Document Conventions for the Scripting API</span></span>

<span data-ttu-id="c7b9d-104">Per informazioni di riferimento sull' [API di scripting per WMI](scripting-api-for-wmi.md) vengono utilizzate le convenzioni dei documenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="c7b9d-104">The [Scripting API for WMI](scripting-api-for-wmi.md) reference uses the following document conventions:</span></span>

-   <span data-ttu-id="c7b9d-105">I tipi di parametro vengono definiti utilizzando un prefisso: b (booleano), Str (String), I (Integer), obj (oggetto di automazione), var (Variant).</span><span class="sxs-lookup"><span data-stu-id="c7b9d-105">Parameter types are defined using a prefix: b (Boolean), str (string), I (integer), obj (Automation object), var (Variant).</span></span>
-   <span data-ttu-id="c7b9d-106">I parametri facoltativi sono racchiusi tra parentesi quadre con i valori predefiniti indicati dall'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="c7b9d-106">Optional parameters are placed in square brackets with their default values shown by assignment.</span></span>
-   <span data-ttu-id="c7b9d-107">Nel caso dei parametri oggetto, i caratteri successivi al prefisso "obj" indicano il tipo di oggetto previsto.</span><span class="sxs-lookup"><span data-stu-id="c7b9d-107">In the case of object parameters, the characters after the "obj" prefix indicate the type of object expected.</span></span>



| <span data-ttu-id="c7b9d-108">Parametro dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="c7b9d-108">Object parameter</span></span>      | <span data-ttu-id="c7b9d-109">Tipo di oggetto</span><span class="sxs-lookup"><span data-stu-id="c7b9d-109">Object type</span></span>                                          |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="c7b9d-110">*WbemDatetime*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-110">*WbemDatetime*</span></span>        | [<span data-ttu-id="c7b9d-111">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-111">**SWbemDateTime**</span></span>](swbemdatetime.md)               |
| <span data-ttu-id="c7b9d-112">*WbemEventSource*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-112">*WbemEventSource*</span></span>     | [<span data-ttu-id="c7b9d-113">**SWbemEventSource**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-113">**SWbemEventSource**</span></span>](swbemeventsource.md)         |
| <span data-ttu-id="c7b9d-114">*WbemLocator*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-114">*WbemLocator*</span></span>         | [<span data-ttu-id="c7b9d-115">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-115">**SWbemLocator**</span></span>](swbemlocator.md)                 |
| <span data-ttu-id="c7b9d-116">*WbemMethod*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-116">*WbemMethod*</span></span>          | [<span data-ttu-id="c7b9d-117">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-117">**SWbemMethod**</span></span>](swbemmethod.md)                   |
| <span data-ttu-id="c7b9d-118">*WbemMethodSet*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-118">*WbemMethodSet*</span></span>       | [<span data-ttu-id="c7b9d-119">**SWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-119">**SWbemMethodSet**</span></span>](swbemmethodset.md)             |
| <span data-ttu-id="c7b9d-120">*WbemNamedValueSet*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-120">*WbemNamedValueSet*</span></span>   | [<span data-ttu-id="c7b9d-121">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-121">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)     |
| <span data-ttu-id="c7b9d-122">*WbemObject*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-122">*WbemObject*</span></span>          | [<span data-ttu-id="c7b9d-123">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-123">**SWbemObject**</span></span>](swbemobject.md)                   |
| <span data-ttu-id="c7b9d-124">*WbemObjectEx*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-124">*WbemObjectEx*</span></span>        | [<span data-ttu-id="c7b9d-125">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-125">**SWbemObjectEx**</span></span>](swbemobjectex.md)               |
| <span data-ttu-id="c7b9d-126">*WbemObjectPath*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-126">*WbemObjectPath*</span></span>      | [<span data-ttu-id="c7b9d-127">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-127">**SWbemObjectPath**</span></span>](swbemobjectpath.md)           |
| <span data-ttu-id="c7b9d-128">*WbemObjectSet*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-128">*WbemObjectSet*</span></span>       | [<span data-ttu-id="c7b9d-129">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-129">**SWbemObjectSet**</span></span>](swbemobjectset.md)             |
| <span data-ttu-id="c7b9d-130">*WbemPrivilege*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-130">*WbemPrivilege*</span></span>       | [<span data-ttu-id="c7b9d-131">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-131">**SWbemPrivilege**</span></span>](swbemprivilege.md)             |
| <span data-ttu-id="c7b9d-132">*WbemPrivilegeSet*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-132">*WbemPrivilegeSet*</span></span>    | [<span data-ttu-id="c7b9d-133">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-133">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)       |
| <span data-ttu-id="c7b9d-134">*WbemProperty*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-134">*WbemProperty*</span></span>        | [<span data-ttu-id="c7b9d-135">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-135">**SWbemProperty**</span></span>](swbemproperty.md)               |
| <span data-ttu-id="c7b9d-136">*WbemPropertySet*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-136">*WbemPropertySet*</span></span>     | [<span data-ttu-id="c7b9d-137">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-137">**SWbemPropertySet**</span></span>](swbempropertyset.md)         |
| <span data-ttu-id="c7b9d-138">*WbemQualifier*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-138">*WbemQualifier*</span></span>       | [<span data-ttu-id="c7b9d-139">**Oggetto SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-139">**SWbemQualifier**</span></span>](swbemqualifier.md)             |
| <span data-ttu-id="c7b9d-140">*WbemQualifierSet*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-140">*WbemQualifierSet*</span></span>    | [<span data-ttu-id="c7b9d-141">**Dell'SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-141">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)       |
| <span data-ttu-id="c7b9d-142">*WbemRefreshableItem*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-142">*WbemRefreshableItem*</span></span> | [<span data-ttu-id="c7b9d-143">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-143">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md) |
| <span data-ttu-id="c7b9d-144">*WbemRefresher*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-144">*WbemRefresher*</span></span>       | [<span data-ttu-id="c7b9d-145">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-145">**SWbemRefresher**</span></span>](swbemrefresher.md)             |
| <span data-ttu-id="c7b9d-146">*WbemServices*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-146">*WbemServices*</span></span>        | [<span data-ttu-id="c7b9d-147">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-147">**SWbemServices**</span></span>](swbemservices.md)               |
| <span data-ttu-id="c7b9d-148">*WbemServicesEx*</span><span class="sxs-lookup"><span data-stu-id="c7b9d-148">*WbemServicesEx*</span></span>      | [<span data-ttu-id="c7b9d-149">**SWbemServicesEx**</span><span class="sxs-lookup"><span data-stu-id="c7b9d-149">**SWbemServicesEx**</span></span>](swbemservicesex.md)           |



 

<span data-ttu-id="c7b9d-150">Il codice seguente, ad esempio, Mostra come denominare le variabili per diversi tipi di oggetti:</span><span class="sxs-lookup"><span data-stu-id="c7b9d-150">For example, the following code shows how to name variables for different types of objects:</span></span>


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



