---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: DocumentName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66809ef18edb7aa313ea5218f9122acf4ddd1ee8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997798"
---
# <a name="documentname"></a><span data-ttu-id="63503-104">DocumentName</span><span class="sxs-lookup"><span data-stu-id="63503-104">DocumentName</span></span>

<span data-ttu-id="63503-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="63503-105">This topic is not current.</span></span> <span data-ttu-id="63503-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="63503-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="63503-107">Specifica un nome descrittivo per il documento.</span><span class="sxs-lookup"><span data-stu-id="63503-107">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="63503-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="63503-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="63503-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="63503-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="63503-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="63503-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="63503-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="63503-111">Element Information</span></span>



| <span data-ttu-id="63503-112">Nome</span><span class="sxs-lookup"><span data-stu-id="63503-112">Name</span></span> | <span data-ttu-id="63503-113">Valore</span><span class="sxs-lookup"><span data-stu-id="63503-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="63503-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="63503-114">Element Type</span></span> <br/>   | <span data-ttu-id="63503-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="63503-115">Property</span></span><br/> |
| <span data-ttu-id="63503-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="63503-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="63503-117">Documento</span><span class="sxs-lookup"><span data-stu-id="63503-117">Document</span></span><br/> |
| <span data-ttu-id="63503-118">Note</span><span class="sxs-lookup"><span data-stu-id="63503-118">Notes</span></span> <br/>          | <span data-ttu-id="63503-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="63503-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="63503-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="63503-120">Structural Content</span></span>

<span data-ttu-id="63503-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="63503-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="63503-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="63503-122">Structure Variables</span></span>

<span data-ttu-id="63503-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="63503-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="63503-124">Nome</span><span class="sxs-lookup"><span data-stu-id="63503-124">Name</span></span>                             | <span data-ttu-id="63503-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="63503-125">Data type</span></span>         | <span data-ttu-id="63503-126">Unità</span><span class="sxs-lookup"><span data-stu-id="63503-126">Unit</span></span> | <span data-ttu-id="63503-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="63503-127">Supported values</span></span> | <span data-ttu-id="63503-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="63503-128">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="63503-129">\_DocumentNameValue\_</span><span class="sxs-lookup"><span data-stu-id="63503-129">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="63503-130">string</span><span class="sxs-lookup"><span data-stu-id="63503-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="63503-131">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="63503-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="63503-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63503-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63503-133">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="63503-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




