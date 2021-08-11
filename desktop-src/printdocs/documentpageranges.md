---
description: Informazioni sull'elemento DocumentPageRanges, che descrive l'intervallo di output del documento nelle pagine.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9a1941b36970628ddcb5c94cad42bd7f520f0b48e00ff5e1263079818757a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235118"
---
# <a name="documentpageranges"></a>DocumentPageRanges

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive l'intervallo di output del documento nelle pagine. Il valore del parametro deve essere conforme alla struttura seguente:

-   PageRangeText: "*PageRange*" o "*PageRange*,*PageRange*"

-   PageRange: "*PageNumber*" o "*PageNumber* - *PageNumber*"

-   PageNumber: da 1 a N, dove N è il numero di pagine nel documento. Se *PageNumber >* N, *PageNumber* = N.

Gli spazi vuoti nella stringa devono essere ignorati.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|-------------------------|
| Tipo di elemento <br/>   | ParameterDef<br/> |
| Prefisso di ambito <br/> | Documento<br/>     |
| Note <br/>          | nessuno<br/>         |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è:

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Proprietà della struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Proprietà                | xsi:type           | Valore                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:string<br/>       |
| DefaultValue<br/> | string<br/>  | Non definito<br/>       |
| MaxLength<br/>    | numero intero<br/> | Non definito<br/>       |
| Minlength<br/>    | integer<br/> | 1<br/>               |
| Obbligatorio<br/>    | string<br/>  | psk:Conditional<br/> |
| UnitType<br/>     | string<br/>  | caratteri<br/>      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




