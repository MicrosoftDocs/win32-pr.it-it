---
description: Specifica un tipo da includere da un file XSD.
ms.assetid: dd3894a8-1848-4ae0-ba6c-42ac4fe36ff3
title: elemento typeUri
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9ef0a2482354fcfd962a7e41a7c2b94b54f5cb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998688"
---
# <a name="typeuri-element"></a><span data-ttu-id="3abbc-103">Elemento typeUri</span><span class="sxs-lookup"><span data-stu-id="3abbc-103">typeUri element</span></span>

<span data-ttu-id="3abbc-104">Specifica un tipo da includere da un file XSD.</span><span class="sxs-lookup"><span data-stu-id="3abbc-104">Specifies a type to include from an XSD file.</span></span>

## <a name="usage"></a><span data-ttu-id="3abbc-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="3abbc-105">Usage</span></span>

``` syntax
<typeUri
  type = "character_string"
  uri = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="3abbc-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="3abbc-106">Attributes</span></span>



| <span data-ttu-id="3abbc-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="3abbc-107">Attribute</span></span>           | <span data-ttu-id="3abbc-108">Type</span><span class="sxs-lookup"><span data-stu-id="3abbc-108">Type</span></span>                         | <span data-ttu-id="3abbc-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="3abbc-109">Required</span></span>       | <span data-ttu-id="3abbc-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3abbc-110">Description</span></span>                                                            |
|---------------------|------------------------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="3abbc-111">**type**</span><span class="sxs-lookup"><span data-stu-id="3abbc-111">**type**</span></span><br/> | <span data-ttu-id="3abbc-112">stringa di \_ caratteri</span><span class="sxs-lookup"><span data-stu-id="3abbc-112">character\_string</span></span><br/> | <span data-ttu-id="3abbc-113">Sì</span><span class="sxs-lookup"><span data-stu-id="3abbc-113">Yes</span></span><br/> | <span data-ttu-id="3abbc-114">Nome del tipo.</span><span class="sxs-lookup"><span data-stu-id="3abbc-114">The name of the type.</span></span><br/> <br/>                           |
| <span data-ttu-id="3abbc-115">**Uri**</span><span class="sxs-lookup"><span data-stu-id="3abbc-115">**uri**</span></span><br/>  | <span data-ttu-id="3abbc-116">stringa di \_ caratteri</span><span class="sxs-lookup"><span data-stu-id="3abbc-116">character\_string</span></span><br/> | <span data-ttu-id="3abbc-117">Sì</span><span class="sxs-lookup"><span data-stu-id="3abbc-117">Yes</span></span><br/> | <span data-ttu-id="3abbc-118">Spazio dei nomi del tipo.</span><span class="sxs-lookup"><span data-stu-id="3abbc-118">The namespace of the type.</span></span> <span data-ttu-id="3abbc-119">Deve essere un URI valido.</span><span class="sxs-lookup"><span data-stu-id="3abbc-119">Must be a valid URI.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="3abbc-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3abbc-120">Child elements</span></span>

<span data-ttu-id="3abbc-121">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="3abbc-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="3abbc-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3abbc-122">Parent elements</span></span>



| <span data-ttu-id="3abbc-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="3abbc-123">Element</span></span>                       | <span data-ttu-id="3abbc-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3abbc-124">Description</span></span>                                                                       |
|-------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="3abbc-125">**Xsd**</span><span class="sxs-lookup"><span data-stu-id="3abbc-125">**xsd**</span></span>](xsd.md)<br/> | <span data-ttu-id="3abbc-126">Specifica un file XSD da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="3abbc-126">Specifies an XSD file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="3abbc-127">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3abbc-127">Element information</span></span>



| <span data-ttu-id="3abbc-128">Label</span><span class="sxs-lookup"><span data-stu-id="3abbc-128">Label</span></span> | <span data-ttu-id="3abbc-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3abbc-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="3abbc-130">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3abbc-130">Minimum supported system</span></span><br/> | <span data-ttu-id="3abbc-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3abbc-131">Windows Vista</span></span> |
| <span data-ttu-id="3abbc-132">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="3abbc-132">Can be empty</span></span>                        | <span data-ttu-id="3abbc-133">Sì</span><span class="sxs-lookup"><span data-stu-id="3abbc-133">Yes</span></span>           |



 

 




