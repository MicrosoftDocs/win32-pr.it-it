---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Parametri di riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815ec7cd412e158a73e2b760f9f6080d7b0326a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321061"
---
# <a name="referencing-parameters"></a>Parametri di riferimento

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un esempio concreto di un'opzione che include un elemento ParameterRef è l'opzione Dimensioni supporti personalizzate. Si noti che fa riferimento a due parametri: PageMediaSizeMediaSizeWidth e PageMediaSizeMediaSizeHeight. Ogni istanza di ParameterRef fa riferimento a un'istanza di ParameterDef definita altrove nel documento PrintCapabilities. Per informazioni sull'elemento ParameterDef, vedere [ParameterDef](parameterdef.md). Per informazioni concettuali sulla definizione dei parametri, vedere [elementi ParameterDef e ParameterInit](parameterdef-and-parameterinit-elements.md).

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

La semplice creazione di un'opzione con parametri non è sufficiente per garantire che l'opzione venga gestita ed elaborata correttamente. Il provider PrintCapabilities/PrintTicket e i client devono fornire supporto aggiuntivo per implementare correttamente le istanze di opzioni con parametri. Le sezioni seguenti illustrano i comportamenti richiesti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



