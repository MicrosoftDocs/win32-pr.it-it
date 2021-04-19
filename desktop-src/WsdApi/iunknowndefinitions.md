---
description: Genera implementazioni per le funzioni QueryInterface, AddRef e release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310295"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="9353f-103">Elemento IUnknownDefinitions</span><span class="sxs-lookup"><span data-stu-id="9353f-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="9353f-104">Genera implementazioni per le funzioni QueryInterface, AddRef e release.</span><span class="sxs-lookup"><span data-stu-id="9353f-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="9353f-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="9353f-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="9353f-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="9353f-106">Attributes</span></span>



| <span data-ttu-id="9353f-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="9353f-107">Attribute</span></span>                  | <span data-ttu-id="9353f-108">Type</span><span class="sxs-lookup"><span data-stu-id="9353f-108">Type</span></span>                         | <span data-ttu-id="9353f-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="9353f-109">Required</span></span>       | <span data-ttu-id="9353f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9353f-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="9353f-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="9353f-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="9353f-112">stringa di caratteri \_</span><span class="sxs-lookup"><span data-stu-id="9353f-112">character\_string</span></span><br/> | <span data-ttu-id="9353f-113">Sì</span><span class="sxs-lookup"><span data-stu-id="9353f-113">Yes</span></span><br/> | <span data-ttu-id="9353f-114">Nome della classe di implementazione.</span><span class="sxs-lookup"><span data-stu-id="9353f-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="9353f-115">**refCountVar**</span><span class="sxs-lookup"><span data-stu-id="9353f-115">**refCountVar**</span></span><br/> | <span data-ttu-id="9353f-116">stringa di caratteri \_</span><span class="sxs-lookup"><span data-stu-id="9353f-116">character\_string</span></span><br/> | <span data-ttu-id="9353f-117">Sì</span><span class="sxs-lookup"><span data-stu-id="9353f-117">Yes</span></span><br/> | <span data-ttu-id="9353f-118">Nome della variabile di conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="9353f-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="9353f-119">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="9353f-119">Child elements</span></span>



| <span data-ttu-id="9353f-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="9353f-120">Element</span></span>                                   | <span data-ttu-id="9353f-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9353f-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="9353f-122">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="9353f-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="9353f-123">Nome dell'interfaccia che deve essere restituita da QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="9353f-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="9353f-124">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="9353f-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="9353f-125">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="9353f-125">Parent elements</span></span>



| <span data-ttu-id="9353f-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="9353f-126">Element</span></span>                         | <span data-ttu-id="9353f-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9353f-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9353f-128">**file**</span><span class="sxs-lookup"><span data-stu-id="9353f-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="9353f-129">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="9353f-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9353f-130">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9353f-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9353f-131">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9353f-131">Minimum supported system</span></span><br/> | <span data-ttu-id="9353f-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9353f-132">Windows Vista</span></span> |
| <span data-ttu-id="9353f-133">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="9353f-133">Can be empty</span></span>                        | <span data-ttu-id="9353f-134">No</span><span class="sxs-lookup"><span data-stu-id="9353f-134">No</span></span>            |



 

 




