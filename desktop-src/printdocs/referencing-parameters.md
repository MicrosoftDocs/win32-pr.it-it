---
description: Informazioni sui parametri di riferimento e sull'elemento ParameterDef. Un esempio di opzione che include un elemento ParameterRef è l'opzione delle dimensioni del supporto personalizzate.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Parametri di riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def14223c2d1a4471582e28881a3784eb86239e8daec0e9ec63bff8bc8b7838a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112141"
---
# <a name="referencing-parameters"></a>Parametri di riferimento

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un esempio concreto di option che include un elemento ParameterRef è l'opzione delle dimensioni del supporto personalizzate. Si noti che fa riferimento a due parametri: PageMediaSizeMediaSizeWidth e PageMediaSizeMediaSizeHeight. Ogni istanza ParameterRef fa riferimento a un'istanza ParameterDef definita altrove nel documento PrintCapabilities. Per informazioni sull'elemento ParameterDef, vedere [ParameterDef.](parameterdef.md) Per informazioni concettuali sulla definizione dei parametri, vedere [Elementi ParameterDef e ParameterInit.](parameterdef-and-parameterinit-elements.md)

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

La semplice creazione di un'opzione con parametri non è sufficiente per garantire che l'opzione venga gestita ed elaborata correttamente. Il provider PrintCapabilities/PrintTicket e i client devono fornire supporto aggiuntivo per implementare correttamente le istanze Option con parametri. I comportamenti necessari sono descritti nelle sezioni seguenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



