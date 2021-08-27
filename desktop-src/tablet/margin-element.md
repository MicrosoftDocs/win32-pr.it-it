---
description: Definisce le linee dei margini disegnate nella pagina.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Elemento Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c264c2470d070353d1fd19340a161cf765bc05
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478667"
---
# <a name="margin-element"></a>Elemento Margin

Definisce le linee dei margini disegnate nella pagina.

## <a name="definition"></a>Definizione

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>Elementi padre

Nessuno.

## <a name="child-elements"></a>Elementi figlio

Nessuno..

## <a name="attributes"></a>Attributi




| Attributo | Type | Obbligatoria | Descrizione | Valori possibili | 
|-----------|------|----------|-------------|-----------------|
| <strong>Style</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>SimpleType LineLayoutStyleType</strong></a> | Obbligatoria | Specifica il tipo di linea da disegnare. | <ul><li>Nessuno</li><li>Tinta unita</li><li>Trattino</li><li>Punto</li><li>DashDot</li><li>DashDotDot</li><li>Double</li></ul> | 
| <strong>Colore</strong> | <a href="colortype-simple-type.md"><strong>SimpleType ColorType</strong></a> | Facoltativo | Colore dell'elemento. | Valore RGB esadecimale. Corrisponde all'espressione regolare seguente: #[0-9a-zA-Z] {6} . Ad esempio, #4a79B5.<br /> | 
| <strong>Tipo</strong> | <a href="margintypetype-simple-type.md"><strong>SimpleType MarginTypeType</strong></a> | Facoltativo | Indica il margine sinistro o destro. | <ul><li>Sinistra</li><li>Destra</li></ul> | 
| <strong>Spaziatura</strong> | <strong>xs:nonNegativeInteger</strong> | Facoltativo | Spaziatura tra il bordo della pagina e il margine. | Qualsiasi numero intero non negativo. | 




 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                     |
|--------------|-----------------------------------------------------------|
| Tipo di elemento | [**complexType MarginType**](margintype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                |
| Nome schema  | Lettore journal                                            |



 

 

 




