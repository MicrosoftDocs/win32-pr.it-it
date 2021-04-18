---
description: Genera dichiarazioni di costanti C per i tipi di porta.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: elemento portTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e202f1451d93b519bd59ea51f591c37a92957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310280"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="8da74-103">elemento portTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="8da74-103">portTypeDeclarations element</span></span>

<span data-ttu-id="8da74-104">Genera dichiarazioni di costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="8da74-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="8da74-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="8da74-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="8da74-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="8da74-106">Attributes</span></span>

<span data-ttu-id="8da74-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="8da74-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8da74-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8da74-108">Child elements</span></span>



| <span data-ttu-id="8da74-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="8da74-109">Element</span></span>                                   | <span data-ttu-id="8da74-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8da74-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8da74-111">**codeName**</span><span class="sxs-lookup"><span data-stu-id="8da74-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="8da74-112">Specifica il nome da utilizzare per il tipo di porta nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="8da74-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="8da74-113">Per impostazione predefinita, il nome del codice viene generato dal nome completo del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="8da74-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="8da74-114">**operazione**</span><span class="sxs-lookup"><span data-stu-id="8da74-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="8da74-115">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="8da74-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="8da74-116">**portType**</span><span class="sxs-lookup"><span data-stu-id="8da74-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="8da74-117">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="8da74-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="8da74-118">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8da74-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="8da74-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="8da74-119">Parent elements</span></span>



| <span data-ttu-id="8da74-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="8da74-120">Element</span></span>                         | <span data-ttu-id="8da74-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8da74-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8da74-122">**file**</span><span class="sxs-lookup"><span data-stu-id="8da74-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="8da74-123">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="8da74-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8da74-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="8da74-124">Remarks</span></span>

<span data-ttu-id="8da74-125">L'applicazione fa riferimento alle dichiarazioni dei tipi di porta e gran parte del codice generato.</span><span class="sxs-lookup"><span data-stu-id="8da74-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="8da74-126">Questo elemento viene utilizzato per generare file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="8da74-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="8da74-127">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8da74-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="8da74-128">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8da74-128">Minimum supported system</span></span><br/> | <span data-ttu-id="8da74-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8da74-129">Windows Vista</span></span> |
| <span data-ttu-id="8da74-130">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="8da74-130">Can be empty</span></span>                        | <span data-ttu-id="8da74-131">Sì</span><span class="sxs-lookup"><span data-stu-id="8da74-131">Yes</span></span>           |



 

 




