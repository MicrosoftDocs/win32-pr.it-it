---
description: Contiene informazioni sulla posizione e sul delimitatore per la nota Titolo, se presente.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Elemento TitleArea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f95c06e6aabe7c73cdc02a7fdb66c60f220adfbe72ea565b73cbc2c3f1a88bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589311"
---
# <a name="titlearea-element"></a>Elemento TitleArea

Contiene informazioni sulla posizione e sul delimitatore per la nota Titolo, se presente.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementi padre

[**Titolo**](title-element.md)

## <a name="child-elements"></a>Elementi figlio

Nessuno.

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**   | **xs:integer**            | Necessario | Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento. | Qualsiasi numero intero.              |
| **Top**    | **xs:integer**            | Necessario | Distanza dall'origine al punto più in alto nel rettangolo di selezione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**  | **xs:nonNegativeInteger** | Necessario | Larghezza del rettangolo di selezione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza** | **xs:nonNegativeInteger** | Necessario | Altezza del rettangolo di selezione per l'elemento.                                         | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|   Elemento    | valore                                                           |
|--------------|-----------------------------------------------------------------|
| Tipo di elemento | [**ComplexType TitleAreaType**](titleareatype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                      |
| Nome schema  | Lettore journal                                                  |



 

 

 



