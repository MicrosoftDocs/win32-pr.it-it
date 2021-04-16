---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize dell'oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca243defc08b43a79e897bfa91913a954bf37
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104570616"
---
# <a name="pageimageablesize"></a>PageImageableSize dell'oggetto

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive l'area di disegno con immagine per il layout e il rendering. Questa operazione verrà segnalata in base a PageMediaSize e PageOrientation.

I diagrammi seguenti illustrano l'utilizzo delle variabili PageImageableSize dell'oggetto in base a PageOrientation.

![diagramma che mostra le misurazioni di pagina](images/local-1641910626-image.png)

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Contenuto Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento



|                            |                     |
|----------------------------|---------------------|
| Nome                       |                     |
| Tipo di elemento<br/>    | Proprietà<br/> |
| Prefisso ambito <br/> | Pagina<br/>     |
| Note <br/>          | nessuno<br/>     |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è la seguente:

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a>Variabili di struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Nome                                    | Tipo di dati          | Unità               | Valori supportati                       | Riepilogo                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| \_ImageableSizeWidthValue\_<br/>  | numero intero<br/> | micron<br/> | Maggiore di 0.<br/>             | Specifica la dimensione orizzontale della dimensione del supporto dell'applicazione rispetto a PageOrientation.<br/>               |
| \_ImageableSizeHeightValue\_<br/> | numero intero<br/> | micron<br/> | Maggiore di 0.<br/>             | Specifica la dimensione verticale della dimensione del supporto dell'applicazione rispetto a PageOrientation.<br/>                 |
| \_OriginWidthValue\_<br/>         | numero intero<br/> | micron<br/> | Maggiore o uguale a 0.<br/> | Specifica l'origine orizzontale dell'area stampabile rispetto alla dimensione del supporto dell'applicazione.<br/>                   |
| \_OriginHeightValue\_<br/>        | numero intero<br/> | micron<br/> | Maggiore o uguale a 0.<br/> | Specifica l'origine verticale dell'area stampabile rispetto alla dimensione del supporto dell'applicazione.<br/>                     |
| \_ExtentWidthValue\_<br/>         | numero intero<br/> | micron<br/> | Maggiore di 0.<br/>             | Specifica la distanza orizzontale tra l'origine e il limite delimitatore delle dimensioni del supporto dell'applicazione.<br/>      |
| \_ExtentHeightValue\_<br/>        | numero intero<br/> | micron<br/> | Maggiore di 0.<br/>             | Specifica la distanza verticale tra l'origine e il limite delimitatore delle dimensioni del supporto dell'applicazione Canvas.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Contenuto Extensible Markup Language (XML)

Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi. Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




