---
description: Specifica il provider di detouring Microsoft Media Foundation, che traccia Media Foundation chiamate API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09d39d6f8a7c7ff1d88471e71c6fc58aa49bd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308409"
---
# <a name="mfdetours-element"></a><span data-ttu-id="b308a-103">elemento mfdetours</span><span class="sxs-lookup"><span data-stu-id="b308a-103">mfdetours element</span></span>

<span data-ttu-id="b308a-104">Specifica il provider di detouring Microsoft Media Foundation, che traccia Media Foundation chiamate API.</span><span class="sxs-lookup"><span data-stu-id="b308a-104">Specifies the Microsoft Media Foundation Detours provider, which traces Media Foundation API calls.</span></span>

## <a name="usage"></a><span data-ttu-id="b308a-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b308a-105">Usage</span></span>

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a><span data-ttu-id="b308a-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="b308a-106">Attributes</span></span>



| <span data-ttu-id="b308a-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="b308a-107">Attribute</span></span>            | <span data-ttu-id="b308a-108">Type</span><span class="sxs-lookup"><span data-stu-id="b308a-108">Type</span></span>             | <span data-ttu-id="b308a-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b308a-109">Required</span></span>       | <span data-ttu-id="b308a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b308a-110">Description</span></span>                             |
|----------------------|------------------|----------------|-----------------------------------------|
| <span data-ttu-id="b308a-111">**level**</span><span class="sxs-lookup"><span data-stu-id="b308a-111">**level**</span></span><br/> | <span data-ttu-id="b308a-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="b308a-112">CDATA</span></span><br/> | <span data-ttu-id="b308a-113">Sì</span><span class="sxs-lookup"><span data-stu-id="b308a-113">Yes</span></span><br/> | <span data-ttu-id="b308a-114">Livello di traccia.</span><span class="sxs-lookup"><span data-stu-id="b308a-114">The trace level.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="b308a-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b308a-115">Child elements</span></span>



| <span data-ttu-id="b308a-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="b308a-116">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="b308a-117">**parola chiave**</span><span class="sxs-lookup"><span data-stu-id="b308a-117">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="b308a-118">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b308a-118">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="b308a-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b308a-119">Parent elements</span></span>



| <span data-ttu-id="b308a-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="b308a-120">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="b308a-121">**provider**</span><span class="sxs-lookup"><span data-stu-id="b308a-121">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="b308a-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b308a-122">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="b308a-123">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="b308a-123">Can be empty</span></span> | <span data-ttu-id="b308a-124">No</span><span class="sxs-lookup"><span data-stu-id="b308a-124">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="b308a-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b308a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b308a-126">File di configurazione MFTrace</span><span class="sxs-lookup"><span data-stu-id="b308a-126">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




