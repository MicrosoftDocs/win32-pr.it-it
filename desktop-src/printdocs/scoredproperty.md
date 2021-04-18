---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321038"
---
# <a name="scoredproperty"></a>ScoredProperty

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ScoredProperty dichiara una proprietà intrinseca a una definizione di opzione. È necessario confrontare tali proprietà quando si valuta il modo in cui un'opzione richiesta corrisponde a un'opzione supportata dal dispositivo.

## <a name="element-tag"></a>Tag elemento

<ScoredProperty>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Include l'attributo Name di ScoredProperty, ovvero una proprietà standard o una proprietà definita privatamente. <br/> |



 

Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.



| Category                   | Dettagli                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | *Opzione*<br/> *ScoredProperty*<br/>                                                                                                                          |
| Elementi figlio<br/>  | Prima o dopo<br/> *ParameterRef* (uno)<br/> oppure<br/> *Valore* (uno)<br/> *Property* (zero o più)<br/> *ScoredProperty* (zero o più)<br/> |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/>                                                                        |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Un elemento ScoredProperty non può avere dipendenze di configurazione.

## <a name="example"></a>Esempio

Dichiarare un elemento ScoredProperty denominato MediaSizeWidth con un valore pari a 11.

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




