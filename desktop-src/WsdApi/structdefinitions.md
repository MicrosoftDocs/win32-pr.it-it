---
description: Genera definizioni della struttura C per i tipi noti.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: Elemento structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f680db18b06253362f932cc7d34d5b85f7c1b5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996458"
---
# <a name="structdefinitions-element"></a><span data-ttu-id="3edd6-103">Elemento structDefinitions</span><span class="sxs-lookup"><span data-stu-id="3edd6-103">structDefinitions element</span></span>

<span data-ttu-id="3edd6-104">Genera definizioni della struttura C per i tipi noti.</span><span class="sxs-lookup"><span data-stu-id="3edd6-104">Generates C structure definitions for known types.</span></span>

## <a name="usage"></a><span data-ttu-id="3edd6-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="3edd6-105">Usage</span></span>

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a><span data-ttu-id="3edd6-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="3edd6-106">Attributes</span></span>

<span data-ttu-id="3edd6-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="3edd6-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3edd6-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3edd6-108">Child elements</span></span>

<span data-ttu-id="3edd6-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="3edd6-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="3edd6-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3edd6-110">Parent elements</span></span>



| <span data-ttu-id="3edd6-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="3edd6-111">Element</span></span>                         | <span data-ttu-id="3edd6-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3edd6-112">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="3edd6-113">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="3edd6-113">**file**</span></span>](file.md)<br/> | <span data-ttu-id="3edd6-114">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="3edd6-114">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3edd6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3edd6-115">Remarks</span></span>

<span data-ttu-id="3edd6-116">Gran parte del codice generato e del codice dell'applicazione fa riferimento alle strutture per i tipi noti.</span><span class="sxs-lookup"><span data-stu-id="3edd6-116">Structures for known types are referenced by much of the generated code and by application code.</span></span> <span data-ttu-id="3edd6-117">Questo elemento viene usato per generare file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="3edd6-117">This element is used to generate include files.</span></span> <span data-ttu-id="3edd6-118">Questo elemento deve verificarsi dopo un [**elemento structDeclarations**](structdeclarations.md) in modo che i riferimenti tra strutture siano gestiti correttamente.</span><span class="sxs-lookup"><span data-stu-id="3edd6-118">This element should occur after a [**structDeclarations**](structdeclarations.md) element so that references between structures are handled properly.</span></span>

## <a name="element-information"></a><span data-ttu-id="3edd6-119">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3edd6-119">Element information</span></span>



| <span data-ttu-id="3edd6-120">Label</span><span class="sxs-lookup"><span data-stu-id="3edd6-120">Label</span></span> | <span data-ttu-id="3edd6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3edd6-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="3edd6-122">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3edd6-122">Minimum supported system</span></span><br/> | <span data-ttu-id="3edd6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3edd6-123">Windows Vista</span></span> |
| <span data-ttu-id="3edd6-124">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="3edd6-124">Can be empty</span></span>                        | <span data-ttu-id="3edd6-125">Sì</span><span class="sxs-lookup"><span data-stu-id="3edd6-125">Yes</span></span>           |



 

 




