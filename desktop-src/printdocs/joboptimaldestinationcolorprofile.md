---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954f67df5720e19de39d2c1c752c6d9eb860a502
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "103969017"
---
# <a name="joboptimaldestinationcolorprofile"></a>JobOptimalDestinationColorProfile

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica il profilo colori ottimale in base alla configurazione corrente del dispositivo.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Contenuto Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome                       |                     |
|----------------------------|---------------------|
| Tipo di elemento <br/>   | Proprietà<br/> |
| Prefisso ambito <br/> | Processo<br/>      |
| Note <br/>          | nessuno<br/>     |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è la seguente:

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
| \_Su pathValue\_<br/>        | string<br/> | n/d<br/> | n/d<br/>            | Specifica il percorso del file del profilo.<br/> |
| \_ProfileDataValue\_<br/> | string<br/> | n/d<br/> | n/d<br/>            | Contiene il contenuto dei dati del profilo.<br/>      |



 

## <a name="extensible-markup-language-xml-content"></a>Contenuto Extensible Markup Language (XML)

Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi. Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:

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

 

 




