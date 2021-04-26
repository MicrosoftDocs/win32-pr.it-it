---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c80611a4e7dbd10f4841fae098578f0a8fdc96
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993888"
---
# <a name="joburi"></a><span data-ttu-id="e134e-104">JobURI</span><span class="sxs-lookup"><span data-stu-id="e134e-104">JobURI</span></span>

<span data-ttu-id="e134e-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="e134e-105">This topic is not current.</span></span> <span data-ttu-id="e134e-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e134e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e134e-107">Specifica un URI (Uniform Resource Identifier) per il documento.</span><span class="sxs-lookup"><span data-stu-id="e134e-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="e134e-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e134e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e134e-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e134e-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e134e-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e134e-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e134e-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e134e-111">Element Information</span></span>



| <span data-ttu-id="e134e-112">Nome</span><span class="sxs-lookup"><span data-stu-id="e134e-112">Name</span></span> | <span data-ttu-id="e134e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e134e-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="e134e-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="e134e-114">Element Type</span></span> <br/>   | <span data-ttu-id="e134e-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e134e-115">Property</span></span><br/> |
| <span data-ttu-id="e134e-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="e134e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e134e-117">Processo</span><span class="sxs-lookup"><span data-stu-id="e134e-117">Job</span></span><br/>      |
| <span data-ttu-id="e134e-118">Note</span><span class="sxs-lookup"><span data-stu-id="e134e-118">Notes</span></span> <br/>          | <span data-ttu-id="e134e-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="e134e-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="e134e-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="e134e-120">Structural Content</span></span>

<span data-ttu-id="e134e-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="e134e-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="e134e-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="e134e-122">Structure Variables</span></span>

<span data-ttu-id="e134e-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="e134e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e134e-124">Nome</span><span class="sxs-lookup"><span data-stu-id="e134e-124">Name</span></span>                       | <span data-ttu-id="e134e-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e134e-125">Data type</span></span>         | <span data-ttu-id="e134e-126">Unità</span><span class="sxs-lookup"><span data-stu-id="e134e-126">Unit</span></span> | <span data-ttu-id="e134e-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="e134e-127">Supported values</span></span> | <span data-ttu-id="e134e-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="e134e-128">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="e134e-129">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="e134e-129">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="e134e-130">string</span><span class="sxs-lookup"><span data-stu-id="e134e-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e134e-131">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="e134e-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="e134e-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e134e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e134e-133">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e134e-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




