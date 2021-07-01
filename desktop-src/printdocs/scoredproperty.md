---
description: Trovare informazioni sull'elemento ScoredProperty. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb93fbdaeb6101cbd1ff75d6c0b3a829afe0d317
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119116"
---
# <a name="scoredproperty"></a>ScoredProperty

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ScoredProperty dichiara una proprietà intrinseca a una definizione option. Tali proprietà devono essere confrontate quando si valuta quanto un'opzione richiesta corrisponde a un'opzione supportata dal dispositivo.

## <a name="element-tag"></a>Element Tag

<ScoredProperty>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene l'attributo name di ScoredProperty, una proprietà standard o una proprietà definita privatamente. <br/> |



 

Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere figli di questo elemento ed eventuali restrizioni sull'elemento stesso.



| Categoria                   | Dettagli                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | *Opzione*<br/> *ScoredProperty*<br/>                                                                                                                          |
| Elementi figlio<br/>  | Prima o dopo<br/> *ParameterRef* (uno)<br/> oppure<br/> *Valore* (uno)<br/> *Proprietà* (zero o più)<br/> *ScoredProperty* (zero o più)<br/> |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/>                                                                        |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Un elemento ScoredProperty potrebbe non avere dipendenze di configurazione.

## <a name="example"></a>Esempio

Dichiarare un elemento ScoredProperty denominato MediaSizeWidth con valore 11.

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




