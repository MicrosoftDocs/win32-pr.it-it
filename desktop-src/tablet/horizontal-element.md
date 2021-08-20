---
description: Contiene informazioni di formattazione per le linee orizzontali utilizzate per gli elementi decorativi in una nota del journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b66e8557d73570ce1a0b7eb7217c02435c51a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482687"
---
# <a name="horizontal-element"></a>Elemento Horizontal

Contiene informazioni di formattazione per le linee orizzontali utilizzate per gli elementi decorativi in una nota del journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
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



|  Elemento     | valore                                                     |
|--------------|-------------------------------------------------------------------|
| Tipo di elemento | [**ComplexType HorizontalType**](horizontaltype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                        |
| Nome schema  | Lettore di journal                                                    |



 

 

 




