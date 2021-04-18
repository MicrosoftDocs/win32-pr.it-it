---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c182e5d0bfcfb395eb553570cca745b618fc56b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320966"
---
# <a name="jobid"></a><span data-ttu-id="bb984-104">JobID</span><span class="sxs-lookup"><span data-stu-id="bb984-104">JobID</span></span>

<span data-ttu-id="bb984-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="bb984-105">This topic is not current.</span></span> <span data-ttu-id="bb984-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bb984-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bb984-107">Specifica un ID univoco per il processo.</span><span class="sxs-lookup"><span data-stu-id="bb984-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="bb984-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bb984-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bb984-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="bb984-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bb984-110">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="bb984-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bb984-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bb984-111">Element Information</span></span>



| <span data-ttu-id="bb984-112">Nome</span><span class="sxs-lookup"><span data-stu-id="bb984-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="bb984-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="bb984-113">Element Type</span></span> <br/>   | <span data-ttu-id="bb984-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bb984-114">Property</span></span><br/> |
| <span data-ttu-id="bb984-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="bb984-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bb984-116">Processo</span><span class="sxs-lookup"><span data-stu-id="bb984-116">Job</span></span><br/>      |
| <span data-ttu-id="bb984-117">Note</span><span class="sxs-lookup"><span data-stu-id="bb984-117">Notes</span></span> <br/>          | <span data-ttu-id="bb984-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="bb984-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="bb984-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="bb984-119">Structural Content</span></span>

<span data-ttu-id="bb984-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="bb984-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="bb984-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="bb984-121">Structure Variables</span></span>

<span data-ttu-id="bb984-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="bb984-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bb984-123">Nome</span><span class="sxs-lookup"><span data-stu-id="bb984-123">Name</span></span>                      | <span data-ttu-id="bb984-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bb984-124">Data type</span></span>         | <span data-ttu-id="bb984-125">Unità</span><span class="sxs-lookup"><span data-stu-id="bb984-125">Unit</span></span> | <span data-ttu-id="bb984-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="bb984-126">Supported values</span></span> | <span data-ttu-id="bb984-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="bb984-127">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="bb984-128">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="bb984-128">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="bb984-129">string</span><span class="sxs-lookup"><span data-stu-id="bb984-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bb984-130">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="bb984-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="bb984-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bb984-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb984-132">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="bb984-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




