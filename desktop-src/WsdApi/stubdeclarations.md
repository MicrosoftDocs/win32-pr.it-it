---
description: Genera dichiarazioni per le funzioni stub per le operazioni del tipo di porta.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: elemento stubDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ceaa8871928031edff90db0491483cfd06bdcc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319802"
---
# <a name="stubdeclarations-element"></a><span data-ttu-id="0a1c5-103">elemento stubDeclarations</span><span class="sxs-lookup"><span data-stu-id="0a1c5-103">stubDeclarations element</span></span>

<span data-ttu-id="0a1c5-104">Genera dichiarazioni per le funzioni stub per le operazioni del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-104">Generates declarations for stub functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="0a1c5-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0a1c5-105">Usage</span></span>

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="0a1c5-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="0a1c5-106">Attributes</span></span>

<span data-ttu-id="0a1c5-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0a1c5-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0a1c5-108">Child elements</span></span>



| <span data-ttu-id="0a1c5-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="0a1c5-109">Element</span></span>                                   | <span data-ttu-id="0a1c5-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a1c5-110">Description</span></span>                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a1c5-111">**eventi**</span><span class="sxs-lookup"><span data-stu-id="0a1c5-111">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="0a1c5-112">Specifica se gli eventi correlati sono inclusi nelle funzioni generate.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-112">Specifies whether related events are included in the generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="0a1c5-113">**operazione**</span><span class="sxs-lookup"><span data-stu-id="0a1c5-113">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="0a1c5-114">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-114">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                 |
| [<span data-ttu-id="0a1c5-115">**portType**</span><span class="sxs-lookup"><span data-stu-id="0a1c5-115">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="0a1c5-116">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-116">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                |



### <a name="child-element-sequence"></a><span data-ttu-id="0a1c5-117">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0a1c5-117">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a><span data-ttu-id="0a1c5-118">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0a1c5-118">Parent elements</span></span>



| <span data-ttu-id="0a1c5-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="0a1c5-119">Element</span></span>                         | <span data-ttu-id="0a1c5-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a1c5-120">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="0a1c5-121">**file**</span><span class="sxs-lookup"><span data-stu-id="0a1c5-121">**file**</span></span>](file.md)<br/> | <span data-ttu-id="0a1c5-122">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-122">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="0a1c5-123">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0a1c5-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0a1c5-124">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a1c5-124">Minimum supported system</span></span><br/> | <span data-ttu-id="0a1c5-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a1c5-125">Windows Vista</span></span> |
| <span data-ttu-id="0a1c5-126">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="0a1c5-126">Can be empty</span></span>                        | <span data-ttu-id="0a1c5-127">Sì</span><span class="sxs-lookup"><span data-stu-id="0a1c5-127">Yes</span></span>           |



 

 




