---
description: Contiene un'alternativa di riconoscimento per InkWord. Le alternative sono ordinate in base all'attendibilità del riconoscimento nell'alternativa, con il valore più alto per primo.
ms.assetid: 6ec78ac9-c10c-4227-bead-5ddfc48ce27e
title: Elemento Alternate (Wingdi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55dfb629aadea988a6aeec1cba1020c8ab47c994
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436606"
---
# <a name="alternate-element"></a>Elemento alternativo

Contiene un'alternativa di riconoscimento per [**un oggetto InkWord.**](inkword-element.md) Le alternative sono ordinate in base all'attendibilità del riconoscimento nell'alternativa, con il valore più alto per primo.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Alternate" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementi padre

[**AlternateList**](alternatelist-element.md)

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



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wingdi.h</dt> </dl> |



 

 




