---
description: Trovare informazioni sull'elemento ScoredProperty. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb600f3fa30c475f7bf28ab1e4c12b19875b6ef49e4f6f3537aead95bf47b999
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033889"
---
# <a name="scoredproperty"></a>ScoredProperty

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ScoredProperty dichiara una proprietà intrinseca a una definizione di opzione. Tali proprietà devono essere confrontate quando si valuta la corrispondenza tra un'opzione richiesta e un'opzione supportata dal dispositivo.

## <a name="element-tag"></a>Tag di elemento

<ScoredProperty>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene l'attributo name di ScoredProperty, una proprietà standard o una proprietà definita privatamente. <br/> |



 

Per altre informazioni, vedere la [sezione Attributi XML.](xml-attributes.md)

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.



| Category                   | Dettagli                                                                                                                                                                  |
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

 

 




