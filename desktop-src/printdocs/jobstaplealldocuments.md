---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: JobStapleAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b3576611dcdc746342b8ed1b2c3d7ebf8fb779
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "103969019"
---
# <a name="jobstaplealldocuments"></a>JobStapleAllDocuments

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive le caratteristiche di graffatura dell'output. Tutti i documenti del processo vengono graffettati insieme. Le parole chiave JobStapleAllDocuments e DocumentStaple si escludono a vicenda. Spetta al driver determinare la gestione dei vincoli tra queste parole chiave.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Contenuto Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome                       |                                                                                |
|----------------------------|--------------------------------------------------------------------------------|
| Tipo di elemento <br/>   | Funzionalità<br/>                                                             |
| Prefisso ambito <br/> | Processo<br/>                                                                 |
| Note <br/>          | Top, Bottom, Left e Right sono relativi a PageImageableSize dell'oggetto <br/> |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è la seguente:

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:Angle" >
      <psf:Value xsi:type="xs:integer">_AngleValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_SheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Variabili di struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Nome                               | Tipo di dati          | Unità                       | Valori supportati                                                                                                                                                                      | Riepilogo                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/>  | Caratteri<br/>      | Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.<br/> | Nome dell'opzione.<br/>                                                                                                                    |
| \_IdentityOptionValue\_<br/> | string<br/>  | n/d<br/>             | True, False.<br/>                                                                                                                                                               | Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.<br/>                                                                          |
| \_AngleValue\_<br/>          | numero intero<br/> | gradi<br/>         | Maggiore di 0.<br/>                                                                                                                                                            | Specifica l'angolo della graffetta, relativo alla larghezza del PageImageableSize dell'oggetto. L'angolo della graffetta viene misurato in senso antiorario.<br/> |
| \_SheetCapacityValue\_<br/>  | numero intero<br/> | fogli di supporti<br/> | Maggiore di 0.<br/>                                                                                                                                                            | Specifica il numero di fogli supportati dall'opzione di pinzatura per il MediaType attualmente selezionato.<br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a>Contenuto Extensible Markup Language (XML)

Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi. Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies saddle stitch stapling -->
  <psf:Option name="psk:SaddleStitch">
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, left corner. -->
  <psf:Option name="psk:StapleBottomLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, right corner. -->
  <psf:Option name="psk:StapleBottomRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the left edge. -->
  <psf:Option name="psk:StapleDualLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the right edge. -->
  <psf:Option name="psk:StapleDualRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the top edge. -->
  <psf:Option name="psk:StapleDualTop">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no stapling. -->
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, left corner. -->
  <psf:Option name="psk:StapleTopLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, right corner. -->
  <psf:Option name="psk:StapleTopRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the bottom edge. -->
  <psf:Option name="psk:StapleDualBottom">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




