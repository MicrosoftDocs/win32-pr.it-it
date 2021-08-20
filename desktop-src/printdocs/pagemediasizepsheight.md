---
description: Ottenere informazioni sul parametro PageMediaSizePSHeight. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: PageMediaSizePSHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53af9494fe895c16fd884e06991b3072f320261e6a47d5fd7f2f06e029bff2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868206"
---
# <a name="pagemediasizepsheight"></a>PageMediaSizePSHeight

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica l'altezza della pagina, parallela alla direzione di orientamento del feed (Riferimento PostScript specifica del formato del file di [descrizione della stampante](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).

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
<psf:ParameterDef name="psk:PageMediaSizePSHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Proprietà della struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Proprietà                | xsi:type           | Valore                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | numero intero<br/> | Non definito<br/>       |
| MaxValue<br/>     | numero intero<br/> | Non definito<br/>       |
| Minvalue<br/>     | numero intero<br/> | Non definito<br/>       |
| Obbligatorio<br/>    | string<br/>  | psk:Conditional<br/> |
| Multipli<br/>     | integer<br/> | 1<br/>               |
| UnitType<br/>     | string<br/>  | Micron<br/>         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[PostScript Specifica del formato del file di descrizione della stampante](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




