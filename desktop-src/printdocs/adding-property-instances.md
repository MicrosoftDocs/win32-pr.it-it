---
description: Informazioni sull'aggiunta di istanze property. Lo schema di stampa consente alle istanze property di essere presenti in un'istanza option.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Aggiunta di istanze di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8085fa10f824f32dc76aef0f1e5f78ca05b22b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409694"
---
# <a name="adding-property-instances"></a>Aggiunta di istanze di proprietà

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema di stampa consente alle istanze property di essere presenti in un'istanza option. Le istanze Property definite nel documento PrintCapabilities non vengono propagate alle istanze Option salvate in PrintTicket. Gli elementi proprietà non influiscono sul risultato del processo di assegnazione dei punteggi quando vengono confrontate due istanze di Option, ma le istanze ScoredProperty influiscono su questo processo. Tutti i driver di dispositivo che implementano un algoritmo di assegnazione dei punteggi devono osservare questa convenzione. I provider PrintCapabilities sono autorizzati ad aggiungere istanze Property a un'opzione se queste istanze sono specifiche di tale opzione specifica e nessun altro oppure se il provider intende che il valore di questa proprietà venga visualizzato per ogni opzione nella funzionalità. Si supponga, ad esempio, che la proprietà PrintRate sia dipendente dall'opzione selezionata per la funzionalità PageResolution. Se la proprietà PrintRate fosse posizionata al livello radice del documento PrintCapabilities, sarebbe a valore singolo e rifletterebbe solo la frequenza di stampa per la risoluzione attualmente selezionata. Tuttavia, se la proprietà PrintRate è stata inserita all'interno di ogni opzione PageResolution, ogni istanza della proprietà PrintRate potrebbe riflettere la frequenza di stampa per l'opzione PageResolution che la conteneva. Il documento PrintCapabilities conterrà più definizioni per PrintRate, una corrispondente a ogni opzione PageResolution. Usando una rappresentazione abbreviata, PrintCapabilities conterrà:

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

In alcune situazioni, inserire una proprietà della frequenza di stampa all'interno di ogni opzione di risoluzione è più utile per il client, perché il client può determinare a colpo d'occhio l'effetto che ogni opzione di risoluzione ha sulla frequenza di stampa, senza la necessità di ottenere un nuovo documento PrintCapabilities per ogni impostazione di risoluzione.

Si noti anche che le istanze property possono essere aggiunte anche come elementi figlio degli elementi Feature. Ciò è utile se sono presenti istanze Property o valori di istanze Property specifici di ogni funzionalità. Ad esempio, potrebbe essere presente una proprietà che specifica se è consentito selezionare una sola opzione contemporaneamente per una funzionalità o se è possibile selezionare più opzioni. Si tratta della proprietà PICK \_ ONE, PICK \_ MANY usata nei file PPD e GPD. Poiché alcune istanze di funzionalità possono essere identificate come PICK ONE, mentre altre possono essere identificate come PICK MANY, questa proprietà deve essere \_ \_ definita per ogni funzionalità. L'individuazione della proprietà come elemento figlio della funzionalità produce l'associazione tra la proprietà e la funzionalità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



