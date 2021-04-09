---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9964df145e75fe2b30d670d5575928485e00c5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103969011"
---
# <a name="documenturi"></a><span data-ttu-id="eec70-104">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="eec70-104">DocumentURI</span></span>

<span data-ttu-id="eec70-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="eec70-105">This topic is not current.</span></span> <span data-ttu-id="eec70-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eec70-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eec70-107">Specifica un URI (Uniform Resource Identifier) per il documento.</span><span class="sxs-lookup"><span data-stu-id="eec70-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="eec70-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="eec70-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eec70-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="eec70-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="eec70-110">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="eec70-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="eec70-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="eec70-111">Element Information</span></span>



| <span data-ttu-id="eec70-112">Nome</span><span class="sxs-lookup"><span data-stu-id="eec70-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="eec70-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="eec70-113">Element Type</span></span> <br/>   | <span data-ttu-id="eec70-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eec70-114">Property</span></span><br/> |
| <span data-ttu-id="eec70-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="eec70-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eec70-116">Documento</span><span class="sxs-lookup"><span data-stu-id="eec70-116">Document</span></span><br/> |
| <span data-ttu-id="eec70-117">Note</span><span class="sxs-lookup"><span data-stu-id="eec70-117">Notes</span></span> <br/>          | <span data-ttu-id="eec70-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="eec70-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="eec70-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="eec70-119">Structural Content</span></span>

<span data-ttu-id="eec70-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="eec70-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="eec70-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="eec70-121">Structure Variables</span></span>

<span data-ttu-id="eec70-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="eec70-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eec70-123">Nome</span><span class="sxs-lookup"><span data-stu-id="eec70-123">Name</span></span>                            | <span data-ttu-id="eec70-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="eec70-124">Data type</span></span>         | <span data-ttu-id="eec70-125">Unità</span><span class="sxs-lookup"><span data-stu-id="eec70-125">Unit</span></span> | <span data-ttu-id="eec70-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="eec70-126">Supported values</span></span> | <span data-ttu-id="eec70-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="eec70-127">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="eec70-128">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="eec70-128">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="eec70-129">string</span><span class="sxs-lookup"><span data-stu-id="eec70-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="eec70-130">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="eec70-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="eec70-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eec70-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eec70-132">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="eec70-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




