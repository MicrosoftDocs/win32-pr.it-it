---
description: Le istanze ScoredProperty possono anche essere annidate all'interno di altre istanze scoredProperty o come elementi figlio di un'istanza option.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Istanze scoredProperty annidate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a80d291fa59b2f36191f42b2f99ea9d22789a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408604"
---
# <a name="nested-scoredproperty-instances"></a><span data-ttu-id="e8f0b-103">Istanze scoredProperty annidate</span><span class="sxs-lookup"><span data-stu-id="e8f0b-103">Nested ScoredProperty Instances</span></span>

<span data-ttu-id="e8f0b-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="e8f0b-104">This topic is not current.</span></span> <span data-ttu-id="e8f0b-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e8f0b-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e8f0b-106">Si noti che non si è limitati all'aggiunta di istanze ScoredProperty come elementi figlio di un'istanza option.</span><span class="sxs-lookup"><span data-stu-id="e8f0b-106">Notice that you are not restricted to adding ScoredProperty instances as child elements of an Option instance.</span></span> <span data-ttu-id="e8f0b-107">Le istanze ScoredProperty possono anche essere annidate all'interno di altre istanze scoredProperty.</span><span class="sxs-lookup"><span data-stu-id="e8f0b-107">ScoredProperty instances may also be nested within other ScoredProperty instances.</span></span> <span data-ttu-id="e8f0b-108">Ciò è utile quando una proprietà del dispositivo è complessa ed è rappresentata meglio da più sottoproprietà.</span><span class="sxs-lookup"><span data-stu-id="e8f0b-108">This is useful when a device property is complex and is best represented by multiple subproperties.</span></span> <span data-ttu-id="e8f0b-109">L'aggiunta di sottoproprietà a una proprietà esistente (o pubblica) o ScoredProperty è un buon modo per migliorare un'opzione, mantenendo al tempo stesso la portabilità con le istanze Option esistenti.</span><span class="sxs-lookup"><span data-stu-id="e8f0b-109">Adding subproperties to an existing (or public) Property or ScoredProperty is a good way to enhance an Option, while retaining portability with existing Option instances.</span></span> <span data-ttu-id="e8f0b-110">Ad esempio, le istanze Option standard per la funzionalità MediaType contengono un oggetto ScoredProperty che descrive il peso dei supporti come Light, Medium, Heavy o ExtraHeavy.</span><span class="sxs-lookup"><span data-stu-id="e8f0b-110">For example, the standard Option instances for the MediaType Feature contain a ScoredProperty describing the weight of the media as Light, Medium, Heavy, or ExtraHeavy.</span></span> <span data-ttu-id="e8f0b-111">Se si desidera una descrizione più precisa del peso, è possibile aggiungere una sottoproprietà (SheetsPer100Sheets nell'esempio seguente) che contiene il peso effettivo (in grammi) di 100 fogli di supporti.</span><span class="sxs-lookup"><span data-stu-id="e8f0b-111">If you want more precise descriptions of the weight, you can add a subproperty (GramsPer100Sheets in the following example) that contains the actual weight (in grams) of 100 sheets of media.</span></span> <span data-ttu-id="e8f0b-112">L'opzione avanzata potrebbe essere simile all'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="e8f0b-112">The enhanced Option might look like the following example.</span></span>

``` syntax
<!-- Note: The following ScoredProperty is not a Public Print Schema ScoredProperty -->
<!-- This example shows a nested ScoredProperty defined by a Private namespace-->
<!-- It is included for illustration purposes. -->

<psf:ScoredProperty name="FabrikamES500:PaperWeight">
  <psf:Value xsi:type="xs:string">Medium</psf:Value>
  <psf:ScoredProperty name="FabrikamES500:GramsPerSheet">
    <Value xsi:type="decimal">109.5</Value>
  </psf:ScoredProperty>
</psf:ScoredProperty>
```

<span data-ttu-id="e8f0b-113">Un confronto tra le istanze Option originali e migliorate produce una corrispondenza quasi perfetta, perché l'opzione avanzata è un superset dell'originale e vengono mantenuti i percorsi e i valori di ognuna delle istanze scoredProperty originali.</span><span class="sxs-lookup"><span data-stu-id="e8f0b-113">A comparison of the original and enhanced Option instances produces a near-perfect match, because the enhanced Option is a superset of the original, and the locations and values of each of the original ScoredProperty instances is preserved.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8f0b-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8f0b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8f0b-115">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e8f0b-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



