---
description: Informazioni sulla proprietà DocumentName, che specifica un nome descrittivo per il documento.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: DocumentName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202ff1f5bac85fec3feac9f141834adfcd37e70
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409274"
---
# <a name="documentname"></a><span data-ttu-id="770e2-103">DocumentName</span><span class="sxs-lookup"><span data-stu-id="770e2-103">DocumentName</span></span>

<span data-ttu-id="770e2-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="770e2-104">This topic is not current.</span></span> <span data-ttu-id="770e2-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="770e2-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="770e2-106">Specifica un nome descrittivo per il documento.</span><span class="sxs-lookup"><span data-stu-id="770e2-106">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="770e2-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="770e2-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="770e2-108">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="770e2-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="770e2-109">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="770e2-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="770e2-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="770e2-110">Element Information</span></span>



| <span data-ttu-id="770e2-111">Nome</span><span class="sxs-lookup"><span data-stu-id="770e2-111">Name</span></span> | <span data-ttu-id="770e2-112">Valore</span><span class="sxs-lookup"><span data-stu-id="770e2-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="770e2-113">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="770e2-113">Element Type</span></span> <br/>   | <span data-ttu-id="770e2-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="770e2-114">Property</span></span><br/> |
| <span data-ttu-id="770e2-115">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="770e2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="770e2-116">Documento</span><span class="sxs-lookup"><span data-stu-id="770e2-116">Document</span></span><br/> |
| <span data-ttu-id="770e2-117">Note</span><span class="sxs-lookup"><span data-stu-id="770e2-117">Notes</span></span> <br/>          | <span data-ttu-id="770e2-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="770e2-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="770e2-119">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="770e2-119">Structural Content</span></span>

<span data-ttu-id="770e2-120">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="770e2-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="770e2-121">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="770e2-121">Structure Variables</span></span>

<span data-ttu-id="770e2-122">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="770e2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="770e2-123">Nome</span><span class="sxs-lookup"><span data-stu-id="770e2-123">Name</span></span>                             | <span data-ttu-id="770e2-124">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="770e2-124">Data type</span></span>         | <span data-ttu-id="770e2-125">Unità</span><span class="sxs-lookup"><span data-stu-id="770e2-125">Unit</span></span> | <span data-ttu-id="770e2-126">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="770e2-126">Supported values</span></span> | <span data-ttu-id="770e2-127">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="770e2-127">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="770e2-128">\_DocumentNameValue\_</span><span class="sxs-lookup"><span data-stu-id="770e2-128">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="770e2-129">string</span><span class="sxs-lookup"><span data-stu-id="770e2-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="770e2-130">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="770e2-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="770e2-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="770e2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="770e2-132">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="770e2-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




