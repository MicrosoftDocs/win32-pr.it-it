---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Aggiunta di istanze di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08e3df1b6c271c37c080968cc775ac11eba2e3ce
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104401836"
---
# <a name="adding-property-instances"></a>Aggiunta di istanze di proprietà

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema di stampa consente la presenza di istanze di proprietà in un'istanza di Option. Le istanze di proprietà definite nel documento PrintCapabilities non vengono propagate alle istanze delle opzioni salvate nel PrintTicket. Gli elementi proprietà non influiscono sul risultato del processo di assegnazione dei punteggi quando vengono confrontate due istanze di opzioni, ma le istanze di ScoredProperty influiscono su questo processo. Tutti i driver di dispositivo che implementano un algoritmo di assegnazione dei punteggi devono osservare questa convenzione. Ai provider PrintCapabilities è consentito aggiungere istanze di proprietà a un'opzione se tali istanze sono specifiche di questa particolare opzione e non altre, oppure se il provider intende visualizzare il valore di questa proprietà per ogni opzione della funzionalità. Si supponga, ad esempio, che la proprietà PrintRate dipenda dall'opzione selezionata per la funzionalità PageResolution. Se la proprietà PrintRate è stata posizionata al livello radice del documento PrintCapabilities, sarà a valore singolo e rifletterà solo la velocità di stampa per la risoluzione attualmente selezionata. Tuttavia, se la proprietà PrintRate è stata inserita all'interno di ogni opzione PageResolution, ogni istanza della proprietà PrintRate potrebbe riflettere la velocità di stampa per l'opzione PageResolution che lo conteneva. Il documento PrintCapabilities conterrebbe più definizioni per PrintRate, una corrispondente a ogni opzione PageResolution. Utilizzando una rappresentazione abbreviata, l'oggetto PrintCapabilities conterrebbe:

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

In alcune situazioni, l'inserimento di una proprietà della frequenza di stampa all'interno di ogni opzione di risoluzione è più utile per il client, perché il client può determinare a colpo d'occhio l'effetto di ogni opzione di risoluzione sulla frequenza di stampa, senza dover ottenere un nuovo documento PrintCapabilities per ogni impostazione di risoluzione.

Si noti inoltre che anche le istanze di proprietà possono essere aggiunte come elementi figlio di elementi Feature. Questa operazione è utile se sono presenti istanze di proprietà o valori di istanze di proprietà specifiche di ogni funzionalità. Ad esempio, potrebbe essere presente una proprietà che specifica se è consentita la selezione di una sola opzione alla volta per una funzionalità o se è possibile selezionare più opzioni. Questa è la scelta selezionata \_ . scegliere \_ molti proprietà usati nei file PPD e GPD. Poiché alcune istanze della funzionalità possono essere identificate come PICK \_ One, mentre altre possono essere identificate come pick \_ many, questa proprietà deve essere definita per ogni funzionalità. L'individuazione della proprietà come elemento figlio della funzionalità produce l'associazione tra la proprietà e la funzionalità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



