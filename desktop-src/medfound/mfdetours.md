---
description: Specifica il provider Microsoft Media Foundation Detours, che traccia Media Foundation chiamate API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: Elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cd03711c74c21a9a6ff33d2cc2560e4b6d6e0a3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119336"
---
# <a name="mfdetours-element"></a><span data-ttu-id="0bd5f-103">Elemento mfdetours</span><span class="sxs-lookup"><span data-stu-id="0bd5f-103">mfdetours element</span></span>

<span data-ttu-id="0bd5f-104">Specifica il provider Microsoft Media Foundation Detours, che traccia Media Foundation chiamate API.</span><span class="sxs-lookup"><span data-stu-id="0bd5f-104">Specifies the Microsoft Media Foundation Detours provider, which traces Media Foundation API calls.</span></span>

## <a name="usage"></a><span data-ttu-id="0bd5f-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0bd5f-105">Usage</span></span>

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a><span data-ttu-id="0bd5f-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="0bd5f-106">Attributes</span></span>



| <span data-ttu-id="0bd5f-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="0bd5f-107">Attribute</span></span>            | <span data-ttu-id="0bd5f-108">Type</span><span class="sxs-lookup"><span data-stu-id="0bd5f-108">Type</span></span>             | <span data-ttu-id="0bd5f-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="0bd5f-109">Required</span></span>       | <span data-ttu-id="0bd5f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bd5f-110">Description</span></span>                             |
|----------------------|------------------|----------------|-----------------------------------------|
| <span data-ttu-id="0bd5f-111">**level**</span><span class="sxs-lookup"><span data-stu-id="0bd5f-111">**level**</span></span><br/> | <span data-ttu-id="0bd5f-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="0bd5f-112">CDATA</span></span><br/> | <span data-ttu-id="0bd5f-113">Sì</span><span class="sxs-lookup"><span data-stu-id="0bd5f-113">Yes</span></span><br/> | <span data-ttu-id="0bd5f-114">Livello di traccia.</span><span class="sxs-lookup"><span data-stu-id="0bd5f-114">The trace level.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="0bd5f-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0bd5f-115">Child elements</span></span>



| <span data-ttu-id="0bd5f-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="0bd5f-116">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="0bd5f-117">**Parola chiave**</span><span class="sxs-lookup"><span data-stu-id="0bd5f-117">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="0bd5f-118">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0bd5f-118">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="0bd5f-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0bd5f-119">Parent elements</span></span>

| <span data-ttu-id="0bd5f-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="0bd5f-120">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="0bd5f-121">**Provider**</span><span class="sxs-lookup"><span data-stu-id="0bd5f-121">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="0bd5f-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0bd5f-122">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="0bd5f-123">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="0bd5f-123">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="0bd5f-124">No</span><span class="sxs-lookup"><span data-stu-id="0bd5f-124">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="0bd5f-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0bd5f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd5f-126">File di configurazione di MFTrace</span><span class="sxs-lookup"><span data-stu-id="0bd5f-126">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




