---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c80611a4e7dbd10f4841fae098578f0a8fdc96
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993888"
---
# <a name="joburi"></a>JobURI

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica un URI (Uniform Resource Identifier) per il documento.

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

La struttura XML di questo elemento è la seguente:

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a>Variabili di struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Nome                       | Tipo di dati         | Unità | Valori supportati | Riepilogo |
|----------------------------|-------------------|------|------------------|---------|
| \_JobURIValue\_<br/> | string<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Extensible Markup Language (XML) Content

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




