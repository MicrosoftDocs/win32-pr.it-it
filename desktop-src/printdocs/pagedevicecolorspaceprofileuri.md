---
description: Informazioni sul parametro PageDeviceColorSpaceProfileURI. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21420dec2e3057de903b1e04c55a7c6d234343b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396646"
---
# <a name="pagedevicecolorspaceprofileuri"></a>PageDeviceColorSpaceProfileURI

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica un URI relativo alla radice del pacchetto a un profilo ICC contenuto in un documento XPS. L'elaborazione di questa opzione dipende dall'impostazione della funzionalità PageDeviceColorSpaceUsage. Si presuppone che tutti gli elementi che usano tale profilo siano già nello spazio colori del dispositivo appropriato e non saranno gestiti a colori nel driver o nel dispositivo.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto della struttura](#structure-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo di elemento <br/>   | ParameterDef<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Prefisso di ambito <br/> | Pagina<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Note <br/>          | Questo vale solo per i documenti XPS e non deve essere usato in PrintTicket arbitrari.<br/> I consumer conformi a XPS DEVONO imporre che un riferimento URI a una risorsa, ad esempio un'immagine o un profilo colori in un documento di Funzionalità di stampa o PrintTicket MUST, faccia riferimento a un nome di parte (URI relativo alla radice del pacchetto) all'interno dello stesso pacchetto di documenti XPS che contiene il PrintTicket risultante. Un consumer XPS conforme NON DEVE usare un URI non conforme alla sintassi del nome di parte. Queste impostazioni sono specifiche di XPS. <br/> Gli URI a cui viene fatto riferimento in un documento di Funzionalità di stampa o PrintTicket NON DEVONO essere risolti come URL. Questo non è sicuro perché potrebbero non risolversi come previsto e possono creare rischi per la sicurezza dannosi per il driver e il sistema operativo.<br/> |



 

## <a name="structure-content"></a>Contenuto della struttura

La struttura XML di questo elemento è:

``` syntax
<psf:ParameterDef name="psk:PageDeviceColorSpaceProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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
| Obbligatorio<br/>    | string<br/>  | psk:Conditional<br/> |
| UnitType<br/>     | string<br/>  | caratteri<br/>      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




