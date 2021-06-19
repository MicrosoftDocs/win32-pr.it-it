---
description: Ottenere informazioni sul parametro PageMediaSizePSWidth. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: PageMediaSizePSWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe678107d2a183ee0f0bf6ce290dfe230fa8cc2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395646"
---
# <a name="pagemediasizepswidth"></a>PageMediaSizePSWidth

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica la larghezza della pagina perpendicolare alla direzione di orientamento del feed (Specifica del formato del file di descrizione della stampante PostScript di [riferimento).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)

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
<psf:ParameterDef name="psk:PageMediaSizePSWidth">
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
| Obbligatorio<br/>    | string<br/>  | psk:Condizionale<br/> |
| Multipli<br/>     | integer<br/> | 1<br/>               |
| Tipo di unità<br/>     | string<br/>  | Micron<br/>         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica del formato del file di descrizione della stampante PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




