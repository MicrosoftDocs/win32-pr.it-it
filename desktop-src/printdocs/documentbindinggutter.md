---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2372636ea22610e6a209cfad3f1fe6297be34833
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997188"
---
# <a name="documentbindinggutter"></a>DocumentBindingGutter

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica la larghezza della barra di associazione.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto della struttura](#structure-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|----------------------------------------------|
| Tipo di elemento <br/>   | ParameterDef<br/>                      |
| Prefisso di ambito <br/> | Documento<br/>                          |
| Note <br/>          | Collegato all'elemento DocumentBinding<br/> |



 

## <a name="structure-content"></a>Contenuto della struttura

La struttura XML di questo elemento è:

``` syntax
<psf:ParameterDef name="psk:DocumentBindingGutter">
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
| Obbligatorio<br/>    | Stringa<br/>  | psk:Condizionale<br/> |
| Più elementi<br/>     | integer<br/> | 1<br/>               |
| Tipo di unità<br/>     | string<br/>  | Micron<br/>         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




