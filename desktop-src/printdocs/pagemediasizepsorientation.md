---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16a9a2e59ebffb41ad7c9a9c16eaf41497ade62
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997558"
---
# <a name="pagemediasizepsorientation"></a>PageMediaSizePSOrientation

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica l'orientamento relativo alla direzione dell'orientamento del feed (Specifica del formato del file di descrizione della stampante [PostScript di riferimento).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto della struttura](#structure-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|-------------------------------------------------------------|
| Tipo di elemento <br/>   | ParameterDef<br/>                                     |
| Prefisso di ambito <br/> | Pagina<br/>                                             |
| Note <br/>          | Collegato all'elemento PageMediaSize, opzione CustomPS<br/> |



 

## <a name="structure-content"></a>Contenuto della struttura

La struttura XML di questo elemento è:

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSOrientation">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">3</psf:Value>
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
    <psf:Value xsi:type="xs:string">PageMediaSizeEnum</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Proprietà della struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Proprietà                | xsi:type           | Valore                        |
|-------------------------|--------------------|------------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>        |
| DefaultValue<br/> | integer<br/> | 0<br/>                 |
| MaxValue<br/>     | numero intero<br/> | 3<br/>                 |
| Minvalue<br/>     | integer<br/> | 0<br/>                 |
| Obbligatorio<br/>    | string<br/>  | psk:Conditional<br/>   |
| Più elementi<br/>     | integer<br/> | 1<br/>                 |
| UnitType<br/>     | string<br/>  | PageMediaSizeEnum<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica del formato del file di descrizione della stampante PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




