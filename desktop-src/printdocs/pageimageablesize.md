---
description: Informazioni sull'elemento pageImageableSize configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4e44bc9afe33b87d32b43c93eafc3b6d4ba4b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395306"
---
# <a name="pageimageablesize"></a>PageImageableSize

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive l'area di disegno con immagini per il layout e il rendering. Verrà segnalato in base a PageMediaSize e PageOrientation.

I diagrammi seguenti illustrano l'utilizzo delle variabili PageImageableSize in base a PageOrientation.

![diagramma che mostra le misurazioni della pagina](images/local-1641910626-image.png)

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Extensible Markup Language (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento

| Nome                 | Valore         |
|----------------------|---------------|
| Tipo di elemento<br/>    | Proprietà<br/> |
| Prefisso di ambito <br/> | Pagina<br/>     |
| Note <br/>          | nessuno<br/>     |

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è:

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
| \_ImageableSizeWidthValue\_<br/>  | numero intero<br/> | Micron<br/> | Maggiore di 0.<br/>             | Specifica la dimensione orizzontale delle dimensioni dei supporti dell'applicazione rispetto a PageOrientation.<br/>               |
| \_ImageableSizeHeightValue\_<br/> | numero intero<br/> | Micron<br/> | Maggiore di 0.<br/>             | Specifica la dimensione verticale delle dimensioni dei supporti dell'applicazione rispetto a PageOrientation.<br/>                 |
| \_OriginWidthValue\_<br/>         | numero intero<br/> | Micron<br/> | Maggiore o uguale a 0.<br/> | Specifica l'origine orizzontale dell'area immagine rispetto alle dimensioni del supporto dell'applicazione.<br/>                   |
| \_OriginHeightValue\_<br/>        | numero intero<br/> | Micron<br/> | Maggiore o uguale a 0.<br/> | Specifica l'origine verticale dell'area immagine rispetto alle dimensioni del supporto dell'applicazione.<br/>                     |
| \_ExtentWidthValue\_<br/>         | numero intero<br/> | Micron<br/> | Maggiore di 0.<br/>             | Specifica la distanza orizzontale tra l'origine e il limite di delimitazione delle dimensioni del supporto dell'applicazione.<br/>      |
| \_ExtentHeightValue\_<br/>        | numero intero<br/> | Micron<br/> | Maggiore di 0.<br/>             | Specifica la distanza verticale tra l'origine e il limite di delimitazione delle dimensioni del supporto dell'applicazione canvas.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language (XML) Content

Le parole chiave pubbliche dello schema di stampa sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi . Il contenuto Extensible Markup Language (XML) pubblico per questa parola chiave è definito di seguito:

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

 

 




