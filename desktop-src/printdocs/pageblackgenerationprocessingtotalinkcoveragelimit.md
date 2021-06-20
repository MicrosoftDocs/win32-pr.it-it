---
description: Informazioni sull'elemento PageBlackGenerationProcessingTotalInkCoverageLimit, che specifica la somma massima consentita della copertura di quattro input penna in qualsiasi punto di un'immagine.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68410cabdfafa5ce82450821e4ae45709ee8d4c9
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408444"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a>PageBlackGenerationProcessingTotalInkCoverageLimit

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica la somma massima consentita della copertura di quattro input penna in qualsiasi punto di un'immagine.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto della struttura](#structure-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|------------------------------------------------------------|
| Tipo di elemento <br/>   | ParameterDef<br/>                                    |
| Prefisso di ambito <br/> | Pagina<br/>                                            |
| Note <br/>          | Collegato all'elemento PageBlackGenerationProcessing<br/> |



 

## <a name="structure-content"></a>Contenuto della struttura

La struttura XML di questo elemento è:

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">200</psf:Value>
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

## <a name="structure-properties"></a>Proprietà della struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Proprietà                | xsi:type           | Valore                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | string<br/>  | Non definito<br/>       |
| MaxValue<br/>     | numero intero<br/> | 400<br/>             |
| Minvalue<br/>     | numero intero<br/> | 200<br/>             |
| Multipli<br/>     | integer<br/> | 1<br/>               |
| Obbligatorio<br/>    | string<br/>  | psk:Condizionale<br/> |
| Tipo di unità<br/>     | string<br/>  | percent<br/>         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




