---
description: Contiene un elenco di provider di traccia per MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: Elemento providers
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38a86bf3ca8ffa1ea9e3da20e0244e7abec8513
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118486"
---
# <a name="providers-element"></a><span data-ttu-id="61c97-103">Elemento providers</span><span class="sxs-lookup"><span data-stu-id="61c97-103">providers element</span></span>

<span data-ttu-id="61c97-104">Contiene un elenco di provider di traccia per [MFTrace.](mftrace.md)</span><span class="sxs-lookup"><span data-stu-id="61c97-104">Contains a list of trace providers for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="61c97-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="61c97-105">Usage</span></span>

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a><span data-ttu-id="61c97-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="61c97-106">Attributes</span></span>

<span data-ttu-id="61c97-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="61c97-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="61c97-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="61c97-108">Child elements</span></span>



| <span data-ttu-id="61c97-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="61c97-109">Element</span></span>                                   | <span data-ttu-id="61c97-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61c97-110">Description</span></span>                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61c97-111">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="61c97-111">**mfdetours**</span></span>](mfdetours.md)<br/> | <span data-ttu-id="61c97-112">Specifica il provider Media Foundation Detours, che traccia Media Foundation chiamate API.</span><span class="sxs-lookup"><span data-stu-id="61c97-112">Specifies the Media Foundation Detours provider, which traces Media Foundation API calls.</span></span><br/> <br/> |
| [<span data-ttu-id="61c97-113">**Provider**</span><span class="sxs-lookup"><span data-stu-id="61c97-113">**provider**</span></span>](provider.md)<br/>   | <span data-ttu-id="61c97-114">Specifica un provider di traccia (ETW o WPP).</span><span class="sxs-lookup"><span data-stu-id="61c97-114">Specifies a trace provider (ETW or WPP).</span></span><br/> <br/>                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="61c97-115">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="61c97-115">Child element sequence</span></span>

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a><span data-ttu-id="61c97-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="61c97-116">Parent elements</span></span>

<span data-ttu-id="61c97-117">Non ci sono elementi padre.</span><span class="sxs-lookup"><span data-stu-id="61c97-117">There are no parent elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="61c97-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="61c97-118">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="61c97-119">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="61c97-119">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="61c97-120">Sì</span><span class="sxs-lookup"><span data-stu-id="61c97-120">Yes</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="61c97-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="61c97-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61c97-122">File di configurazione di MFTrace</span><span class="sxs-lookup"><span data-stu-id="61c97-122">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




