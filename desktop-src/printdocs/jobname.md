---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161801e56a27e33cdf921cc07c93e59836d4dd90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320869"
---
# <a name="jobname"></a><span data-ttu-id="bd86d-104">JobName</span><span class="sxs-lookup"><span data-stu-id="bd86d-104">JobName</span></span>

<span data-ttu-id="bd86d-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="bd86d-105">This topic is not current.</span></span> <span data-ttu-id="bd86d-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bd86d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bd86d-107">Specifica un nome descrittivo per il processo.</span><span class="sxs-lookup"><span data-stu-id="bd86d-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="bd86d-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bd86d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bd86d-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="bd86d-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bd86d-110">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="bd86d-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bd86d-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bd86d-111">Element Information</span></span>



| <span data-ttu-id="bd86d-112">Nome</span><span class="sxs-lookup"><span data-stu-id="bd86d-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="bd86d-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="bd86d-113">Element Type</span></span> <br/>   | <span data-ttu-id="bd86d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bd86d-114">Property</span></span><br/> |
| <span data-ttu-id="bd86d-115">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="bd86d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bd86d-116">Processo</span><span class="sxs-lookup"><span data-stu-id="bd86d-116">Job</span></span><br/>      |
| <span data-ttu-id="bd86d-117">Note</span><span class="sxs-lookup"><span data-stu-id="bd86d-117">Notes</span></span> <br/>          | <span data-ttu-id="bd86d-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="bd86d-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="bd86d-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="bd86d-119">Structural Content</span></span>

<span data-ttu-id="bd86d-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="bd86d-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="bd86d-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="bd86d-121">Structure Variables</span></span>

<span data-ttu-id="bd86d-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="bd86d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bd86d-123">Nome</span><span class="sxs-lookup"><span data-stu-id="bd86d-123">Name</span></span>                        | <span data-ttu-id="bd86d-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bd86d-124">Data type</span></span>         | <span data-ttu-id="bd86d-125">Unità</span><span class="sxs-lookup"><span data-stu-id="bd86d-125">Unit</span></span> | <span data-ttu-id="bd86d-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="bd86d-126">Supported values</span></span> | <span data-ttu-id="bd86d-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="bd86d-127">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="bd86d-128">\_JobNameValue\_</span><span class="sxs-lookup"><span data-stu-id="bd86d-128">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="bd86d-129">string</span><span class="sxs-lookup"><span data-stu-id="bd86d-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bd86d-130">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="bd86d-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="bd86d-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd86d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd86d-132">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="bd86d-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




