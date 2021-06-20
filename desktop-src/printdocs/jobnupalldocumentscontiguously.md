---
description: Informazioni sull'elemento JobNUpAllDocumentsContiguously, che descrive l'output di più pagine logiche in un singolo foglio fisico.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9106259c80a7efb89cc4481780bfb55af4f07e23
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408864"
---
# <a name="jobnupalldocumentscontiguously"></a>JobNUpAllDocumentsContiguously

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descrive l'output di più pagine logiche in un singolo foglio fisico. Tutti i documenti nel processo vengono compilati insieme in modo contiguo. JobNUpAllDocumentsContiguously e DocumentNUp si escludono a vicenda. È responsabilità del driver determinare la gestione dei vincoli tra queste parole chiave.

Il diagramma seguente illustra un esempio con il documento 1 contenente 3 pagine e il documento 2 contenente 2 pagine. Ogni documento del processo è duplex in modo contiguo. Le direzioni di presentazione mostrate nell'esempio sono l'opzione RightBottom.

![diagramma che mostra come vengono disposte le pagine del documento in un singolo foglio in base all'impostazione di documentnup](images/local-1242234459-jobduplexpics.gif)

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Extensible Markup Language (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome | Valore |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo di elemento <br/>   | Funzionalità<br/>                                                                                                                             |
| Prefisso di ambito <br/> | Processo<br/>                                                                                                                                 |
| Note <br/>          | Top, Bottom, Left e Right sono relativi a PageImageableSize, dove TopLeft è denotato dall'origine dell'altezza e della larghezza.<br/> |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è:

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Variabili di struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Nome                                           | Tipo di dati          | Unità                     | Valori supportati                                                                                                                                                                      | Riepilogo                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| \_OptionName\_<br/>                      | string<br/>  | caratteri<br/>    | Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.<br/> | Nome dell'opzione.<br/>                                                                                                   |
| \_IdentityOptionValue\_<br/>             | string<br/>  | n/d<br/>           | True, False.<br/>                                                                                                                                                               | Definisce un'opzione che, se selezionata, disabilita questa funzionalità.<br/>                                                         |
| \_PagesPerSheetValue\_<br/>              | numero intero<br/> | Pagine logiche<br/> | Tutti i numeri interi (maggiore di zero).<br/>                                                                                                                                          | Specifica il numero di pagine logiche per foglio fisico. Il set supportato può essere qualsiasi set di numeri interi, ad esempio {1,2,4,6,8,9,16}.<br/> |
| \_PresentationDirectionOptionName\_<br/> | string<br/>  | caratteri<br/>    | Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.<br/> | Nome dell'opzione.<br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language (XML) Content

Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi . Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




