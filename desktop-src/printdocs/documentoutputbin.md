---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444ca63fee0b76f17909b1aa08e65cd468537dee
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104234599"
---
# <a name="documentoutputbin"></a>DocumentOutputBin

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive l'elenco completo dei cestini supportati per il dispositivo. Consente di specificare il cestino di output in base al documento. Le parole chiave JobOutputBin, DocumentOutputBin e PageOutputBin si escludono a vicenda. è necessario specificare solo un oggetto PrintTicket o un documento sulle funzionalità di stampa.

-   [Informazioni sull'elemento](#element-information)

-   [Contenuto strutturale](#structural-content)

-   [Contenuto XML](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome                       |                     |
|----------------------------|---------------------|
| Tipo di elemento <br/>   | Funzionalità<br/>  |
| Prefisso ambito <br/> | Documento<br/> |
| Note <br/>          | nessuno<br/>     |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è la seguente:

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Variabili di struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Nome                                   | Tipo di dati          | Unità                  | Valori supportati                                                                                                                                                             | Riepilogo                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| \_OptionName\_<br/>              | string<br/>  | caratteri<br/> | Nome completo valido definito da https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname . Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.<br/> | Nome dell'opzione.<br/>                                                  |
| \_IdentityOptionValue\_<br/>     | string<br/>  | n/d<br/>        | True, False.<br/>                                                                                                                                                      | Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.<br/>        |
| \_BinTypeValue\_<br/>            | string<br/>  | n/d<br/>        | MailBox, sorter, Stacker, Finisher, None.<br/>                                                                                                                         | Specifica il tipo generale del cestino.<br/>                                   |
| \_MediaSheetCapacityValue\_<br/> | numero intero<br/> | fogli<br/>     | Maggiore di 0.<br/>                                                                                                                                                   | Specifica la capacità del supporto in numero di pagine (livello completo) del cestino.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Contenuto Extensible Markup Language (XML)

Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi. Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!--Specifies type of output bin-->
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!--Specifies media capacity for output bin-->
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




