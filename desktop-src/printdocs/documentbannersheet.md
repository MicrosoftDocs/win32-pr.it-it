---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac772fdbd9bf378716c42362dc1657a100f1231
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321095"
---
# <a name="documentbannersheet"></a>DocumentBannerSheet

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive il foglio banner da restituire per un documento specifico. Il foglio banner deve essere output sul valore predefinito PageMediaSize, usando il valore predefinito di PageMediaType. Il foglio banner deve anche essere isolato dal resto del documento. Ciò significa che tutte le opzioni di completamento o elaborazione dei documenti, ad esempio DocumentDuplex, DocumentStaple o documento, non devono includere il foglio banner. Il foglio banner potrebbe non essere isolato dal resto del processo. Ciò significa che tutte le opzioni di completamento o elaborazione dei processi possono includere il foglio banner del documento. Il foglio banner dovrebbe essere visualizzato come primo foglio del documento.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo di elemento <br/>   | Funzionalità<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Prefisso ambito <br/> | Documento<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Note <br/>          | I consumer compatibili con XPS devono applicare che un riferimento URI a una risorsa, ad esempio un profilo immagine o colori in un documento sulle funzionalità di stampa o un oggetto PrintTicket, deve fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) nello stesso pacchetto di documento XPS che contiene l'oggetto PrintTicket risultante. Un consumer XPS conforme non deve usare un URI non conforme alla sintassi del nome della parte. Queste impostazioni sono specifiche di XPS. <br/> Gli URI a cui viene fatto riferimento in un documento sulle funzionalità di stampa o in un PrintTicket non devono essere risolti come URL. Questo non è sicuro perché potrebbe non risolversi come previsto e potrebbe creare rischi di sicurezza dannosi per il driver e il sistema operativo.<br/> |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è la seguente:

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a>Variabili di struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Nome                               | Tipo di dati         | Unità                   | Valori supportati                                                                                                                                                                      | Riepilogo                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | caratteri <br/> | Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.<br/> | Nome dell'opzione<br/>                                            |
| \_IdentityOptionValue\_<br/> | string<br/> | n/d<br/>         | True, False<br/>                                                                                                                                                                | Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Contenuto Extensible Markup Language (XML)

Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi. Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a DocumentBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




