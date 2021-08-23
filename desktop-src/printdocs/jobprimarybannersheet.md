---
description: Informazioni sull'elemento JobPrimaryBannerSheet, che descrive il foglio banner da visualizzare come output per il processo.
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e16c3f371a92924dd7d9b5bf9a2746386b615b821d1f58b2e57acd03f9ed11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711821"
---
# <a name="jobprimarybannersheet"></a>JobPrimaryBannerSheet

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive il foglio banner da visualizzare come output per il processo. Il foglio banner deve essere restituito nel valore pageMediaSize predefinito e usando il pageMediaType predefinito. Il foglio del banner deve essere isolato dal resto del processo. Ciò significa che qualsiasi opzione di completamento o elaborazione (ad esempio JobDuplexAllDocumentsContiguously, JobStapleAllDocuments o JobBindAllDocuments) non deve includere il foglio banner. Il foglio banner deve essere il primo foglio del processo.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Extensible Markup Language (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo di elemento <br/>   | Funzionalità<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Prefisso di ambito <br/> | Processo<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Note <br/>          | I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un profilo immagine o colore in un documento di funzionalità di stampa o PrintTicket DEVE fare riferimento a un nome di parte (un URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante. Un consumer XPS conforme NON DEVE utilizzare un URI non conforme alla sintassi del nome della parte. Queste impostazioni sono specifiche di XPS. <br/> Gli URI a cui si fa riferimento in un documento di funzionalità di stampa o printTicket NON DEVONO essere risolti come URL. Ciò non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi di sicurezza dannosi per il driver e il sistema operativo.<br/> |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è:

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the banner sheet. -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
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

Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi . Il contenuto Extensible Markup Language (XML) per questa parola chiave è definito di seguito:

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a JobPrimaryBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored.  -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
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

 

 




