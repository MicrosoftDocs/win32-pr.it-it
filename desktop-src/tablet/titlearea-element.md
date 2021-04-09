---
description: Contiene la posizione e le informazioni di delimitazione per il titolo della nota, se presente.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Elemento elemento titlearea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c009d817af9679edda618dd0262c7cbb85a612ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968515"
---
# <a name="titlearea-element"></a>Elemento elemento titlearea

Contiene la posizione e le informazioni di delimitazione per il titolo della nota, se presente.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementi padre

[**Titolo**](title-element.md)

## <a name="child-elements"></a>Elementi figlio

Nessuna.

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
| Tipo di elemento | ComplexType [**TitleAreaType**](titleareatype-complex-type.md) |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk                      |
| Nome schema  | Lettore Journal                                                  |



 

 

 



