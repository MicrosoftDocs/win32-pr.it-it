---
description: Genera costanti C per i tipi di porta.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: elemento portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60f55408df938ed95af14c69b2676473ac1bda71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231667"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="95603-103">elemento portTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="95603-103">portTypeDefinitions element</span></span>

<span data-ttu-id="95603-104">Genera costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="95603-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="95603-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="95603-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="95603-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="95603-106">Attributes</span></span>

<span data-ttu-id="95603-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="95603-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="95603-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="95603-108">Child elements</span></span>



| <span data-ttu-id="95603-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="95603-109">Element</span></span>                                                   | <span data-ttu-id="95603-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95603-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95603-111">**codeName**</span><span class="sxs-lookup"><span data-stu-id="95603-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="95603-112">Specifica il nome da utilizzare per il tipo di porta nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="95603-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="95603-113">Per impostazione predefinita, il nome del codice viene generato dal nome completo del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="95603-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="95603-114">**eventStubFunction**</span><span class="sxs-lookup"><span data-stu-id="95603-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="95603-115">Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni di notifica.</span><span class="sxs-lookup"><span data-stu-id="95603-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="95603-116">**operazione**</span><span class="sxs-lookup"><span data-stu-id="95603-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="95603-117">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="95603-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="95603-118">**portType**</span><span class="sxs-lookup"><span data-stu-id="95603-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="95603-119">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="95603-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="95603-120">**stubFunction**</span><span class="sxs-lookup"><span data-stu-id="95603-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="95603-121">Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni unidirezionali e bidirezionali.</span><span class="sxs-lookup"><span data-stu-id="95603-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="95603-122">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="95603-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="95603-123">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="95603-123">Parent elements</span></span>



| <span data-ttu-id="95603-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="95603-124">Element</span></span>                         | <span data-ttu-id="95603-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95603-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="95603-126">**file**</span><span class="sxs-lookup"><span data-stu-id="95603-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="95603-127">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="95603-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="95603-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="95603-128">Remarks</span></span>

<span data-ttu-id="95603-129">Questo elemento viene in genere usato nei file di origine C per fornire le costanti del tipo di porta dichiarate da [**portTypeDeclarations**](porttypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="95603-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="95603-130">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="95603-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="95603-131">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95603-131">Minimum supported system</span></span><br/> | <span data-ttu-id="95603-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95603-132">Windows Vista</span></span> |
| <span data-ttu-id="95603-133">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="95603-133">Can be empty</span></span>                        | <span data-ttu-id="95603-134">Sì</span><span class="sxs-lookup"><span data-stu-id="95603-134">Yes</span></span>           |



 

 




