---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92845b635aa7db1f44394cb6ef76b32292ea0dd4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996138"
---
# <a name="pagedestinationcolorprofile"></a>PageDestinationColorProfile

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Definisce le caratteristiche del profilo colori di destinazione. Descrive se l'applicazione o il driver seleziona il profilo colori di destinazione da utilizzare.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Extensible Markup Language (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo di elemento <br/>   | Caratteristica<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Prefisso di ambito <br/> | Pagina<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Note <br/>          | I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un profilo immagine o colore in un documento di funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (un URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il printTicket risultante. Un consumer XPS conforme NON DEVE utilizzare un URI non conforme alla sintassi del nome della parte. Queste impostazioni sono specifiche di XPS. <br/> Gli URI a cui viene fatto riferimento in un documento di funzionalità di stampa o printTicket NON DEVONO essere risolti come URL. Ciò non è sicuro perché potrebbero non risolversi come previsto e potrebbero creare rischi di sicurezza dannosi per il driver e il sistema operativo.<br/> |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è:

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
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
| \_OptionName\_<br/>          | string<br/> | caratteri<br/> | Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.<br/> | Nome dell'opzione.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | n/d<br/>        | True, False.<br/>                                                                                                                                                               | Definisce un'opzione che, se selezionata, disabilita questa funzionalità.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language (XML) Content

Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi . Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
  <!-- Application specifies the destination profile to be used. -->
  <psf:Option name="psk:Application">
    <!-- Destination profile used to perform color management. -->
    <psf:ScoredProperty name="psk:DestinationColorProfileURI">
      <psf:ParameterRef name="psk:PageDestinationColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DestinationColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageDestinationColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Driver selects the destination profile that best matches its current configuration. -->
  <psf:Option name="psk:DriverConfiguration" />
</psf:Feature>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




