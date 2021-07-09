---
description: Ottenere informazioni sulla proprietà DocumentURI. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: DocumentURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb4d1572417ac85e14c25c238be1d49611ba858
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548809"
---
# <a name="documenturi"></a><span data-ttu-id="86142-105">DocumentURI</span><span class="sxs-lookup"><span data-stu-id="86142-105">DocumentURI</span></span>

<span data-ttu-id="86142-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="86142-106">This topic is not current.</span></span> <span data-ttu-id="86142-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="86142-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="86142-108">Specifica un URI (Uniform Resource Identifier) per il documento.</span><span class="sxs-lookup"><span data-stu-id="86142-108">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="86142-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="86142-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="86142-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="86142-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="86142-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="86142-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="86142-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="86142-112">Element Information</span></span>



| <span data-ttu-id="86142-113">Nome</span><span class="sxs-lookup"><span data-stu-id="86142-113">Name</span></span> | <span data-ttu-id="86142-114">Valore</span><span class="sxs-lookup"><span data-stu-id="86142-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="86142-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="86142-115">Element Type</span></span> <br/>   | <span data-ttu-id="86142-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="86142-116">Property</span></span><br/> |
| <span data-ttu-id="86142-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="86142-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="86142-118">Documento</span><span class="sxs-lookup"><span data-stu-id="86142-118">Document</span></span><br/> |
| <span data-ttu-id="86142-119">Note</span><span class="sxs-lookup"><span data-stu-id="86142-119">Notes</span></span> <br/>          | <span data-ttu-id="86142-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="86142-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="86142-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="86142-121">Structural Content</span></span>

<span data-ttu-id="86142-122">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="86142-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="86142-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="86142-123">Structure Variables</span></span>

<span data-ttu-id="86142-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="86142-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="86142-125">Nome</span><span class="sxs-lookup"><span data-stu-id="86142-125">Name</span></span>                            | <span data-ttu-id="86142-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="86142-126">Data type</span></span>         | <span data-ttu-id="86142-127">Unità</span><span class="sxs-lookup"><span data-stu-id="86142-127">Unit</span></span> | <span data-ttu-id="86142-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="86142-128">Supported values</span></span> | <span data-ttu-id="86142-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="86142-129">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="86142-130">\_DocumentURIValue\_</span><span class="sxs-lookup"><span data-stu-id="86142-130">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="86142-131">string</span><span class="sxs-lookup"><span data-stu-id="86142-131">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="86142-132">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="86142-132">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="86142-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86142-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86142-134">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="86142-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




