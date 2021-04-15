---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d44dbc63632479c66686cea50b781abf715c76
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104401842"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a>PageBlackGenerationProcessingUnderColorAdditionStart

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive il livello di ombreggiatura al di sotto del quale verrà applicata l'UCA.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto della struttura](#structure-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome                       |                                                            |
|----------------------------|------------------------------------------------------------|
| Tipo di elemento <br/>   | ParameterDef<br/>                                    |
| Prefisso ambito <br/> | Pagina<br/>                                            |
| Note <br/>          | Collegato a elemento PageBlackGenerationProcessing<br/> |



 

## <a name="structure-content"></a>Contenuto della struttura

La struttura XML di questo elemento è la seguente:

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a>Proprietà struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Proprietà                | xsi:type           | Valore                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | string<br/>  | Non definito<br/>       |
| MaxValue<br/>     | numero intero<br/> | 100<br/>             |
| MinValue<br/>     | integer<br/> | 0<br/>               |
| Più elementi<br/>     | integer<br/> | 1<br/>               |
| Obbligatorio<br/>    | string<br/>  | PSK: condizionale<br/> |
| UnitType<br/>     | string<br/>  | percent<br/>         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




