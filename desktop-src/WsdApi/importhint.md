---
description: Specifica il percorso di download per una direttiva wsdl:import che non specifica in modo esplicito un percorso.
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: Elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c874879ee0a608c100f32a0520a85efe76080cc2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998758"
---
# <a name="importhint-element"></a><span data-ttu-id="44fd7-103">Elemento importHint</span><span class="sxs-lookup"><span data-stu-id="44fd7-103">importHint element</span></span>

<span data-ttu-id="44fd7-104">Specifica il percorso di download per una \<wsdl:import> direttiva che non specifica in modo esplicito un percorso.</span><span class="sxs-lookup"><span data-stu-id="44fd7-104">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="44fd7-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="44fd7-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="44fd7-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="44fd7-106">Attributes</span></span>

<span data-ttu-id="44fd7-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="44fd7-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="44fd7-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="44fd7-108">Child elements</span></span>



| <span data-ttu-id="44fd7-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="44fd7-109">Element</span></span>                                   | <span data-ttu-id="44fd7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44fd7-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44fd7-111">**Posizione**</span><span class="sxs-lookup"><span data-stu-id="44fd7-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="44fd7-112">Percorso del file da importare.</span><span class="sxs-lookup"><span data-stu-id="44fd7-112">The location of the file to import.</span></span> <span data-ttu-id="44fd7-113">Il percorso può essere un percorso relativo, un percorso assoluto o un URL HTTP.</span><span class="sxs-lookup"><span data-stu-id="44fd7-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="44fd7-114">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="44fd7-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="44fd7-115">Spazio dei nomi da importare.</span><span class="sxs-lookup"><span data-stu-id="44fd7-115">The namespace to import.</span></span> <span data-ttu-id="44fd7-116">Deve corrispondere allo spazio dei nomi specificato \<wsdl:import> nell'elemento .</span><span class="sxs-lookup"><span data-stu-id="44fd7-116">This should match the namespace specified in the \<wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="44fd7-117">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="44fd7-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="44fd7-118">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="44fd7-118">Parent elements</span></span>



| <span data-ttu-id="44fd7-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="44fd7-119">Element</span></span>                         | <span data-ttu-id="44fd7-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44fd7-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="44fd7-121">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="44fd7-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="44fd7-122">Specifica un file WSDL da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="44fd7-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="44fd7-123">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="44fd7-123">Element information</span></span>



| <span data-ttu-id="44fd7-124">Label</span><span class="sxs-lookup"><span data-stu-id="44fd7-124">Label</span></span> | <span data-ttu-id="44fd7-125">Valore</span><span class="sxs-lookup"><span data-stu-id="44fd7-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="44fd7-126">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44fd7-126">Minimum supported system</span></span><br/> | <span data-ttu-id="44fd7-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44fd7-127">Windows Vista</span></span> |
| <span data-ttu-id="44fd7-128">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="44fd7-128">Can be empty</span></span>                        | <span data-ttu-id="44fd7-129">No</span><span class="sxs-lookup"><span data-stu-id="44fd7-129">No</span></span>            |



 

 




