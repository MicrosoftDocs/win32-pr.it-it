---
description: Specifica il tipo di porta per cui deve essere generato il codice.
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: elemento portType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98f02fc5a18e330bb5617b52563adc79a039831
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996538"
---
# <a name="porttype-element"></a><span data-ttu-id="9f736-103">elemento portType</span><span class="sxs-lookup"><span data-stu-id="9f736-103">portType element</span></span>

<span data-ttu-id="9f736-104">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="9f736-104">Specifies the port type for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="9f736-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="9f736-105">Usage</span></span>

``` syntax
<portType/>
```

## <a name="attributes"></a><span data-ttu-id="9f736-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="9f736-106">Attributes</span></span>

<span data-ttu-id="9f736-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="9f736-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9f736-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="9f736-108">Child elements</span></span>

<span data-ttu-id="9f736-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="9f736-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9f736-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="9f736-110">Parent elements</span></span>



| <span data-ttu-id="9f736-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="9f736-111">Element</span></span>                                                                                                 | <span data-ttu-id="9f736-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f736-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f736-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="9f736-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="9f736-114">Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="9f736-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="9f736-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="9f736-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="9f736-116">Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="9f736-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="9f736-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="9f736-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="9f736-118">Genera definizioni di struttura C per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="9f736-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="9f736-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="9f736-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="9f736-120">Genera dichiarazioni di costanti C per le tabelle di XML Schema per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="9f736-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="9f736-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="9f736-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="9f736-122">Genera costanti C per le tabelle di XML Schema per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="9f736-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="9f736-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="9f736-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="9f736-124">Genera dichiarazioni di costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="9f736-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="9f736-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="9f736-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="9f736-126">Genera costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="9f736-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="9f736-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="9f736-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="9f736-128">Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="9f736-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="9f736-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="9f736-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="9f736-130">Genera dichiarazioni per le funzioni stub per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="9f736-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="9f736-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="9f736-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="9f736-132">Genera implementazioni per le funzioni stub per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="9f736-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="9f736-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="9f736-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="9f736-134">Genera dichiarazioni di implementazione per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="9f736-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="9f736-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="9f736-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="9f736-136">Genera dichiarazioni IDL per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="9f736-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="9f736-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="9f736-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="9f736-138">Genera implementazioni per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="9f736-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="9f736-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f736-139">Remarks</span></span>

<span data-ttu-id="9f736-140">Per impostazione predefinita, il codice viene generato per tutti i tipi di porta nei file di input WSDL.</span><span class="sxs-lookup"><span data-stu-id="9f736-140">By default, code is generated for all port types in WSDL input files.</span></span>

## <a name="element-information"></a><span data-ttu-id="9f736-141">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9f736-141">Element information</span></span>



| <span data-ttu-id="9f736-142">Label</span><span class="sxs-lookup"><span data-stu-id="9f736-142">Label</span></span> | <span data-ttu-id="9f736-143">Valore</span><span class="sxs-lookup"><span data-stu-id="9f736-143">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="9f736-144">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f736-144">Minimum supported system</span></span><br/> | <span data-ttu-id="9f736-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f736-145">Windows Vista</span></span> |
| <span data-ttu-id="9f736-146">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="9f736-146">Can be empty</span></span>                        | <span data-ttu-id="9f736-147">Sì</span><span class="sxs-lookup"><span data-stu-id="9f736-147">Yes</span></span>           |



 

 




