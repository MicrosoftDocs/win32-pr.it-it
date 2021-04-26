---
description: Genera implementazioni per le funzioni QueryInterface, AddRef e Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995148"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="9914a-103">Elemento IUnknownDefinitions</span><span class="sxs-lookup"><span data-stu-id="9914a-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="9914a-104">Genera implementazioni per le funzioni QueryInterface, AddRef e Release.</span><span class="sxs-lookup"><span data-stu-id="9914a-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="9914a-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="9914a-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="9914a-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="9914a-106">Attributes</span></span>



| <span data-ttu-id="9914a-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="9914a-107">Attribute</span></span>                  | <span data-ttu-id="9914a-108">Type</span><span class="sxs-lookup"><span data-stu-id="9914a-108">Type</span></span>                         | <span data-ttu-id="9914a-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="9914a-109">Required</span></span>       | <span data-ttu-id="9914a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9914a-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="9914a-111">**classe proxy**</span><span class="sxs-lookup"><span data-stu-id="9914a-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="9914a-112">stringa di \_ caratteri</span><span class="sxs-lookup"><span data-stu-id="9914a-112">character\_string</span></span><br/> | <span data-ttu-id="9914a-113">Sì</span><span class="sxs-lookup"><span data-stu-id="9914a-113">Yes</span></span><br/> | <span data-ttu-id="9914a-114">Nome della classe di implementazione.</span><span class="sxs-lookup"><span data-stu-id="9914a-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="9914a-115">**refCountVar**</span><span class="sxs-lookup"><span data-stu-id="9914a-115">**refCountVar**</span></span><br/> | <span data-ttu-id="9914a-116">stringa di \_ caratteri</span><span class="sxs-lookup"><span data-stu-id="9914a-116">character\_string</span></span><br/> | <span data-ttu-id="9914a-117">Sì</span><span class="sxs-lookup"><span data-stu-id="9914a-117">Yes</span></span><br/> | <span data-ttu-id="9914a-118">Nome della variabile del conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="9914a-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="9914a-119">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="9914a-119">Child elements</span></span>



| <span data-ttu-id="9914a-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="9914a-120">Element</span></span>                                   | <span data-ttu-id="9914a-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9914a-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="9914a-122">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="9914a-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="9914a-123">Nome dell'interfaccia che deve essere restituita da QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="9914a-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="9914a-124">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="9914a-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="9914a-125">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="9914a-125">Parent elements</span></span>



| <span data-ttu-id="9914a-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="9914a-126">Element</span></span>                         | <span data-ttu-id="9914a-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9914a-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9914a-128">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="9914a-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="9914a-129">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="9914a-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9914a-130">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9914a-130">Element information</span></span>



| <span data-ttu-id="9914a-131">Label</span><span class="sxs-lookup"><span data-stu-id="9914a-131">Label</span></span> | <span data-ttu-id="9914a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9914a-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="9914a-133">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9914a-133">Minimum supported system</span></span><br/> | <span data-ttu-id="9914a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9914a-134">Windows Vista</span></span> |
| <span data-ttu-id="9914a-135">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="9914a-135">Can be empty</span></span>                        | <span data-ttu-id="9914a-136">No</span><span class="sxs-lookup"><span data-stu-id="9914a-136">No</span></span>            |



 

 




