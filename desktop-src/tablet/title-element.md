---
description: Contiene informazioni sul titolo della nota journal.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05661be8566cf4136194af4e08d8f9774d3413dc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473137"
---
# <a name="title-element"></a>Elemento Title

Contiene informazioni sul titolo della nota journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementi padre

[**Cancelleria**](stationery-element.md)

## <a name="child-elements"></a>Elementi figlio

[**Area titolo**](titlearea-element.md)

## <a name="attributes"></a>Attributi




| Attributo | Type | Obbligatoria | Descrizione | Valori possibili | 
|-----------|------|----------|-------------|-----------------|
| <strong>Style</strong> | <strong>xs:string</strong> | Obbligatoria | Specifica il tipo di bordo che circonda il titolo della nota. | <ul><li>Nessuno</li><li>SolidSquare</li><li>OutlineSquare</li><li>SolidRoundRect</li><li>OutlineRoundRect</li><li>SolidRoundRectDottedBaseline</li></ul> | 
| <strong>DateStyle</strong> | <strong>xs:string</strong> | Obbligatoria | Definisce se il titolo include o meno una data. | <ul><li>Nessuno</li><li>Short</li></ul> | 
| <strong>Colore</strong> | <a href="colortype-simple-type.md"><strong>SimpleType ColorType</strong></a> | Facoltativo | Specifica il colore dello sfondo. | Vedere <a href="colortype-simple-type.md"><strong>ColorType simpleType.</strong></a> | 




 

## <a name="element-information"></a>Informazioni sull'elemento



| Elemento      | valore                                                   |
|--------------|---------------------------------------------------------|
| Tipo di elemento | [**complexType TitleType**](titletype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink              |
| Nome schema  | Lettore journal                                          |



 

 

 



