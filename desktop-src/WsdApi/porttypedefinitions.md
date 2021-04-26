---
description: Genera costanti C per i tipi di porta.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: elemento portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff073eb7b0f9cbc4b0b6df87c8f9fc84d4f62882
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996548"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="32f0a-103">elemento portTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="32f0a-103">portTypeDefinitions element</span></span>

<span data-ttu-id="32f0a-104">Genera costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="32f0a-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="32f0a-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="32f0a-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="32f0a-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="32f0a-106">Attributes</span></span>

<span data-ttu-id="32f0a-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="32f0a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="32f0a-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="32f0a-108">Child elements</span></span>



| <span data-ttu-id="32f0a-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="32f0a-109">Element</span></span>                                                   | <span data-ttu-id="32f0a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32f0a-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32f0a-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="32f0a-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="32f0a-112">Specifica il nome da utilizzare per il tipo di porta nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="32f0a-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="32f0a-113">Per impostazione predefinita, il nome in codice viene generato dal nome completo del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="32f0a-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="32f0a-114">**eventStubFunction**</span><span class="sxs-lookup"><span data-stu-id="32f0a-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="32f0a-115">Specifica se i riferimenti alle funzioni stub devono essere inclusi nelle strutture delle operazioni nelle definizioni dei tipi di porta per le operazioni di notifica.</span><span class="sxs-lookup"><span data-stu-id="32f0a-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="32f0a-116">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="32f0a-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="32f0a-117">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="32f0a-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="32f0a-118">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="32f0a-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="32f0a-119">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="32f0a-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="32f0a-120">**StubFunction**</span><span class="sxs-lookup"><span data-stu-id="32f0a-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="32f0a-121">Specifica se i riferimenti alle funzioni stub devono essere inclusi nelle strutture delle operazioni nelle definizioni dei tipi di porta per le operazioni unidirezionale e bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="32f0a-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="32f0a-122">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="32f0a-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="32f0a-123">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="32f0a-123">Parent elements</span></span>



| <span data-ttu-id="32f0a-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="32f0a-124">Element</span></span>                         | <span data-ttu-id="32f0a-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32f0a-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="32f0a-126">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="32f0a-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="32f0a-127">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="32f0a-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="32f0a-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="32f0a-128">Remarks</span></span>

<span data-ttu-id="32f0a-129">Questo elemento viene in genere usato nei file di origine C per fornire le costanti del tipo di porta dichiarate da [**portTypeDeclarations.**](porttypedeclarations.md)</span><span class="sxs-lookup"><span data-stu-id="32f0a-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="32f0a-130">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="32f0a-130">Element information</span></span>



| <span data-ttu-id="32f0a-131">Label</span><span class="sxs-lookup"><span data-stu-id="32f0a-131">Label</span></span> | <span data-ttu-id="32f0a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="32f0a-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="32f0a-133">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32f0a-133">Minimum supported system</span></span><br/> | <span data-ttu-id="32f0a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32f0a-134">Windows Vista</span></span> |
| <span data-ttu-id="32f0a-135">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="32f0a-135">Can be empty</span></span>                        | <span data-ttu-id="32f0a-136">Sì</span><span class="sxs-lookup"><span data-stu-id="32f0a-136">Yes</span></span>           |



 

 




