---
description: Informazioni sull'elemento JobID, che specifica un ID univoco per il processo. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfd17d068f34b56d45e4851c06b7ed1d9bd6fcc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408884"
---
# <a name="jobid"></a><span data-ttu-id="4d4fe-104">JobID</span><span class="sxs-lookup"><span data-stu-id="4d4fe-104">JobID</span></span>

<span data-ttu-id="4d4fe-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="4d4fe-105">This topic is not current.</span></span> <span data-ttu-id="4d4fe-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4d4fe-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4d4fe-107">Specifica un ID univoco per il processo.</span><span class="sxs-lookup"><span data-stu-id="4d4fe-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="4d4fe-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4d4fe-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4d4fe-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="4d4fe-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4d4fe-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4d4fe-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4d4fe-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4d4fe-111">Element Information</span></span>



| <span data-ttu-id="4d4fe-112">Nome</span><span class="sxs-lookup"><span data-stu-id="4d4fe-112">Name</span></span> | <span data-ttu-id="4d4fe-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4d4fe-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="4d4fe-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="4d4fe-114">Element Type</span></span> <br/>   | <span data-ttu-id="4d4fe-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4d4fe-115">Property</span></span><br/> |
| <span data-ttu-id="4d4fe-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="4d4fe-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4d4fe-117">Processo</span><span class="sxs-lookup"><span data-stu-id="4d4fe-117">Job</span></span><br/>      |
| <span data-ttu-id="4d4fe-118">Note</span><span class="sxs-lookup"><span data-stu-id="4d4fe-118">Notes</span></span> <br/>          | <span data-ttu-id="4d4fe-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="4d4fe-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="4d4fe-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="4d4fe-120">Structural Content</span></span>

<span data-ttu-id="4d4fe-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="4d4fe-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="4d4fe-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="4d4fe-122">Structure Variables</span></span>

<span data-ttu-id="4d4fe-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="4d4fe-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4d4fe-124">Nome</span><span class="sxs-lookup"><span data-stu-id="4d4fe-124">Name</span></span>                      | <span data-ttu-id="4d4fe-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4d4fe-125">Data type</span></span>         | <span data-ttu-id="4d4fe-126">Unità</span><span class="sxs-lookup"><span data-stu-id="4d4fe-126">Unit</span></span> | <span data-ttu-id="4d4fe-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="4d4fe-127">Supported values</span></span> | <span data-ttu-id="4d4fe-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="4d4fe-128">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="4d4fe-129">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="4d4fe-129">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="4d4fe-130">string</span><span class="sxs-lookup"><span data-stu-id="4d4fe-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4d4fe-131">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="4d4fe-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="4d4fe-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4d4fe-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d4fe-133">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="4d4fe-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




