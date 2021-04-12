---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563ed1746743d3329e0cd31c84c32bb8b407c56c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351806"
---
# <a name="documentpageranges"></a>DocumentPageRanges

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive l'intervallo di output del documento in pagine. Il valore del parametro deve essere conforme alla struttura seguente:

-   PageRangeText: "*PageRange*" o "*PageRange*,*PageRange*"

-   PageRange: "*pageNumber*" o "*pageNumber* - *pageNumber*"

-   PageNumber: da 1 a N, dove N è il numero di pagine nel documento. Se *pagenumber* > n, *pageNumber* = N.

Gli spazi vuoti nella stringa devono essere ignorati.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome                       |                         |
|----------------------------|-------------------------|
| Tipo di elemento <br/>   | ParameterDef<br/> |
| Prefisso ambito <br/> | Documento<br/>     |
| Note <br/>          | nessuno<br/>         |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è la seguente:

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

## <a name="structure-properties"></a>Proprietà struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Proprietà                | xsi:type           | Valore                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:string<br/>       |
| DefaultValue<br/> | string<br/>  | Non definito<br/>       |
| MaxLength<br/>    | numero intero<br/> | Non definito<br/>       |
| MinLength<br/>    | integer<br/> | 1<br/>               |
| Obbligatorio<br/>    | string<br/>  | PSK: condizionale<br/> |
| UnitType<br/>     | string<br/>  | caratteri<br/>      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




