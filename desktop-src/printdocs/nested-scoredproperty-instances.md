---
description: Le istanze scoredProperty possono anche essere annidate all'interno di altre istanze scoredProperty o come elementi figlio di un'istanza option.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Istanze scoredProperty annidate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0824e5645d723cdf3f0f45d985f3dd06b8c1b74de32fd2e47bb5843e37c2540f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099045"
---
# <a name="nested-scoredproperty-instances"></a>Istanze scoredProperty annidate

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Si noti che non si è limitati all'aggiunta di istanze ScoredProperty come elementi figlio di un'istanza option. Le istanze scoredProperty possono anche essere annidate all'interno di altre istanze scoredProperty. Ciò è utile quando una proprietà del dispositivo è complessa ed è rappresentata meglio da più sottoproprietà. L'aggiunta di sottoproprietà a una proprietà esistente (o pubblica) o ScoredProperty è un buon modo per migliorare un'opzione, mantenendo al tempo stesso la portabilità con le istanze Option esistenti. Ad esempio, le istanze Option standard per la funzionalità MediaType contengono un oggetto ScoredProperty che descrive il peso dei supporti come Light, Medium, Heavy o ExtraHeavy. Se si desidera una descrizione più precisa del peso, è possibile aggiungere una sottoproprietà (GramsPer100Sheets nell'esempio seguente) che contiene il peso effettivo (in grammi) di 100 fogli di supporti. L'opzione avanzata potrebbe essere simile all'esempio seguente.

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

Un confronto tra le istanze Option originali e migliorate produce una corrispondenza quasi perfetta, perché l'opzione avanzata è un superset dell'originale e vengono mantenuti i percorsi e i valori di ognuna delle istanze scoredProperty originali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



