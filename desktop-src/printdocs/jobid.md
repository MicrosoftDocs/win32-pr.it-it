---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2d77d185ab7edc611a82f94a2ce92428d9f167
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998138"
---
# <a name="jobid"></a><span data-ttu-id="74e85-104">JobID</span><span class="sxs-lookup"><span data-stu-id="74e85-104">JobID</span></span>

<span data-ttu-id="74e85-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="74e85-105">This topic is not current.</span></span> <span data-ttu-id="74e85-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="74e85-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="74e85-107">Specifica un ID univoco per il processo.</span><span class="sxs-lookup"><span data-stu-id="74e85-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="74e85-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="74e85-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="74e85-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="74e85-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="74e85-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="74e85-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="74e85-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="74e85-111">Element Information</span></span>



| <span data-ttu-id="74e85-112">Nome</span><span class="sxs-lookup"><span data-stu-id="74e85-112">Name</span></span> | <span data-ttu-id="74e85-113">Valore</span><span class="sxs-lookup"><span data-stu-id="74e85-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="74e85-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="74e85-114">Element Type</span></span> <br/>   | <span data-ttu-id="74e85-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="74e85-115">Property</span></span><br/> |
| <span data-ttu-id="74e85-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="74e85-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="74e85-117">Processo</span><span class="sxs-lookup"><span data-stu-id="74e85-117">Job</span></span><br/>      |
| <span data-ttu-id="74e85-118">Note</span><span class="sxs-lookup"><span data-stu-id="74e85-118">Notes</span></span> <br/>          | <span data-ttu-id="74e85-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="74e85-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="74e85-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="74e85-120">Structural Content</span></span>

<span data-ttu-id="74e85-121">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="74e85-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="74e85-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="74e85-122">Structure Variables</span></span>

<span data-ttu-id="74e85-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="74e85-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="74e85-124">Nome</span><span class="sxs-lookup"><span data-stu-id="74e85-124">Name</span></span>                      | <span data-ttu-id="74e85-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="74e85-125">Data type</span></span>         | <span data-ttu-id="74e85-126">Unità</span><span class="sxs-lookup"><span data-stu-id="74e85-126">Unit</span></span> | <span data-ttu-id="74e85-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="74e85-127">Supported values</span></span> | <span data-ttu-id="74e85-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="74e85-128">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="74e85-129">\_JobIDValue\_</span><span class="sxs-lookup"><span data-stu-id="74e85-129">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="74e85-130">string</span><span class="sxs-lookup"><span data-stu-id="74e85-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="74e85-131">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="74e85-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="74e85-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74e85-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74e85-133">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="74e85-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




