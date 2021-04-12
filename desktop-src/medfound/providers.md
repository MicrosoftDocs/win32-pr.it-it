---
description: Contiene un elenco di provider di traccia per MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: Providers (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226510"
---
# <a name="providers-element"></a><span data-ttu-id="a8f09-103">Providers (elemento)</span><span class="sxs-lookup"><span data-stu-id="a8f09-103">providers element</span></span>

<span data-ttu-id="a8f09-104">Contiene un elenco di provider di traccia per [MFTrace](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="a8f09-104">Contains a list of trace providers for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="a8f09-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a8f09-105">Usage</span></span>

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a><span data-ttu-id="a8f09-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="a8f09-106">Attributes</span></span>

<span data-ttu-id="a8f09-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="a8f09-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a8f09-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a8f09-108">Child elements</span></span>



| <span data-ttu-id="a8f09-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8f09-109">Element</span></span>                                   | <span data-ttu-id="a8f09-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8f09-110">Description</span></span>                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8f09-111">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="a8f09-111">**mfdetours**</span></span>](mfdetours.md)<br/> | <span data-ttu-id="a8f09-112">Specifica il provider di detouring Media Foundation, che traccia Media Foundation chiamate API.</span><span class="sxs-lookup"><span data-stu-id="a8f09-112">Specifies the Media Foundation Detours provider, which traces Media Foundation API calls.</span></span><br/> <br/> |
| [<span data-ttu-id="a8f09-113">**provider**</span><span class="sxs-lookup"><span data-stu-id="a8f09-113">**provider**</span></span>](provider.md)<br/>   | <span data-ttu-id="a8f09-114">Specifica un provider di traccia (ETW o WPP).</span><span class="sxs-lookup"><span data-stu-id="a8f09-114">Specifies a trace provider (ETW or WPP).</span></span><br/> <br/>                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="a8f09-115">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a8f09-115">Child element sequence</span></span>

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a><span data-ttu-id="a8f09-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a8f09-116">Parent elements</span></span>

<span data-ttu-id="a8f09-117">Non ci sono elementi padre.</span><span class="sxs-lookup"><span data-stu-id="a8f09-117">There are no parent elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="a8f09-118">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a8f09-118">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="a8f09-119">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="a8f09-119">Can be empty</span></span> | <span data-ttu-id="a8f09-120">Sì</span><span class="sxs-lookup"><span data-stu-id="a8f09-120">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="a8f09-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8f09-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f09-122">File di configurazione MFTrace</span><span class="sxs-lookup"><span data-stu-id="a8f09-122">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




