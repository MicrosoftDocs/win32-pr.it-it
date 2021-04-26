---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d4bfb09a1c3f6f43f11886685a0edfcf2bbd92
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997048"
---
# <a name="documentrollcut"></a>DocumentRollCut

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive il metodo di taglio per la carta a rullo. Ogni documento viene gestito separatamente. Le opzioni specificate descrivono i diversi metodi per il roll cut.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Extensible Markup Language (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|---------------------|
| Tipo di elemento <br/>   | Caratteristica<br/>  |
| Prefisso di ambito <br/> | Documento<br/> |
| Note <br/>          | nessuno<br/>     |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è:

``` syntax
<psf:Feature name="psk:DocumentRollCut">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Variabili di struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Nome                               | Tipo di dati         | Unità                  | Valori supportati                                                                                                                                                                      | Riepilogo                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | caratteri<br/> | Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.<br/> | Nome dell'opzione.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | n/d<br/>        | True, False.<br/>                                                                                                                                                               | Definisce un'opzione che, se selezionata, disabilita questa funzionalità.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language (XML) Content

Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi . Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:

``` syntax
<psf:Feature name="psk:DocumentRollCut">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies cutting method for banner -->
  <psf:Option name="psk:Banner" />
  <!-- Specifies cutting at the edge of the image --> 
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!-- Specifies cutting for media size selected for PageMediaSize -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!-- Specifies no document roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




