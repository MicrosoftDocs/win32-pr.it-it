---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161801e56a27e33cdf921cc07c93e59836d4dd90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320869"
---
# <a name="jobname"></a>JobName

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica un nome descrittivo per il processo.

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
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a>Variabili di struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Nome                        | Tipo di dati         | Unità | Valori supportati | Riepilogo |
|-----------------------------|-------------------|------|------------------|---------|
| \_JobNameValue\_<br/> | string<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Contenuto Extensible Markup Language (XML)

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




