---
description: Specifica il percorso di download per una direttiva wsdl:import che non specifica in modo esplicito un percorso.
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: Elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29fcd65f9af02b8077ba828081ac9ed767d64e3
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380655"
---
# <a name="importhint-element"></a><span data-ttu-id="16842-103">Elemento importHint</span><span class="sxs-lookup"><span data-stu-id="16842-103">importHint element</span></span>

<span data-ttu-id="16842-104">Specifica il percorso di download per una \<wsdl:import> direttiva che non specifica in modo esplicito un percorso.</span><span class="sxs-lookup"><span data-stu-id="16842-104">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="16842-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="16842-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="16842-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="16842-106">Attributes</span></span>

<span data-ttu-id="16842-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="16842-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="16842-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="16842-108">Child elements</span></span>



| <span data-ttu-id="16842-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="16842-109">Element</span></span>                                   | <span data-ttu-id="16842-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16842-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16842-111">**Posizione**</span><span class="sxs-lookup"><span data-stu-id="16842-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="16842-112">Percorso del file da importare.</span><span class="sxs-lookup"><span data-stu-id="16842-112">The location of the file to import.</span></span> <span data-ttu-id="16842-113">Il percorso può essere un percorso relativo, un percorso assoluto o un URL HTTP.</span><span class="sxs-lookup"><span data-stu-id="16842-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="16842-114">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="16842-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="16842-115">Spazio dei nomi da importare.</span><span class="sxs-lookup"><span data-stu-id="16842-115">The namespace to import.</span></span> <span data-ttu-id="16842-116">Deve corrispondere allo spazio dei nomi specificato \<wsdl:import> nell'elemento .</span><span class="sxs-lookup"><span data-stu-id="16842-116">This should match the namespace specified in the \<wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="16842-117">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="16842-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="16842-118">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="16842-118">Parent elements</span></span>



| <span data-ttu-id="16842-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="16842-119">Element</span></span>                         | <span data-ttu-id="16842-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16842-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="16842-121">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="16842-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="16842-122">Specifica un file WSDL da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="16842-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="16842-123">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="16842-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="16842-124">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16842-124">Minimum supported system</span></span><br/> | <span data-ttu-id="16842-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16842-125">Windows Vista</span></span> |
| <span data-ttu-id="16842-126">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="16842-126">Can be empty</span></span>                        | <span data-ttu-id="16842-127">No</span><span class="sxs-lookup"><span data-stu-id="16842-127">No</span></span>            |



 

 




