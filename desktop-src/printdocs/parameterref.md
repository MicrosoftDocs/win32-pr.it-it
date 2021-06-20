---
description: Informazioni sull'elemento ParameterRef, che definisce un riferimento a un elemento ParameterInit e sul suo funzionamento con ScoredProperty.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff3b0e16f53e8399a5bbbb5974a05fd6886cdd2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407184"
---
# <a name="parameterref"></a>ParameterRef

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ParameterRef definisce un riferimento a un elemento ParameterInit. Un elemento ScoredProperty che contiene un elemento ParameterRef non ha un elemento Value impostato in modo esplicito. L'elemento ScoredProperty riceve invece il valore dall'elemento ParameterInit a cui fa riferimento un elemento ParameterRef.

## <a name="element-tag"></a>Element Tag

<ParameterRef>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene l'attributo name dell'elemento ParameterDef a cui viene fatto riferimento nel contesto del documento corrente.<br/> |



 

Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.



| Categoria                   | Dettagli                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | ScoredProperty <br/>                                                                        |
| Elementi figlio<br/>  | Non consentito.<br/>                                                                        |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/> |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Gli elementi ParameterRef potrebbero non avere dipendenze di configurazione.

## <a name="example"></a>Esempio

L'esempio seguente illustra come usare gli elementi ParameterRef per consentire agli utenti di immettere parametri personalizzati per le dimensioni dei supporti.

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




