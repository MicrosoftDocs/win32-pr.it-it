---
description: Genera dichiarazioni di costanti C per i tipi di porta.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: elemento portTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19780d4a48c95cd47872b0428b368e6b7e99887
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996558"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="3409d-103">elemento portTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="3409d-103">portTypeDeclarations element</span></span>

<span data-ttu-id="3409d-104">Genera dichiarazioni di costanti C per i tipi di porta.</span><span class="sxs-lookup"><span data-stu-id="3409d-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="3409d-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="3409d-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="3409d-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="3409d-106">Attributes</span></span>

<span data-ttu-id="3409d-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="3409d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3409d-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3409d-108">Child elements</span></span>



| <span data-ttu-id="3409d-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="3409d-109">Element</span></span>                                   | <span data-ttu-id="3409d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3409d-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3409d-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="3409d-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="3409d-112">Specifica il nome da utilizzare per il tipo di porta nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="3409d-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="3409d-113">Per impostazione predefinita, il nome in codice viene generato dal nome completo del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="3409d-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="3409d-114">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="3409d-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="3409d-115">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="3409d-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="3409d-116">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="3409d-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="3409d-117">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="3409d-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="3409d-118">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3409d-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="3409d-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3409d-119">Parent elements</span></span>



| <span data-ttu-id="3409d-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="3409d-120">Element</span></span>                         | <span data-ttu-id="3409d-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3409d-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="3409d-122">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="3409d-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="3409d-123">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="3409d-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3409d-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="3409d-124">Remarks</span></span>

<span data-ttu-id="3409d-125">L'applicazione fa riferimento alle dichiarazioni del tipo di porta e gran parte del codice generato.</span><span class="sxs-lookup"><span data-stu-id="3409d-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="3409d-126">Questo elemento viene usato per generare file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="3409d-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="3409d-127">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3409d-127">Element information</span></span>



| <span data-ttu-id="3409d-128">Label</span><span class="sxs-lookup"><span data-stu-id="3409d-128">Label</span></span> | <span data-ttu-id="3409d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3409d-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="3409d-130">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3409d-130">Minimum supported system</span></span><br/> | <span data-ttu-id="3409d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3409d-131">Windows Vista</span></span> |
| <span data-ttu-id="3409d-132">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="3409d-132">Can be empty</span></span>                        | <span data-ttu-id="3409d-133">Sì</span><span class="sxs-lookup"><span data-stu-id="3409d-133">Yes</span></span>           |



 

 




