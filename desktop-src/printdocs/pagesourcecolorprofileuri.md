---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 25c3c70f-20e3-4e44-9c59-bb66b4bd14d9
title: PageSourceColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b3f2396fe3a886ed797392a3e1fd9f3c6d0170
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104058491"
---
# <a name="pagesourcecolorprofileuri"></a>PageSourceColorProfileURI

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica l'origine per il profilo colori.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto della struttura](#structure-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome                       |                                                     |
|----------------------------|-----------------------------------------------------|
| Tipo di elemento <br/>   | ParameterDef<br/>                             |
| Prefisso ambito <br/> | Pagina<br/>                                     |
| Note <br/>          | Collegato a elemento PageSourceColorProfile<br/> |



 

## <a name="structure-content"></a>Contenuto della struttura

La struttura XML di questo elemento è la seguente:

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileURI">
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

 

 




