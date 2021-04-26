---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: b360f870-bfaa-4d4d-adce-17fcfc48b6a6
title: PageDestinationColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7053cfaf82d7fdfccfe79cebcd76e49befeb125
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996128"
---
# <a name="pagedestinationcolorprofileembedded"></a>PageDestinationColorProfileEmbedded

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica il profilo colori di destinazione incorporato.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto della struttura](#structure-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|----------------------------------------------------------|
| Tipo di elemento <br/>   | ParameterDef<br/>                                  |
| Prefisso di ambito <br/> | Pagina<br/>                                          |
| Note <br/>          | Collegato all'elemento PageDestinationColorProfile<br/> |



 

## <a name="structure-content"></a>Contenuto della struttura

La struttura XML di questo elemento è:

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileEmbedded">
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

 

 




