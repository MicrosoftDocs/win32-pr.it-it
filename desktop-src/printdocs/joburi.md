---
description: Informazioni sull'elemento JobURI, che specifica un URI (Uniform Resource Identifier) per il documento.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc145ac9a393c09ecab762b84e9ac7d58870ddf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408614"
---
# <a name="joburi"></a><span data-ttu-id="9b60f-103">JobURI</span><span class="sxs-lookup"><span data-stu-id="9b60f-103">JobURI</span></span>

<span data-ttu-id="9b60f-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="9b60f-104">This topic is not current.</span></span> <span data-ttu-id="9b60f-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9b60f-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9b60f-106">Specifica un URI (Uniform Resource Identifier) per il documento.</span><span class="sxs-lookup"><span data-stu-id="9b60f-106">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="9b60f-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9b60f-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9b60f-108">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="9b60f-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9b60f-109">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9b60f-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9b60f-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9b60f-110">Element Information</span></span>



| <span data-ttu-id="9b60f-111">Nome</span><span class="sxs-lookup"><span data-stu-id="9b60f-111">Name</span></span> | <span data-ttu-id="9b60f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="9b60f-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="9b60f-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="9b60f-113">Element Type</span></span> <br/>   | <span data-ttu-id="9b60f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9b60f-114">Property</span></span><br/> |
| <span data-ttu-id="9b60f-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="9b60f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9b60f-116">Processo</span><span class="sxs-lookup"><span data-stu-id="9b60f-116">Job</span></span><br/>      |
| <span data-ttu-id="9b60f-117">Note</span><span class="sxs-lookup"><span data-stu-id="9b60f-117">Notes</span></span> <br/>          | <span data-ttu-id="9b60f-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="9b60f-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="9b60f-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="9b60f-119">Structural Content</span></span>

<span data-ttu-id="9b60f-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="9b60f-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="9b60f-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="9b60f-121">Structure Variables</span></span>

<span data-ttu-id="9b60f-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="9b60f-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9b60f-123">Nome</span><span class="sxs-lookup"><span data-stu-id="9b60f-123">Name</span></span>                       | <span data-ttu-id="9b60f-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9b60f-124">Data type</span></span>         | <span data-ttu-id="9b60f-125">Unità</span><span class="sxs-lookup"><span data-stu-id="9b60f-125">Unit</span></span> | <span data-ttu-id="9b60f-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="9b60f-126">Supported values</span></span> | <span data-ttu-id="9b60f-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="9b60f-127">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="9b60f-128">\_JobURIValue\_</span><span class="sxs-lookup"><span data-stu-id="9b60f-128">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="9b60f-129">string</span><span class="sxs-lookup"><span data-stu-id="9b60f-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9b60f-130">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9b60f-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="9b60f-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b60f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b60f-132">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="9b60f-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




