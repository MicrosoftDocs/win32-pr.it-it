---
description: Contiene un'alternativa di riconoscimento per InkWord. Le alternative vengono ordinate in base all'attendibilità del sistema di riconoscimento nell'alternativa, con il valore più alto per primo.
ms.assetid: 6ec78ac9-c10c-4227-bead-5ddfc48ce27e
title: Elemento Alternate (Wingdi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306371c1f2eff41629c115261fecb0d807652a598458be79bbabf8d7c7cc7587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884017"
---
# <a name="alternate-element"></a>Elemento alternativo

Contiene un'alternativa di riconoscimento per [**un oggetto InkWord.**](inkword-element.md) Le alternative vengono ordinate in base all'attendibilità del sistema di riconoscimento nell'alternativa, con il valore più alto per primo.

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
| **Nome schema**  | Lettore journal                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wingdi.h</dt> </dl> |



 

 




