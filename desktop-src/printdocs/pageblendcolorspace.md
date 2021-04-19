---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf68660929839fad79be26daebf32b9bc0f7ea5
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321132"
---
# <a name="pageblendcolorspace"></a>PageBlendColorSpace

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive lo spazio dei colori da usare per le operazioni di fusione.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Contenuto Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo di elemento <br/>   | Funzionalità<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Prefisso ambito <br/> | Processo<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Note <br/>          | I consumer compatibili con XPS devono applicare che un riferimento URI a una risorsa, ad esempio un profilo immagine o colori in un documento sulle funzionalità di stampa o un oggetto PrintTicket, deve fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) nello stesso pacchetto di documento XPS che contiene l'oggetto PrintTicket risultante. Un consumer XPS conforme non deve usare un URI non conforme alla sintassi del nome della parte. Queste impostazioni sono specifiche di XPS. <br/> Gli URI a cui viene fatto riferimento in un documento sulle funzionalità di stampa o in un PrintTicket non devono essere risolti come URL. Questo non è sicuro perché potrebbe non risolversi come previsto e potrebbe creare rischi di sicurezza dannosi per il driver e il sistema operativo.<br/> |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è la seguente:

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
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
| \_OptionName\_<br/>          | string<br/> | caratteri<br/> | Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.<br/> | Nome dell'opzione.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | n/d<br/>        | True, False.<br/>                                                                                                                                                               | Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Contenuto Extensible Markup Language (XML)

Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi. Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- sRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:sRGB" />
  <!-- scRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:scRGB" />
  <!-- Specifies an ICC profile defining the color space that SHOULD be used for blending.  Note: This applies to XPS Documents only and should not be used in arbitrary PrintTickets. -->
  <psf:Option name="psk:ICCProfile">
    <!-- XPS specific part name for the blend mode ICC Profile -->
    <psf:ScoredProperty name="psk:URI">
      <psf:ParameterRef name="psk:PageBlendColorSpaceICCProfileURI" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




