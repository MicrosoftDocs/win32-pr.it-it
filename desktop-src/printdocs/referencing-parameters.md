---
description: Informazioni sul riferimento ai parametri e all'elemento ParameterDef. Un esempio di opzione che include un elemento ParameterRef è l'opzione delle dimensioni del supporto personalizzato.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Riferimento ai parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650790af5ca6849bd082b4819dd4c411adea320f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405324"
---
# <a name="referencing-parameters"></a>Riferimento ai parametri

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un esempio concreto di un'opzione che include un elemento ParameterRef è l'opzione delle dimensioni del supporto personalizzato. Si noti che fa riferimento a due parametri: PageMediaSizeMediaSizeWidth e PageMediaSizeMediaSizeHeight. Ogni istanza ParameterRef fa riferimento a un'istanza ParameterDef definita altrove nel documento PrintCapabilities. Per informazioni sull'elemento ParameterDef, vedere [ParameterDef](parameterdef.md). Per informazioni concettuali sulla definizione dei parametri, vedere [Elementi ParameterDef e ParameterInit](parameterdef-and-parameterinit-elements.md).

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

La semplice creazione di un'opzione con parametri non è sufficiente per garantire che l'opzione venga gestita ed elaborata correttamente. I client e il provider PrintCapabilities/PrintTicket devono fornire supporto aggiuntivo per implementare correttamente istanze Option con parametri. I comportamenti necessari sono descritti nelle sezioni seguenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



