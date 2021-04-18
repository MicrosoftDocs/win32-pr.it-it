---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 6e7899e3-9b64-48bd-8683-aba627458f2a
title: DocumentID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d41bb96fe904a80210a951f700830604030eadd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320891"
---
# <a name="documentid"></a>DocumentID

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Specifica un ID univoco per il documento.

-   [Informazioni sull'elemento](#element-information)
-   [Contenuto strutturale](#structural-content)
-   [Contenuto Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informazioni sull'elemento



| Nome                       |                     |
|----------------------------|---------------------|
| Tipo di elemento <br/>   | Proprietà<br/> |
| Prefisso ambito <br/> | Documento<br/> |
| Note <br/>          | nessuno<br/>     |



 

## <a name="structural-content"></a>Contenuto strutturale

La struttura XML di questo elemento è la seguente:

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string">_DocumentIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a>Variabili di struttura

Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.



| Nome                           | Tipo di dati         | Unità | Valori supportati | Riepilogo |
|--------------------------------|-------------------|------|------------------|---------|
| \_DocumentIDValue\_<br/> | string<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Contenuto Extensible Markup Language (XML)

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




