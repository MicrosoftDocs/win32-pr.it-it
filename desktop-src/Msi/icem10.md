---
description: ICEM10 verifica che un modulo merge includa solo le proprietà consentite nella tabella delle proprietà.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314789"
---
# <a name="icem10"></a><span data-ttu-id="8ae50-103">ICEM10</span><span class="sxs-lookup"><span data-stu-id="8ae50-103">ICEM10</span></span>

<span data-ttu-id="8ae50-104">ICEM10 verifica che un modulo merge includa solo le proprietà consentite nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ae50-104">ICEM10 verifies that a merge module contains only properties that are allowed in the [Property Table](property-table.md).</span></span> <span data-ttu-id="8ae50-105">Nella tabella delle proprietà non sono consentite le seguenti proprietà specifiche del prodotto:</span><span class="sxs-lookup"><span data-stu-id="8ae50-105">The following product specific properties are not allowed in the Property Table:</span></span>

-   [<span data-ttu-id="8ae50-106">**Proprietà ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="8ae50-106">**ProductLanguage Property**</span></span>](productlanguage.md)
-   [<span data-ttu-id="8ae50-107">**Proprietà ProductCode**</span><span class="sxs-lookup"><span data-stu-id="8ae50-107">**ProductCode Property**</span></span>](productcode.md)
-   [<span data-ttu-id="8ae50-108">**Proprietà ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="8ae50-108">**ProductVersion Property**</span></span>](productversion.md)
-   [<span data-ttu-id="8ae50-109">**Proprietà ProductName**</span><span class="sxs-lookup"><span data-stu-id="8ae50-109">**ProductName Property**</span></span>](productname.md)
-   [<span data-ttu-id="8ae50-110">**Proprietà produttore**</span><span class="sxs-lookup"><span data-stu-id="8ae50-110">**Manufacturer Property**</span></span>](manufacturer.md)

## <a name="result"></a><span data-ttu-id="8ae50-111">Risultato</span><span class="sxs-lookup"><span data-stu-id="8ae50-111">Result</span></span>

<span data-ttu-id="8ae50-112">ICEM10 Invia un errore quando un modulo merge contiene una proprietà non consentita nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ae50-112">ICEM10 posts an error when a merge module contains a property that is not allowed in the [Property Table](property-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="8ae50-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="8ae50-113">Example</span></span>

<span data-ttu-id="8ae50-114">ICEM10 invia i messaggi di errore seguenti per un modulo che contiene le voci di database indicate.</span><span class="sxs-lookup"><span data-stu-id="8ae50-114">ICEM10 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

<span data-ttu-id="8ae50-115">Nella tabella seguente viene illustrata una [tabella delle proprietà](property-table.md)parziali.</span><span class="sxs-lookup"><span data-stu-id="8ae50-115">The following table shows you a partial [Property Table](property-table.md).</span></span>



| <span data-ttu-id="8ae50-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8ae50-116">Property</span></span>                                   | <span data-ttu-id="8ae50-117">Valori</span><span class="sxs-lookup"><span data-stu-id="8ae50-117">Values</span></span>    |
|--------------------------------------------|-----------|
| <span data-ttu-id="8ae50-118">Colore</span><span class="sxs-lookup"><span data-stu-id="8ae50-118">Color</span></span>                                      | <span data-ttu-id="8ae50-119">Red</span><span class="sxs-lookup"><span data-stu-id="8ae50-119">Red</span></span>       |
| [<span data-ttu-id="8ae50-120">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="8ae50-120">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="8ae50-121">Microsoft</span><span class="sxs-lookup"><span data-stu-id="8ae50-121">Microsoft</span></span> |
| [<span data-ttu-id="8ae50-122">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="8ae50-122">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="8ae50-123">1033</span><span class="sxs-lookup"><span data-stu-id="8ae50-123">1033</span></span>      |



 

<span data-ttu-id="8ae50-124">Nella procedura riportata di seguito viene illustrato come correggere gli errori.</span><span class="sxs-lookup"><span data-stu-id="8ae50-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="8ae50-125">**Per correggere gli errori**</span><span class="sxs-lookup"><span data-stu-id="8ae50-125">**To fix the errors**</span></span>

1.  <span data-ttu-id="8ae50-126">Rimuovere la proprietà'[**Manufacturer**](manufacturer.md)' dalla [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ae50-126">Remove the '[**Manufacturer**](manufacturer.md)' property from the [Property Table](property-table.md).</span></span>
2.  <span data-ttu-id="8ae50-127">Rimuovere la proprietà'[**ProductLanguage**](productlanguage.md)' dalla [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ae50-127">Remove the '[**ProductLanguage**](productlanguage.md)' property from the [Property Table](property-table.md).</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="8ae50-128">Tabella utilizzata durante l'esecuzione</span><span class="sxs-lookup"><span data-stu-id="8ae50-128">Table Used During Execution</span></span>

<span data-ttu-id="8ae50-129">La [tabella delle proprietà](property-table.md) viene utilizzata durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8ae50-129">The [Property Table](property-table.md) is used during execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ae50-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ae50-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ae50-131">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="8ae50-131">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



