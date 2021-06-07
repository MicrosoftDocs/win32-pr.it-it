---
description: Contiene un set di elementi&\# 8212; Paragraph, InkWord, Drawing, Text, Image o Flag&\# 8212; raggruppati nella nota Journal.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento GroupNode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc4d39a592b5b6328bd31ff37761cfd3f0138c0
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432572"
---
# <a name="groupnode-element"></a>Elemento GroupNode

Contiene un set di elementi,[**Paragraph,**](paragraph-element.md) [**InkWord,**](inkword-element.md) [**Drawing,**](drawing-element.md) [**Text,**](text-element.md) [**Image**](image-element.md)o [**Flag,**](flag-element.md)raggruppati nella nota Journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a>Elementi padre

[**Contenuto**](content-element--journal-reader.md)

## <a name="child-elements"></a>Elementi figlio

[**Paragraph**](paragraph-element.md)

[**Inkword**](inkword-element.md)

[**Disegno**](drawing-element.md)

[**Text**](text-element.md)

[**Immagine**](docimage-element.md)

[**Bandiera**](flag-element.md)

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**   | **xs:integer**            | Obbligatoria | Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento. | Qualsiasi numero intero.              |
| **Top**    | **xs:integer**            | Obbligatoria | Distanza dall'origine al punto più in alto nel rettangolo di selezione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**  | **xs:nonNegativeInteger** | Obbligatoria | Larghezza del rettangolo di selezione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza** | **xs:nonNegativeInteger** | Obbligatoria | Altezza del rettangolo di selezione per l'elemento.                                         | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                     |
|--------------|-----------------------------------------------------------------|
| Tipo di elemento | [**ComplexType GroupNodeType**](groupnodetype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                      |
| Nome schema  | Lettore journal                                                  |



 

 

 



