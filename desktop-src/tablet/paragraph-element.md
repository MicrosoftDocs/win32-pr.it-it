---
description: Contiene un paragrafo.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Elemento Paragraph (Windows.ui.xaml.documents.h)
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
ms.openlocfilehash: 2f246294c80814ec809c0a1ca035fcb4741c30c5
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432233"
---
# <a name="paragraph-element"></a>Elemento Paragraph

Contiene un paragrafo.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementi padre

[**Contenuto**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Elementi figlio

[**A linee**](line-element.md)

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="attributes"></a>Attributi



| Attributo       | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**        | **xs:integer**            | Obbligatoria | Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento. | Qualsiasi numero intero.              |
| **Top**         | **xs:integer**            | Obbligatoria | Distanza tra l'origine e il punto in alto nel rettangolo di selezione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**       | **xs:nonNegativeInteger** | Obbligatoria | Larghezza del rettangolo di selezione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza**      | **xs:nonNegativeInteger** | Obbligatoria | Altezza del rettangolo di selezione per l'elemento.                                         | Qualsiasi numero intero non negativo. |
| **BlockNumber** | **xs:nonNegativeInteger** | Obbligatoria | Numero di blocco.                                                                           | Qualsiasi numero intero non negativo. |
| **LineNumber**  | **xs:nonNegativeInteger** | Obbligatoria | Riga in cui inizia il paragrafo.                                                 | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                     |
|--------------|-----------------------------------------------------------------|
| Tipo di elemento | [**complexType ParagraphType**](paragraphtype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                      |
| Nome schema  | Lettore journal                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Windows.ui.xaml.documents.h</dt> </dl> |



 

 




