---
description: Specifica un file XSD da elaborare per le informazioni sul contratto.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: XSD (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103881981"
---
# <a name="xsd-element"></a><span data-ttu-id="c9a52-103">XSD (elemento)</span><span class="sxs-lookup"><span data-stu-id="c9a52-103">xsd element</span></span>

<span data-ttu-id="c9a52-104">Specifica un file XSD da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="c9a52-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="c9a52-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="c9a52-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="c9a52-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="c9a52-106">Attributes</span></span>



| <span data-ttu-id="c9a52-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="c9a52-107">Attribute</span></span>           | <span data-ttu-id="c9a52-108">Type</span><span class="sxs-lookup"><span data-stu-id="c9a52-108">Type</span></span>                       | <span data-ttu-id="c9a52-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="c9a52-109">Required</span></span>       | <span data-ttu-id="c9a52-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9a52-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="c9a52-111">**path**</span><span class="sxs-lookup"><span data-stu-id="c9a52-111">**path**</span></span><br/> | <span data-ttu-id="c9a52-112">stringa PathName</span><span class="sxs-lookup"><span data-stu-id="c9a52-112">pathname string</span></span><br/> | <span data-ttu-id="c9a52-113">Sì</span><span class="sxs-lookup"><span data-stu-id="c9a52-113">Yes</span></span><br/> | <span data-ttu-id="c9a52-114">File e percorso del file di input XSD.</span><span class="sxs-lookup"><span data-stu-id="c9a52-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="c9a52-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c9a52-115">Child elements</span></span>



| <span data-ttu-id="c9a52-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9a52-116">Element</span></span>                               | <span data-ttu-id="c9a52-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9a52-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="c9a52-118">**typeUri**</span><span class="sxs-lookup"><span data-stu-id="c9a52-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="c9a52-119">Specifica un tipo da includere da un file XSD.</span><span class="sxs-lookup"><span data-stu-id="c9a52-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="c9a52-120">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c9a52-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="c9a52-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="c9a52-121">Parent elements</span></span>



| <span data-ttu-id="c9a52-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9a52-122">Element</span></span>                                     | <span data-ttu-id="c9a52-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9a52-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9a52-124">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="c9a52-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="c9a52-125">Elemento radice di un file di script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="c9a52-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c9a52-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9a52-126">Remarks</span></span>

<span data-ttu-id="c9a52-127">La stringa del nome file deve includere anche informazioni complete sul percorso.</span><span class="sxs-lookup"><span data-stu-id="c9a52-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="c9a52-128">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c9a52-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="c9a52-129">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9a52-129">Minimum supported system</span></span><br/> | <span data-ttu-id="c9a52-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9a52-130">Windows Vista</span></span> |
| <span data-ttu-id="c9a52-131">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="c9a52-131">Can be empty</span></span>                        | <span data-ttu-id="c9a52-132">Sì</span><span class="sxs-lookup"><span data-stu-id="c9a52-132">Yes</span></span>           |



 

 




