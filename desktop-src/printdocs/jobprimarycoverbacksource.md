---
description: Informazioni sull'elemento JobPrimaryCoverBackSource, che specifica l'origine per un foglio principale di copertura posteriore personalizzato per il processo.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ac990caca0f10e03f33eda9971ad967c1c7192ae07a1326675f66880c27857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471683"
---
# <a name="jobprimarycoverbacksource"></a>JobPrimaryCoverBackSource

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica l'origine per un foglio principale di copertura posteriore personalizzato per il processo.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto della struttura](#structure-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|-------------------------------------------|
| Tipo di elemento <br/>   | ParameterDef<br/>                   |
| Prefisso di ambito <br/> | Processo<br/>                            |
| Note <br/>          | Collegato all'elemento JobCoverBack<br/> |



 

## <a name="structure-content"></a>Contenuto della struttura

La struttura XML di questo elemento è:

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverBackSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
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
| Obbligatorio<br/>    | string<br/>  | psk:Condizionale<br/> |
| Tipo di unità<br/>     | string<br/>  | caratteri<br/>      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




