---
title: Supporto SVG
description: A partire da Windows 10 Anniversary Update, Direct2D supporta il rendering dei tipi di carattere a colori contenenti contorni di glifi SVG, come descritto nella specifica OpenType (vedere la tabella 'SVG').
ms.assetid: 5cb4cb7c-9b96-e110-bff9-d75ad1980010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8c5f34531264f95c3617d1324079895b6444cbdbc776d5468fe51fc9890992
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917101"
---
# <a name="svg-support"></a>Supporto SVG

A partire da Windows 10 Anniversary Update, Direct2D supporta il [rendering](../directwrite/color-fonts.md) dei tipi di carattere a colori contenenti contorni del glifo SVG, come descritto nella specifica [OpenType](/typography/opentype/spec/) (vedere la tabella [SVG).](/typography/opentype/spec/svg) A partire Windows 10 Creators Update, Direct2D supporta anche il rendering di immagini SVG autonome. Tuttavia, alcune funzionalità SVG non sono consentite nei tipi di carattere OpenType SVG e alcune funzionalità SVG non sono attualmente supportate da Direct2D.  

Questo argomento identifica il set di [funzionalità SVG 1.1](https://www.w3.org/TR/SVG11/) supportate da Direct2D nell Windows 10'aggiornamento dell'anniversario e versioni più nuove. Questo documento si applica a SVG nei tipi di carattere OpenType e nelle immagini SVG autonome.

## <a name="supported-svg-elements-and-attributes"></a>Attributi e elementi SVG supportati

Direct2D supporta il rendering degli elementi SVG seguenti e degli attributi associati per ogni elemento. Gli altri elementi e gli attributi normali vengono ignorati.



| Elemento                                                                                  | Attributi regolari supportati                                                             |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Cerchio](https://www.w3.org/TR/SVG11/shapes.mdl#circleelement)                           | id, style, transform, cx, cy, r                                                          |
| [clipPath](https://www.w3.org/TR/SVG11/masking.mdl#clippathelement)                      | id, style, transform, clipPathUnits                                                      |
| [defs](https://www.w3.org/TR/SVG11/struct.mdl#defselement)                               | id, style, transform                                                                     |
| [Desc](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup>  | id                                                                                       |
| [Ellisse](https://www.w3.org/TR/SVG11/shapes.mdl#ellipseelement)                         | id, style, transform, cx, cy, rx, ry                                                     |
| [G](https://www.w3.org/TR/SVG11/struct.mdl#gelement)                                     | id, style, transform                                                                     |
| [image](https://www.w3.org/TR/SVG11/struct.mdl#imageelement)                             | id, style, transform, x, y, width, height, preserveAspectRatio, xlink:href               |
| [Linea](https://www.w3.org/TR/SVG11/shapes.mdl#lineelement)                               | id, style, transform, x1, y1, x2, y2                                                     |
| [linearGradient](https://www.w3.org/TR/SVG11/pservers.mdl#lineargradientelement)         | id, style, x1, y1, x2, y2, gradientUnits, gradientTransform, spreadMethod, xlink:href    |
| [path](https://www.w3.org/TR/SVG11/paths.mdl#pathelement)                                | id, style, transform, d                                                                  |
| [Poligono](https://www.w3.org/TR/SVG11/shapes.mdl#polygonelement)                         | id, style, transform, points                                                             |
| [Polilinea](https://www.w3.org/TR/SVG11/shapes.mdl#polylineelement)                       | id, style, transform, points                                                             |
| [radialGradient](https://www.w3.org/TR/SVG11/pservers.mdl#radialgradientelement)         | id, style, cx, cy, r, fx, fy, gradientUnits, gradientTransform, spreadMethod, xlink:href |
| [Rect](https://www.w3.org/TR/SVG11/shapes.mdl#rectelement)                               | id, style, transform, x, y, width, height, rx, ry                                        |
| [stop](https://www.w3.org/TR/SVG11/pservers.mdl#stopelement)                             | id, style, offset                                                                        |
| [svg](https://www.w3.org/TR/SVG11/struct.mdl#svgelement)                                 | id, style, x, y, width, height, viewBox, preserveAspectRatio                             |
| [Titolo](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup> | id                                                                                       |
| [use](https://www.w3.org/TR/SVG11/struct.mdl#useelement)                                 | id, style, transform, x, y, width, height, xlink:href                                    |



 

<sup>\*</sup>Supportato solo in Windows 10 Creators Update e versioni più nuove

## <a name="supported-svg-presentation-attributes"></a>Attributi di presentazione SVG supportati

Direct2D supporta anche i seguenti attributi di presentazione. Questi elementi possono essere specificati in qualsiasi elemento SVG, ma influiscono solo sull'aspetto di determinati elementi, come descritto nella specifica SVG (vedere [Attributi di presentazione).](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)

-   tracciato di ritaglio
-   regola di ritaglio
-   color
-   Visualizzazione<sup>\*</sup>
-   fill
-   opacità di riempimento
-   fill-rule
-   opacità
-   overflow
-   colore di arresto
-   opacità di arresto
-   stroke
-   stroke-dasharray
-   stroke-dashoffset
-   stroke-linecap
-   stroke-linejoin
-   tratto-miterlimit
-   opacità del tratto
-   spessore tratto
-   Visibilità<sup>\*</sup>

<sup>\*</sup>Supportato solo in Windows 10 Creators Update e versioni più nuove

## <a name="unsupported-svg-features"></a>Funzionalità SVG non supportate

### <a name="unsupported-elements-and-attributes"></a>Elementi e attributi non supportati

Qualsiasi elemento o attributo non incluso negli elenchi precedenti viene considerato non supportato da Direct2D. Quando si analizza il contenuto SVG che contiene un elemento o un attributo non supportato, l'entità non supportata viene ignorata. Il rendering del resto del contenuto viene eseguito il più possibile.

### <a name="unsupported-length-units"></a>Unità di lunghezza non supportate

A Windows 10'aggiornamento dell'anniversario, Direct2D supporta solo valori di lunghezza dello spazio utente e valori di lunghezza percentuale. Le lunghezze con suffissi di unità, ad esempio "mm" o "em", non sono supportate.

A partire Windows 10 Fall Creators Update, Direct2D supporta anche identificatori di unità assoluti: px, pt, pc, cm, mm e in. Gli identificatori di unità relativa (em, ex) non sono supportati.

### <a name="unsupported-image-sources"></a>Origini di immagini non supportate

L'elemento image è supportato solo se il relativo attributo xlink:href è impostato su un'immagine con codifica Base64. I riferimenti remoti non sono supportati.

 

 