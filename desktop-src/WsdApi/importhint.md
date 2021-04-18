---
description: 'Specifica il percorso di download per un <WSDL: Import> direttiva che non specifica in modo esplicito una posizione.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce8da0a7fa45ed00489d405aaba8f1f6d7ab8fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310301"
---
# <a name="importhint-element"></a><span data-ttu-id="fa36f-103">elemento importHint</span><span class="sxs-lookup"><span data-stu-id="fa36f-103">importHint element</span></span>

<span data-ttu-id="fa36f-104">Specifica il percorso di download per un <WSDL: Import> direttiva che non specifica in modo esplicito una posizione.</span><span class="sxs-lookup"><span data-stu-id="fa36f-104">Specifies the download location for a <wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="fa36f-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="fa36f-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="fa36f-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="fa36f-106">Attributes</span></span>

<span data-ttu-id="fa36f-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="fa36f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fa36f-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fa36f-108">Child elements</span></span>



| <span data-ttu-id="fa36f-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="fa36f-109">Element</span></span>                                   | <span data-ttu-id="fa36f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa36f-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa36f-111">**percorso**</span><span class="sxs-lookup"><span data-stu-id="fa36f-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="fa36f-112">Percorso del file da importare.</span><span class="sxs-lookup"><span data-stu-id="fa36f-112">The location of the file to import.</span></span> <span data-ttu-id="fa36f-113">Il percorso può essere un percorso relativo, un percorso assoluto o un URL HTTP.</span><span class="sxs-lookup"><span data-stu-id="fa36f-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="fa36f-114">**nameSpace**</span><span class="sxs-lookup"><span data-stu-id="fa36f-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="fa36f-115">Spazio dei nomi da importare.</span><span class="sxs-lookup"><span data-stu-id="fa36f-115">The namespace to import.</span></span> <span data-ttu-id="fa36f-116">Deve corrispondere allo spazio dei nomi specificato nell'elemento <WSDL: Import>.</span><span class="sxs-lookup"><span data-stu-id="fa36f-116">This should match the namespace specified in the <wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="fa36f-117">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fa36f-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="fa36f-118">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="fa36f-118">Parent elements</span></span>



| <span data-ttu-id="fa36f-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="fa36f-119">Element</span></span>                         | <span data-ttu-id="fa36f-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa36f-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="fa36f-121">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="fa36f-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="fa36f-122">Specifica un file WSDL da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="fa36f-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="fa36f-123">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fa36f-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="fa36f-124">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa36f-124">Minimum supported system</span></span><br/> | <span data-ttu-id="fa36f-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa36f-125">Windows Vista</span></span> |
| <span data-ttu-id="fa36f-126">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="fa36f-126">Can be empty</span></span>                        | <span data-ttu-id="fa36f-127">No</span><span class="sxs-lookup"><span data-stu-id="fa36f-127">No</span></span>            |



 

 




