---
description: Contiene un paragrafo.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Elemento Paragraph (Windows.ui.xaml.documents. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: bfe3752541bb54571e9802f557e83dcc7632f845
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324356"
---
# <a name="paragraph-element"></a>Paragraph-elemento

Contiene un paragrafo.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementi padre

[**Contenuto**](content-element--journal-reader.md)

[**Nodo del gruppo**](groupnode-element.md)

## <a name="child-elements"></a>Elementi figlio

[**Linea**](line-element.md)

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="attributes"></a>Attributi



| Attributo       | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**        | **xs:integer**            | Necessario | Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento. | Qualsiasi numero intero.              |
| **Top**         | **xs:integer**            | Necessario | Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**       | **xs:nonNegativeInteger** | Necessario | Larghezza del rettangolo di delimitazione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza**      | **xs:nonNegativeInteger** | Necessario | Altezza del rettangolo di delimitazione per l'elemento.                                         | Qualsiasi numero intero non negativo. |
| **BlockNumber** | **xs:nonNegativeInteger** | Necessario | Numero del blocco.                                                                           | Qualsiasi numero intero non negativo. |
| **LineNumber**  | **xs:nonNegativeInteger** | Necessario | Riga in cui inizia il paragrafo.                                                 | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| Tipo di elemento | ComplexType [**ParagraphType**](paragraphtype-complex-type.md) |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk                      |
| Nome schema  | Lettore Journal                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Windows.ui.xaml.documents. h</dt> </dl> |



 

 




