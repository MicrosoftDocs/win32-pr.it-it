---
description: Informazioni su come l'elemento JobCollateAllDocuments descrive le caratteristiche di confronto dell'output. Tutti i documenti in ogni singolo processo vengono fascicolati.
ms.assetid: 64fcd03f-8e0a-498d-82ea-0c69be0a3886
title: JobCollateAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c5e9adc0b6e9682f3c67f1bc8f5ef46c5e272c434968c3c1490e474b7edc0b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971310"
---
# <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive le caratteristiche di confronto dell'output. Tutti i documenti in ogni singolo processo vengono fascicolati. DocumentCollate e JobCollateAlldocuments si escludono a vicenda. Il comportamento e l'implementazione di se vengono implementate entrambe o solo una di queste parole chiave viene lasciata al driver.

Di seguito sono riportate le regole da seguire per l'implementazione di Collate.

## <a name="element-definition-and-rules"></a>Definizione e regole degli elementi

È prima necessario seguire le regole per JobCollateAllDocument e quindi applicare le regole per DocumentCollate per il funzionamento degli scenari. Si noti che in un'impostazione di conversione da PrintTicket a Devmode, in cui JobCollateAllDocuments non è supportata dal driver, è compito del driver scegliere il comportamento appropriato da adottare (JobCollateAllDocuments = ON o OFF). Inoltre, la scelta può essere modificata a seconda delle altre impostazioni di PrintTicket.

### <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

ON: stampare copie (DocumentCopiesAllPages) di ogni documento, ripetere JobCopiesAllDocuments volte.

OFF: per ogni documento, la stampa (JobCopiesAllDocuments x DocumentCopiesAllPages) viene copiata insieme.

### <a name="documentcollate"></a>DocumentCollate

ON: per tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) di un documento stampato in modo contiguo, fascicolare i fogli in tale documento.

OFF: per tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) stampate in modo contiguo, stampare tutte le copie (JobCopiesAllDocuments x DocumentCopiesAllPages) di ogni foglio insieme.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Extensible Markup Language (XML) Content](#extensible-markup-language-xml-content)

### <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|--------------------|
| Tipo di elemento <br/>   | Funzionalità<br/> |
| Prefisso di ambito <br/> | Processo<br/>     |
| Note <br/>          | nessuno<br/>    |



 

### <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è:

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
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

### <a name="structure-variables"></a>Variabili di struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Nome                               | Tipo di dati         | Unità                  | Valori supportati                                                                                                                                                                      | Riepilogo                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | caratteri<br/> | Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.<br/> | Nome dell'opzione.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | n/d<br/>        | True, False.<br/>                                                                                                                                                               | Definisce un'opzione che, se selezionata, disabilita questa funzionalità.<br/> |



 

### <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language (XML) Content

Le parole chiave pubbliche dello schema di stampa sono definite nello spazio https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords dei nomi . Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

 

 




