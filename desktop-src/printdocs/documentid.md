---
description: Informazioni sull'elemento DocumentID, che specifica un ID univoco per il documento. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 6e7899e3-9b64-48bd-8683-aba627458f2a
title: DocumentID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b267fead0322351cde396bf2eb6d0efa8c523f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409285"
---
# <a name="documentid"></a><span data-ttu-id="9c04f-104">DocumentID</span><span class="sxs-lookup"><span data-stu-id="9c04f-104">DocumentID</span></span>

<span data-ttu-id="9c04f-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="9c04f-105">This topic is not current.</span></span> <span data-ttu-id="9c04f-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9c04f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9c04f-107">Specifica un ID univoco per il documento.</span><span class="sxs-lookup"><span data-stu-id="9c04f-107">Specifies a unique ID for the document.</span></span>

-   [<span data-ttu-id="9c04f-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9c04f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9c04f-109">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="9c04f-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9c04f-110">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9c04f-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9c04f-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9c04f-111">Element Information</span></span>



| <span data-ttu-id="9c04f-112">Nome</span><span class="sxs-lookup"><span data-stu-id="9c04f-112">Name</span></span> | <span data-ttu-id="9c04f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="9c04f-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="9c04f-114">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="9c04f-114">Element Type</span></span> <br/>   | <span data-ttu-id="9c04f-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9c04f-115">Property</span></span><br/> |
| <span data-ttu-id="9c04f-116">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="9c04f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9c04f-117">Documento</span><span class="sxs-lookup"><span data-stu-id="9c04f-117">Document</span></span><br/> |
| <span data-ttu-id="9c04f-118">Note</span><span class="sxs-lookup"><span data-stu-id="9c04f-118">Notes</span></span> <br/>          | <span data-ttu-id="9c04f-119">nessuno</span><span class="sxs-lookup"><span data-stu-id="9c04f-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="9c04f-120">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="9c04f-120">Structural Content</span></span>

<span data-ttu-id="9c04f-121">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="9c04f-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string">_DocumentIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="9c04f-122">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="9c04f-122">Structure Variables</span></span>

<span data-ttu-id="9c04f-123">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="9c04f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9c04f-124">Nome</span><span class="sxs-lookup"><span data-stu-id="9c04f-124">Name</span></span>                           | <span data-ttu-id="9c04f-125">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9c04f-125">Data type</span></span>         | <span data-ttu-id="9c04f-126">Unità</span><span class="sxs-lookup"><span data-stu-id="9c04f-126">Unit</span></span> | <span data-ttu-id="9c04f-127">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="9c04f-127">Supported values</span></span> | <span data-ttu-id="9c04f-128">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="9c04f-128">Summary</span></span> |
|--------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="9c04f-129">\_DocumentIDValue\_</span><span class="sxs-lookup"><span data-stu-id="9c04f-129">\_DocumentIDValue\_</span></span><br/> | <span data-ttu-id="9c04f-130">string</span><span class="sxs-lookup"><span data-stu-id="9c04f-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9c04f-131">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="9c04f-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="9c04f-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c04f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c04f-133">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="9c04f-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




