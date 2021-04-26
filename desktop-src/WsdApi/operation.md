---
description: Specifica un'operazione per la quale deve essere generato il codice.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: elemento operation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0e4562241f5f437554d0af28dc8bca482512ea
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994317"
---
# <a name="operation-element"></a><span data-ttu-id="b207d-103">elemento operation</span><span class="sxs-lookup"><span data-stu-id="b207d-103">operation element</span></span>

<span data-ttu-id="b207d-104">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="b207d-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="b207d-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b207d-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="b207d-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="b207d-106">Attributes</span></span>

<span data-ttu-id="b207d-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="b207d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b207d-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b207d-108">Child elements</span></span>

<span data-ttu-id="b207d-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="b207d-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b207d-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b207d-110">Parent elements</span></span>



| <span data-ttu-id="b207d-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="b207d-111">Element</span></span>                                                                                                 | <span data-ttu-id="b207d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b207d-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b207d-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b207d-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="b207d-114">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="b207d-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="b207d-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b207d-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="b207d-116">Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="b207d-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="b207d-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b207d-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="b207d-118">Genera definizioni di struttura C per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="b207d-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="b207d-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b207d-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="b207d-120">Genera dichiarazioni di costanti C per le tabelle di XML Schema per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="b207d-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="b207d-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b207d-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="b207d-122">Genera costanti C per le tabelle di XML Schema per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="b207d-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="b207d-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b207d-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="b207d-124">Genera dichiarazioni di costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="b207d-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="b207d-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b207d-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="b207d-126">Genera costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="b207d-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="b207d-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="b207d-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="b207d-128">Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="b207d-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="b207d-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b207d-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="b207d-130">Genera dichiarazioni per le funzioni stub per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="b207d-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="b207d-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b207d-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="b207d-132">Genera implementazioni per le funzioni stub per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="b207d-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="b207d-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b207d-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="b207d-134">Genera dichiarazioni di implementazione per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="b207d-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="b207d-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b207d-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="b207d-136">Genera dichiarazioni IDL per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="b207d-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="b207d-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="b207d-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="b207d-138">Genera implementazioni per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="b207d-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="b207d-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="b207d-139">Remarks</span></span>

<span data-ttu-id="b207d-140">È possibile che venga specificato un numero qualsiasi di operazioni.</span><span class="sxs-lookup"><span data-stu-id="b207d-140">Any number of operations may be specified.</span></span> <span data-ttu-id="b207d-141">Se non viene specificata alcuna operazione, viene generato codice per tutte le operazioni in tutti i tipi di porta pertinenti.</span><span class="sxs-lookup"><span data-stu-id="b207d-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="b207d-142">**L'uso dell'elemento** operation limiterà i metodi generati a quelli contenuti nell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b207d-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="b207d-143">Ad esempio, una stampante supporta queste operazioni tra le altre:</span><span class="sxs-lookup"><span data-stu-id="b207d-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="b207d-144">**PrintJobByPost**</span><span class="sxs-lookup"><span data-stu-id="b207d-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="b207d-145">**PrintJobByReference**</span><span class="sxs-lookup"><span data-stu-id="b207d-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="b207d-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="b207d-146">**CancelJob**</span></span>
-   <span data-ttu-id="b207d-147">**GetJobElements**</span><span class="sxs-lookup"><span data-stu-id="b207d-147">**GetJobElements**</span></span>
-   <span data-ttu-id="b207d-148">**GetActiveJobs**</span><span class="sxs-lookup"><span data-stu-id="b207d-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="b207d-149">**GetJobHistory**</span><span class="sxs-lookup"><span data-stu-id="b207d-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="b207d-150">**SubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="b207d-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="b207d-151">**UnsubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="b207d-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="b207d-152">Tuttavia, per includere solo i metodi correlati alle operazioni **PrintJobByPost** e **GetJobElements,** lo script di generazione del codice userà gli elementi [**idlFunctionDeclarations**](idlfunctiondeclarations.md) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="b207d-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="b207d-153">Vengono generate dichiarazioni di funzione idl per tutti i metodi associati alle due operazioni , ad esempio **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** **e EndGetJobElements**.</span><span class="sxs-lookup"><span data-stu-id="b207d-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="b207d-154">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b207d-154">Element information</span></span>



| <span data-ttu-id="b207d-155">Label</span><span class="sxs-lookup"><span data-stu-id="b207d-155">Label</span></span> | <span data-ttu-id="b207d-156">Valore</span><span class="sxs-lookup"><span data-stu-id="b207d-156">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b207d-157">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b207d-157">Minimum supported system</span></span><br/> | <span data-ttu-id="b207d-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b207d-158">Windows Vista</span></span> |
| <span data-ttu-id="b207d-159">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="b207d-159">Can be empty</span></span>                        | <span data-ttu-id="b207d-160">Sì</span><span class="sxs-lookup"><span data-stu-id="b207d-160">Yes</span></span>           |



 

 




