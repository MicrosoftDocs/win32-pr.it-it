---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Istanze ScoredProperty annidate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1bfed09c48bc0ac6e93e09f96dc8116e8b0a91
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320933"
---
# <a name="nested-scoredproperty-instances"></a><span data-ttu-id="d720d-104">Istanze ScoredProperty annidate</span><span class="sxs-lookup"><span data-stu-id="d720d-104">Nested ScoredProperty Instances</span></span>

<span data-ttu-id="d720d-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d720d-105">This topic is not current.</span></span> <span data-ttu-id="d720d-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d720d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d720d-107">Si noti che non è possibile aggiungere istanze di ScoredProperty come elementi figlio di un'istanza di Option.</span><span class="sxs-lookup"><span data-stu-id="d720d-107">Notice that you are not restricted to adding ScoredProperty instances as child elements of an Option instance.</span></span> <span data-ttu-id="d720d-108">Le istanze di ScoredProperty possono anche essere annidate all'interno di altre istanze di ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="d720d-108">ScoredProperty instances may also be nested within other ScoredProperty instances.</span></span> <span data-ttu-id="d720d-109">Questa operazione è utile quando una proprietà del dispositivo è complessa ed è rappresentata in modo ottimale da più sottoproprietà.</span><span class="sxs-lookup"><span data-stu-id="d720d-109">This is useful when a device property is complex and is best represented by multiple subproperties.</span></span> <span data-ttu-id="d720d-110">L'aggiunta di sottoproprietà a una proprietà (o Public) esistente o a ScoredProperty è un modo efficace per migliorare un'opzione, mantenendo al tempo stesso la portabilità con le istanze delle opzioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="d720d-110">Adding subproperties to an existing (or public) Property or ScoredProperty is a good way to enhance an Option, while retaining portability with existing Option instances.</span></span> <span data-ttu-id="d720d-111">Ad esempio, le istanze di opzioni standard per la funzionalità MediaType contengono un ScoredProperty che descrive il peso del supporto come leggero, medio, intenso o intenso.</span><span class="sxs-lookup"><span data-stu-id="d720d-111">For example, the standard Option instances for the MediaType Feature contain a ScoredProperty describing the weight of the media as Light, Medium, Heavy, or ExtraHeavy.</span></span> <span data-ttu-id="d720d-112">Se si desidera una descrizione più precisa del peso, è possibile aggiungere una sottoproprietà (GramsPer100Sheets nell'esempio seguente) che contiene il peso effettivo (in grammi) di 100 fogli di supporti.</span><span class="sxs-lookup"><span data-stu-id="d720d-112">If you want more precise descriptions of the weight, you can add a subproperty (GramsPer100Sheets in the following example) that contains the actual weight (in grams) of 100 sheets of media.</span></span> <span data-ttu-id="d720d-113">L'opzione avanzata potrebbe essere simile all'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="d720d-113">The enhanced Option might look like the following example.</span></span>

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

<span data-ttu-id="d720d-114">Un confronto tra le istanze di opzioni originali e avanzate produce una corrispondenza quasi perfetta, perché l'opzione Enhanced è un superset dell'originale e vengono mantenuti i percorsi e i valori di ognuna delle istanze di ScoredProperty originali.</span><span class="sxs-lookup"><span data-stu-id="d720d-114">A comparison of the original and enhanced Option instances produces a near-perfect match, because the enhanced Option is a superset of the original, and the locations and values of each of the original ScoredProperty instances is preserved.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d720d-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d720d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d720d-116">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="d720d-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



