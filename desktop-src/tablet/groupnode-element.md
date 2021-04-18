---
description: Contiene un set di elementi&\# 8212; Paragraph, InkWord, Drawing, text, image o flag&\# 8212; raggruppati nella nota Journal.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento nodo del gruppo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307485"
---
# <a name="groupnode-element"></a>Elemento nodo del gruppo

Contiene un set di elementi, ovvero [**paragrafi**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md)o [**flag**](flag-element.md), raggruppati nella nota Journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a>Elementi padre

[**Contenuto**](content-element--journal-reader.md)

## <a name="child-elements"></a>Elementi figlio

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Disegno**](drawing-element.md)

[**Text**](text-element.md)

[**Immagine**](docimage-element.md)

[**Contrassegno**](flag-element.md)

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**   | **xs:integer**            | Necessario | Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento. | Qualsiasi numero intero.              |
| **Top**    | **xs:integer**            | Necessario | Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**  | **xs:nonNegativeInteger** | Necessario | Larghezza del rettangolo di delimitazione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza** | **xs:nonNegativeInteger** | Necessario | Altezza del rettangolo di delimitazione per l'elemento.                                         | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| Tipo di elemento | ComplexType [**GroupNodeType**](groupnodetype-complex-type.md) |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk                      |
| Nome schema  | Lettore Journal                                                  |



 

 

 



