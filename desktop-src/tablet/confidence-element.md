---
description: Contiene la classificazione di attendibilità restituita dall'analizzatore input penna journal per InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Elemento Confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fdaaed8d9c57822ad94ec49183a399ed317917
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436501"
---
# <a name="confidence-element"></a>Elemento Confidence

Contiene la classificazione di attendibilità restituita dall'analizzatore input penna journal per [**InkWord.**](inkword-element.md)

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementi padre

[**Inkword**](inkword-element.md)

## <a name="values"></a>Valori

I valori validi per questo campo includono "0", "1" e "2". 0 indica attendibilità forte, 1 indica attendibilità intermedia e 2 indica attendibilità scarsa.

## <a name="child-elements"></a>Elementi figlio

Nessuno.

## <a name="attributes"></a>Attributi

Nessuno.

## <a name="element-information"></a>Informazioni sull'elemento



|                  | Valore                                      |
|------------------|--------------------------------------------|
| **Tipo di elemento** | xs:string                                  |
| **Namespace**    | urn:schemas-microsoft-com:tabletpc:richink |
| **Nome schema**  | Lettore di journal                             |



 

 

 



