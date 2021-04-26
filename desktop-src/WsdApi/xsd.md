---
description: Specifica un file XSD da elaborare per le informazioni sul contratto.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: Elemento xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851ce31230ff88ea2465040c33dc131e0902392c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994548"
---
# <a name="xsd-element"></a><span data-ttu-id="b7a0e-103">Elemento xsd</span><span class="sxs-lookup"><span data-stu-id="b7a0e-103">xsd element</span></span>

<span data-ttu-id="b7a0e-104">Specifica un file XSD da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="b7a0e-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="b7a0e-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b7a0e-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="b7a0e-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="b7a0e-106">Attributes</span></span>



| <span data-ttu-id="b7a0e-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="b7a0e-107">Attribute</span></span>           | <span data-ttu-id="b7a0e-108">Type</span><span class="sxs-lookup"><span data-stu-id="b7a0e-108">Type</span></span>                       | <span data-ttu-id="b7a0e-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b7a0e-109">Required</span></span>       | <span data-ttu-id="b7a0e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7a0e-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="b7a0e-111">**path**</span><span class="sxs-lookup"><span data-stu-id="b7a0e-111">**path**</span></span><br/> | <span data-ttu-id="b7a0e-112">stringa pathname</span><span class="sxs-lookup"><span data-stu-id="b7a0e-112">pathname string</span></span><br/> | <span data-ttu-id="b7a0e-113">Sì</span><span class="sxs-lookup"><span data-stu-id="b7a0e-113">Yes</span></span><br/> | <span data-ttu-id="b7a0e-114">File e percorso del file di input XSD.</span><span class="sxs-lookup"><span data-stu-id="b7a0e-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="b7a0e-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b7a0e-115">Child elements</span></span>



| <span data-ttu-id="b7a0e-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="b7a0e-116">Element</span></span>                               | <span data-ttu-id="b7a0e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7a0e-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="b7a0e-118">**typeUri**</span><span class="sxs-lookup"><span data-stu-id="b7a0e-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="b7a0e-119">Specifica un tipo da includere da un file XSD.</span><span class="sxs-lookup"><span data-stu-id="b7a0e-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="b7a0e-120">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b7a0e-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="b7a0e-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b7a0e-121">Parent elements</span></span>



| <span data-ttu-id="b7a0e-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="b7a0e-122">Element</span></span>                                     | <span data-ttu-id="b7a0e-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7a0e-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7a0e-124">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="b7a0e-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="b7a0e-125">Elemento radice di un file di script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="b7a0e-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b7a0e-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7a0e-126">Remarks</span></span>

<span data-ttu-id="b7a0e-127">La stringa del nome file deve includere anche informazioni complete sul percorso.</span><span class="sxs-lookup"><span data-stu-id="b7a0e-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="b7a0e-128">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b7a0e-128">Element information</span></span>



| <span data-ttu-id="b7a0e-129">Label</span><span class="sxs-lookup"><span data-stu-id="b7a0e-129">Label</span></span> | <span data-ttu-id="b7a0e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="b7a0e-130">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b7a0e-131">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7a0e-131">Minimum supported system</span></span><br/> | <span data-ttu-id="b7a0e-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7a0e-132">Windows Vista</span></span> |
| <span data-ttu-id="b7a0e-133">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="b7a0e-133">Can be empty</span></span>                        | <span data-ttu-id="b7a0e-134">Sì</span><span class="sxs-lookup"><span data-stu-id="b7a0e-134">Yes</span></span>           |



 

 




