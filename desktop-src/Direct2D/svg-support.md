---
title: Supporto per SVG
description: A partire dall'aggiornamento dell'anniversario di Windows 10, Direct2D supporta il rendering di tipi di carattere di colore che contengono strutture di glifi SVG, come descritto nella specifica OpenType (vedere la tabella "SVG").
ms.assetid: 5cb4cb7c-9b96-e110-bff9-d75ad1980010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678c5d9ef42a53c854bb2f175fac63816345c519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399071"
---
# <a name="svg-support"></a>Supporto per SVG

A partire dall'aggiornamento dell'anniversario di Windows 10, Direct2D supporta il rendering di [tipi di carattere di colore](../directwrite/color-fonts.md) che contengono strutture di glifi SVG, come descritto nella [specifica OpenType](/typography/opentype/spec/) (vedere [la tabella SVG](/typography/opentype/spec/svg)). A partire da Windows 10 Creators Update, Direct2D supporta anche il rendering di immagini SVG autonome. Tuttavia, alcune funzionalità SVG non sono consentite nei tipi di carattere SVG OpenType e alcune funzionalità SVG non sono attualmente supportate da Direct2D.  

Questo argomento identifica il set di funzionalità [SVG 1,1](https://www.w3.org/TR/SVG11/) supportate da Direct2D nell'aggiornamento dell'anniversario di Windows 10 e versioni successive. Questo documento si applica a SVG in tipi di carattere OpenType e a immagini SVG autonome.

## <a name="supported-svg-elements-and-attributes"></a>Attributi e elementi SVG supportati

Direct2D supporta il rendering degli elementi SVG seguenti e degli attributi associati per ogni elemento. Gli altri elementi e gli attributi regolari vengono ignorati.



| Elemento                                                                                  | Attributi regolari supportati                                                             |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [cerchio](https://www.w3.org/TR/SVG11/shapes.mdl#circleelement)                           | ID, stile, trasformazione, CX, CY, r                                                          |
| [clipPath](https://www.w3.org/TR/SVG11/masking.mdl#clippathelement)                      | ID, stile, trasformazione, clipPathUnits                                                      |
| [defs](https://www.w3.org/TR/SVG11/struct.mdl#defselement)                               | ID, stile, trasformazione                                                                     |
| [DESC](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup>  | id                                                                                       |
| [ellisse](https://www.w3.org/TR/SVG11/shapes.mdl#ellipseelement)                         | ID, stile, trasformazione, CX, CY, RX, Ry                                                     |
| [g](https://www.w3.org/TR/SVG11/struct.mdl#gelement)                                     | ID, stile, trasformazione                                                                     |
| [image](https://www.w3.org/TR/SVG11/struct.mdl#imageelement)                             | ID, stile, trasformazione, x, y, larghezza, altezza, preserveAspectRatio, xlink: href               |
| [linea](https://www.w3.org/TR/SVG11/shapes.mdl#lineelement)                               | ID, stile, trasformazione, x1, Y1, X2, Y2                                                     |
| [linearGradient](https://www.w3.org/TR/SVG11/pservers.mdl#lineargradientelement)         | ID, Style, x1, Y1, X2, Y2, gradientUnits, gradientTransform, spreadMethod, xlink: href    |
| [path](https://www.w3.org/TR/SVG11/paths.mdl#pathelement)                                | ID, stile, trasformazione, d                                                                  |
| [poligono](https://www.w3.org/TR/SVG11/shapes.mdl#polygonelement)                         | ID, stile, trasformazione, punti                                                             |
| [polilinea](https://www.w3.org/TR/SVG11/shapes.mdl#polylineelement)                       | ID, stile, trasformazione, punti                                                             |
| [radialGradient](https://www.w3.org/TR/SVG11/pservers.mdl#radialgradientelement)         | ID, Style, CX, CY, r, FX, FY, gradientUnits, gradientTransform, spreadMethod, xlink: href |
| [Rect](https://www.w3.org/TR/SVG11/shapes.mdl#rectelement)                               | ID, stile, trasformazione, x, y, larghezza, altezza, RX, Ry                                        |
| [stop](https://www.w3.org/TR/SVG11/pservers.mdl#stopelement)                             | ID, stile, offset                                                                        |
| [svg](https://www.w3.org/TR/SVG11/struct.mdl#svgelement)                                 | ID, stile, x, y, larghezza, altezza, viewBox, preserveAspectRatio                             |
| [titolo](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup> | id                                                                                       |
| [use](https://www.w3.org/TR/SVG11/struct.mdl#useelement)                                 | ID, stile, trasformazione, x, y, larghezza, altezza, xlink: href                                    |



 

<sup>\*</sup> Supportato solo in Windows 10 Creators Update e versioni successive

## <a name="supported-svg-presentation-attributes"></a>Attributi di presentazione SVG supportati

Direct2D supporta inoltre i seguenti attributi di presentazione. Questi possono essere specificati in qualsiasi elemento SVG, ma influiscono solo sull'aspetto di determinati elementi, come descritto nella specifica SVG (vedere [attributi di presentazione](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)).

-   clip-percorso
-   regola di ritaglio
-   color
-   visualizzare<sup>\*</sup>
-   fill
-   opacità riempimento
-   regola di riempimento
-   opacità
-   overflow
-   Stop-colore
-   Stop-opacità
-   stroke
-   Stroke-dashArray
-   Stroke-DashOffset
-   Stroke-estremità
-   Stroke-LineJoin
-   Stroke-MiterLimit
-   tratto-opacità
-   Lunghezza tratto
-   visibilità<sup>\*</sup>

<sup>\*</sup> Supportato solo in Windows 10 Creators Update e versioni successive

## <a name="unsupported-svg-features"></a>Funzionalità SVG non supportate

### <a name="unsupported-elements-and-attributes"></a>Elementi e attributi non supportati

Qualsiasi elemento o attributo non incluso negli elenchi precedenti viene considerato non supportato da Direct2D. Quando si analizza il contenuto SVG che contiene un elemento o un attributo non supportato, l'entità non supportata viene ignorata. Il resto del contenuto viene sottoposto a rendering nel modo più fedele possibile.

### <a name="unsupported-length-units"></a>Unità di lunghezza non supportate

A partire dall'aggiornamento dell'anniversario di Windows 10, Direct2D supporta solo i valori della lunghezza dello spazio utente e la percentuale di lunghezza. Le lunghezze con suffissi di unità, come "mm" o "em", non sono supportate.

A partire da Windows 10 Fall Creators Update, Direct2D supporta anche gli identificatori di unità assoluti: px, PT, PC, cm, mm e in. Gli identificatori di unità relative (em, ex) non sono supportati.

### <a name="unsupported-image-sources"></a>Origini immagini non supportate

L'elemento Image è supportato solo se l'attributo xlink: href è impostato su un'immagine con codifica Base64. I riferimenti remoti non sono supportati.

 

 