---
description: Contiene le informazioni che descrivono il componente verticale delle linee negli elementi decorativi utilizzati dalla nota Journal. Usato, ad esempio, quando la nota contiene linee griglia.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Elemento Vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6f05ab8a2160dbf6b987177957e8285385fe4db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479507"
---
# <a name="vertical-element"></a>Elemento Vertical

Contiene le informazioni che descrivono il componente verticale delle linee negli elementi decorativi utilizzati dalla nota Journal. Usato, ad esempio, quando la nota contiene linee griglia.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementi padre

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Elementi figlio

Nessuno.

## <a name="attributes"></a>Attributi




| Attributo | Type | Obbligatoria | Descrizione | Valori possibili | 
|-----------|------|----------|-------------|-----------------|
| <strong>Style</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>SimpleType LineLayoutStyleType</strong></a> | Obbligatoria | Specifica il tipo di linea da disegnare. | <ul><li>Nessuno</li><li>Tinta unita</li><li>Trattino</li><li>Punto</li><li>DashDot</li><li>DashDotDot</li><li>Double</li></ul> | 
| <strong>Colore</strong> | <a href="colortype-simple-type.md"><strong>SimpleType ColorType</strong></a> | Facoltativo | Colore dell'elemento. | Valore RGB esadecimale. Corrisponde all'espressione regolare seguente: #[0-9a-zA-Z] {6} . Ad esempio, #4a79B5.<br /> | 
| <strong>SpacingBefore</strong> | <strong>xs:nonNegativeInteger</strong> | Facoltativo | Spaziatura prima dell'elemento. | Qualsiasi numero intero non negativo. | 
| <strong>SpacingBetween</strong> | <strong>xs:nonNegativeInteger</strong> | Facoltativo | Spaziatura tra questo elemento e gli elementi circostanti. | Qualsiasi numero intero non negativo. | 




 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                         |
|--------------|---------------------------------------------------------------|
| Tipo di elemento | [**ComplexType VerticalType**](verticaltype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                    |
| Nome schema  | Lettore di journal                                                |



 

 

 




