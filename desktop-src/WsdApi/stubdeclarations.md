---
description: Genera dichiarazioni per le funzioni stub per le operazioni sul tipo di porta.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: Elemento stubDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1543883b4d41e7571cd4a4725e2aeab181530d30
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996408"
---
# <a name="stubdeclarations-element"></a><span data-ttu-id="80606-103">Elemento stubDeclarations</span><span class="sxs-lookup"><span data-stu-id="80606-103">stubDeclarations element</span></span>

<span data-ttu-id="80606-104">Genera dichiarazioni per le funzioni stub per le operazioni sul tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="80606-104">Generates declarations for stub functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="80606-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="80606-105">Usage</span></span>

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="80606-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="80606-106">Attributes</span></span>

<span data-ttu-id="80606-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="80606-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="80606-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="80606-108">Child elements</span></span>



| <span data-ttu-id="80606-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="80606-109">Element</span></span>                                   | <span data-ttu-id="80606-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80606-110">Description</span></span>                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80606-111">**Eventi**</span><span class="sxs-lookup"><span data-stu-id="80606-111">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="80606-112">Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="80606-112">Specifies whether related events are included in the generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="80606-113">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="80606-113">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="80606-114">Specifica un'operazione per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="80606-114">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                 |
| [<span data-ttu-id="80606-115">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="80606-115">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="80606-116">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="80606-116">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                |



### <a name="child-element-sequence"></a><span data-ttu-id="80606-117">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="80606-117">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a><span data-ttu-id="80606-118">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="80606-118">Parent elements</span></span>



| <span data-ttu-id="80606-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="80606-119">Element</span></span>                         | <span data-ttu-id="80606-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80606-120">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="80606-121">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="80606-121">**file**</span></span>](file.md)<br/> | <span data-ttu-id="80606-122">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="80606-122">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="80606-123">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="80606-123">Element information</span></span>



| <span data-ttu-id="80606-124">Label</span><span class="sxs-lookup"><span data-stu-id="80606-124">Label</span></span> | <span data-ttu-id="80606-125">Valore</span><span class="sxs-lookup"><span data-stu-id="80606-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="80606-126">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80606-126">Minimum supported system</span></span><br/> | <span data-ttu-id="80606-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80606-127">Windows Vista</span></span> |
| <span data-ttu-id="80606-128">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="80606-128">Can be empty</span></span>                        | <span data-ttu-id="80606-129">Sì</span><span class="sxs-lookup"><span data-stu-id="80606-129">Yes</span></span>           |



 

 




