---
description: Specifica il tipo di porta per il quale deve essere generato il codice.
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: portType (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a466ccdcfda133a2a314609e9698cd37c6bf31c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312675"
---
# <a name="porttype-element"></a><span data-ttu-id="e3a24-103">portType (elemento)</span><span class="sxs-lookup"><span data-stu-id="e3a24-103">portType element</span></span>

<span data-ttu-id="e3a24-104">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="e3a24-104">Specifies the port type for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="e3a24-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="e3a24-105">Usage</span></span>

``` syntax
<portType/>
```

## <a name="attributes"></a><span data-ttu-id="e3a24-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="e3a24-106">Attributes</span></span>

<span data-ttu-id="e3a24-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="e3a24-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e3a24-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e3a24-108">Child elements</span></span>

<span data-ttu-id="e3a24-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="e3a24-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e3a24-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="e3a24-110">Parent elements</span></span>



| <span data-ttu-id="e3a24-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="e3a24-111">Element</span></span>                                                                                                 | <span data-ttu-id="e3a24-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3a24-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3a24-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e3a24-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="e3a24-114">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e3a24-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="e3a24-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e3a24-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="e3a24-116">Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e3a24-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="e3a24-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="e3a24-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="e3a24-118">Genera definizioni della struttura C per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e3a24-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="e3a24-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e3a24-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="e3a24-120">Genera dichiarazioni di costanti C per XML Schema tabelle per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e3a24-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="e3a24-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="e3a24-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="e3a24-122">Genera costanti C per XML Schema tabelle per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e3a24-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="e3a24-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e3a24-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="e3a24-124">Genera dichiarazioni di costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="e3a24-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="e3a24-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="e3a24-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="e3a24-126">Genera costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="e3a24-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="e3a24-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="e3a24-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="e3a24-128">Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e3a24-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="e3a24-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e3a24-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="e3a24-130">Genera dichiarazioni per le funzioni stub per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e3a24-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="e3a24-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="e3a24-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="e3a24-132">Genera implementazioni per le funzioni stub per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e3a24-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="e3a24-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e3a24-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="e3a24-134">Genera dichiarazioni di implementazione per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e3a24-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="e3a24-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="e3a24-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="e3a24-136">Genera dichiarazioni IDL per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e3a24-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="e3a24-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="e3a24-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="e3a24-138">Genera implementazioni per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="e3a24-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="e3a24-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3a24-139">Remarks</span></span>

<span data-ttu-id="e3a24-140">Per impostazione predefinita, il codice viene generato per tutti i tipi di porta nei file di input WSDL.</span><span class="sxs-lookup"><span data-stu-id="e3a24-140">By default, code is generated for all port types in WSDL input files.</span></span>

## <a name="element-information"></a><span data-ttu-id="e3a24-141">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e3a24-141">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e3a24-142">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3a24-142">Minimum supported system</span></span><br/> | <span data-ttu-id="e3a24-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3a24-143">Windows Vista</span></span> |
| <span data-ttu-id="e3a24-144">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="e3a24-144">Can be empty</span></span>                        | <span data-ttu-id="e3a24-145">Sì</span><span class="sxs-lookup"><span data-stu-id="e3a24-145">Yes</span></span>           |



 

 




