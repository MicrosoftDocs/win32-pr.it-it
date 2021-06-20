---
description: Informazioni sull'elemento JobName, che specifica un nome descrittivo per il processo. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfb63a54e9501ff5dc45ff09a925396c168b20c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408874"
---
# <a name="jobname"></a><span data-ttu-id="ee846-104">JobName</span><span class="sxs-lookup"><span data-stu-id="ee846-104">JobName</span></span>

<span data-ttu-id="ee846-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="ee846-105">This topic is not current.</span></span> <span data-ttu-id="ee846-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ee846-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ee846-107">Specifica un nome descrittivo per il processo.</span><span class="sxs-lookup"><span data-stu-id="ee846-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="ee846-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ee846-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ee846-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ee846-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ee846-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ee846-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ee846-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ee846-111">Element Information</span></span>



| <span data-ttu-id="ee846-112">Nome</span><span class="sxs-lookup"><span data-stu-id="ee846-112">Name</span></span> | <span data-ttu-id="ee846-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ee846-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="ee846-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="ee846-114">Element Type</span></span> <br/>   | <span data-ttu-id="ee846-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee846-115">Property</span></span><br/> |
| <span data-ttu-id="ee846-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="ee846-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ee846-117">Processo</span><span class="sxs-lookup"><span data-stu-id="ee846-117">Job</span></span><br/>      |
| <span data-ttu-id="ee846-118">Note</span><span class="sxs-lookup"><span data-stu-id="ee846-118">Notes</span></span> <br/>          | <span data-ttu-id="ee846-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="ee846-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="ee846-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="ee846-120">Structural Content</span></span>

<span data-ttu-id="ee846-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="ee846-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="ee846-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="ee846-122">Structure Variables</span></span>

<span data-ttu-id="ee846-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="ee846-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ee846-124">Nome</span><span class="sxs-lookup"><span data-stu-id="ee846-124">Name</span></span>                        | <span data-ttu-id="ee846-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ee846-125">Data type</span></span>         | <span data-ttu-id="ee846-126">Unità</span><span class="sxs-lookup"><span data-stu-id="ee846-126">Unit</span></span> | <span data-ttu-id="ee846-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="ee846-127">Supported values</span></span> | <span data-ttu-id="ee846-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="ee846-128">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="ee846-129">\_JobNameValue\_</span><span class="sxs-lookup"><span data-stu-id="ee846-129">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="ee846-130">string</span><span class="sxs-lookup"><span data-stu-id="ee846-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ee846-131">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="ee846-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="ee846-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee846-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee846-133">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ee846-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




