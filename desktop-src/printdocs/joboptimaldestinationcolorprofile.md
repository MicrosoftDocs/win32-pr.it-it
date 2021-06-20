---
description: Informazioni sull'elemento JobOptimalDestinationColorProfile che specifica il profilo colori ottimale in base alla configurazione del dispositivo corrente.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7ad2ea269594809b047922ea4f6c99b924e5ae
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408844"
---
# <a name="joboptimaldestinationcolorprofile"></a>JobOptimalDestinationColorProfile

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica il profilo colori ottimale in base alla configurazione del dispositivo corrente.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Extensible Markup Language (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|---------------------|
| Tipo di elemento <br/>   | Proprietà<br/> |
| Prefisso di ambito <br/> | Processo<br/>      |
| Note <br/>          | nessuno<br/>     |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è:

``` syntax
<psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_ProfileValue_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_ProfileDataValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_PathValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a>Variabili di struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Nome                            | Tipo di dati         | Unità           | Valori supportati          | Riepilogo                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| \_ProfileValue\_<br/>     | string<br/> | n/d<br/> | RGB, ICC, CMYK<br/> | Specifica il profilo colori.<br/>        |
| \_PathValue\_<br/>        | string<br/> | n/d<br/> | n/d<br/>            | Specifica il percorso del file del profilo.<br/> |
| \_ProfileDataValue\_<br/> | string<br/> | n/d<br/> | n/d<br/>            | Contiene il contenuto dei dati del profilo.<br/>      |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language (XML) Content

Le parole chiave pubbliche dello schema di stampa sono definite nello spazio https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords dei nomi . Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:

``` syntax
 <psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




