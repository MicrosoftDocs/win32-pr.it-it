---
description: Contiene la classificazione di confidenza restituita da Journal Ink Analyzer per InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Elemento Confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cef4869776a6cafc4e6ef4758649b918e0b5988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128131"
---
# <a name="confidence-element"></a>Elemento Confidence

Contiene la classificazione di confidenza restituita da Journal Ink Analyzer per [**InkWord**](inkword-element.md).

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementi padre

[**InkWord**](inkword-element.md)

## <a name="values"></a>Valori

I valori validi per questo campo sono "0", "1" e "2". 0 indica una confidenza elevata, 1 indica una confidenza intermedia e 2 indica una scarsa confidenza.

## <a name="child-elements"></a>Elementi figlio

Nessuna.

## <a name="attributes"></a>Attributi

Nessuna.

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                            |
|--------------|--------------------------------------------|
| Tipo di elemento | **xs:string**                              |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk |
| Nome schema  | Lettore Journal                             |



 

 

 



