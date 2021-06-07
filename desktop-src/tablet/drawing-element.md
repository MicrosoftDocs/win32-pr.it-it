---
description: Contiene contenuto classificato dall'analizzatore o dall'utente come disegno.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Elemento Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87c0a3d8879fb5f3146c46c9c88d83a6e658d8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432513"
---
# <a name="drawing-element"></a>Elemento Drawing

Contiene contenuto classificato dall'analizzatore o dall'utente come disegno.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementi padre

[**Contenuto**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Elementi figlio

[**ScalarTransform**](scalartransform-element.md)

[**CanReClassify**](canreclassify-element.md)

[**Classe InkClass**](inkclass-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**   | **xs:integer**            | Obbligatoria | Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento. | Qualsiasi numero intero.              |
| **Top**    | **xs:integer**            | Obbligatoria | Distanza dall'origine al punto più in alto nel rettangolo di selezione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**  | **xs:nonNegativeInteger** | Obbligatoria | Larghezza del rettangolo di selezione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza** | **xs:nonNegativeInteger** | Obbligatoria | Altezza del rettangolo di selezione per l'elemento.                                         | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                     |
|--------------|-------------------------------------------------------------|
| Tipo di elemento | [**ComplexType DrawingType**](drawingtype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Nome schema  | Lettore journal                                              |



 

 

 



