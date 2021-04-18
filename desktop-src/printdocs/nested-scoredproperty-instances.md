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
# <a name="nested-scoredproperty-instances"></a>Istanze ScoredProperty annidate

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Si noti che non è possibile aggiungere istanze di ScoredProperty come elementi figlio di un'istanza di Option. Le istanze di ScoredProperty possono anche essere annidate all'interno di altre istanze di ScoredProperty. Questa operazione è utile quando una proprietà del dispositivo è complessa ed è rappresentata in modo ottimale da più sottoproprietà. L'aggiunta di sottoproprietà a una proprietà (o Public) esistente o a ScoredProperty è un modo efficace per migliorare un'opzione, mantenendo al tempo stesso la portabilità con le istanze delle opzioni esistenti. Ad esempio, le istanze di opzioni standard per la funzionalità MediaType contengono un ScoredProperty che descrive il peso del supporto come leggero, medio, intenso o intenso. Se si desidera una descrizione più precisa del peso, è possibile aggiungere una sottoproprietà (GramsPer100Sheets nell'esempio seguente) che contiene il peso effettivo (in grammi) di 100 fogli di supporti. L'opzione avanzata potrebbe essere simile all'esempio seguente.

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

Un confronto tra le istanze di opzioni originali e avanzate produce una corrispondenza quasi perfetta, perché l'opzione Enhanced è un superset dell'originale e vengono mantenuti i percorsi e i valori di ognuna delle istanze di ScoredProperty originali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



