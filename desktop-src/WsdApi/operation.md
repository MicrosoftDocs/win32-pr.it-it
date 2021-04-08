---
description: Specifica un'operazione per la quale deve essere generato il codice.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: Operation-elemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdd8324553e046000f467c103afd6ac0464cbc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049806"
---
# <a name="operation-element"></a><span data-ttu-id="e7766-103">Operation-elemento</span><span class="sxs-lookup"><span data-stu-id="e7766-103">operation element</span></span>

<span data-ttu-id="e7766-104">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="e7766-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="e7766-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="e7766-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="e7766-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="e7766-106">Attributes</span></span>

<span data-ttu-id="e7766-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="e7766-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e7766-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e7766-108">Child elements</span></span>

<span data-ttu-id="e7766-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="e7766-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e7766-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="e7766-110">Parent elements</span></span>



| <span data-ttu-id="e7766-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="e7766-111">Element</span></span>                                                                                                 | <span data-ttu-id="e7766-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7766-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7766-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e7766-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="e7766-114">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e7766-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="e7766-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e7766-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="e7766-116">Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e7766-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="e7766-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="e7766-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="e7766-118">Genera definizioni della struttura C per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e7766-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="e7766-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e7766-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="e7766-120">Genera dichiarazioni di costanti C per XML Schema tabelle per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e7766-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="e7766-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="e7766-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="e7766-122">Genera costanti C per XML Schema tabelle per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e7766-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="e7766-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e7766-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="e7766-124">Genera dichiarazioni di costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="e7766-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="e7766-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="e7766-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="e7766-126">Genera costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="e7766-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="e7766-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="e7766-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="e7766-128">Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e7766-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="e7766-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e7766-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="e7766-130">Genera dichiarazioni per le funzioni stub per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e7766-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="e7766-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="e7766-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="e7766-132">Genera implementazioni per le funzioni stub per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e7766-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="e7766-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e7766-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="e7766-134">Genera dichiarazioni di implementazione per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e7766-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="e7766-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e7766-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="e7766-136">Genera dichiarazioni IDL per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e7766-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="e7766-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="e7766-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="e7766-138">Genera implementazioni per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e7766-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="e7766-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7766-139">Remarks</span></span>

<span data-ttu-id="e7766-140">È possibile specificare un numero qualsiasi di operazioni.</span><span class="sxs-lookup"><span data-stu-id="e7766-140">Any number of operations may be specified.</span></span> <span data-ttu-id="e7766-141">Se non viene specificata alcuna operazione, il codice viene generato per tutte le operazioni in tutti i tipi di porta pertinenti.</span><span class="sxs-lookup"><span data-stu-id="e7766-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="e7766-142">Se si usa l'elemento **Operation** , i metodi generati verranno limitati a quelli contenuti nell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e7766-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="e7766-143">Una stampante, ad esempio, supporta queste operazioni tra le altre:</span><span class="sxs-lookup"><span data-stu-id="e7766-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="e7766-144">**PrintJobByPost**</span><span class="sxs-lookup"><span data-stu-id="e7766-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="e7766-145">**PrintJobByReference**</span><span class="sxs-lookup"><span data-stu-id="e7766-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="e7766-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="e7766-146">**CancelJob**</span></span>
-   <span data-ttu-id="e7766-147">**GetJobElements**</span><span class="sxs-lookup"><span data-stu-id="e7766-147">**GetJobElements**</span></span>
-   <span data-ttu-id="e7766-148">**GetActiveJobs**</span><span class="sxs-lookup"><span data-stu-id="e7766-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="e7766-149">**GetJobHistory**</span><span class="sxs-lookup"><span data-stu-id="e7766-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="e7766-150">**SubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="e7766-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="e7766-151">**UnsubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="e7766-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="e7766-152">Tuttavia, per includere solo i metodi correlati alle operazioni **PrintJobByPost** e **GetJobElements** , lo script di generazione del codice utilizzerà gli elementi [**idlFunctionDeclarations**](idlfunctiondeclarations.md) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e7766-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="e7766-153">Vengono generate le dichiarazioni di funzione IDL per tutti i metodi associati alle due operazioni, ad esempio **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** e **EndGetJobElements**.</span><span class="sxs-lookup"><span data-stu-id="e7766-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="e7766-154">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e7766-154">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e7766-155">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7766-155">Minimum supported system</span></span><br/> | <span data-ttu-id="e7766-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7766-156">Windows Vista</span></span> |
| <span data-ttu-id="e7766-157">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="e7766-157">Can be empty</span></span>                        | <span data-ttu-id="e7766-158">Sì</span><span class="sxs-lookup"><span data-stu-id="e7766-158">Yes</span></span>           |



 

 




