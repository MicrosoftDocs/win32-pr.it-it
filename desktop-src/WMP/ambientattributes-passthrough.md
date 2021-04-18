---
title: AmbientAttributes. passThrough
description: L'attributo passThrough specifica o recupera un valore che indica se il controllo passerà tutti gli eventi del mouse al controllo sottostante.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- Media Player Windows AmbientAttributes. passThrough
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326029"
---
# <a name="ambientattributespassthrough"></a>AmbientAttributes. passThrough

L'attributo **passThrough** specifica o recupera un valore che indica se il controllo passerà tutti gli eventi del mouse al controllo sottostante.

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                            |
|-------|--------------------------------------------------------|
| true  | Il controllo passa gli eventi al controllo al suo interno. |
| false | Valore predefinito. Il controllo non passa gli eventi tramite.         |



 

## <a name="remarks"></a>Commenti

Questo attributo è utile se, ad esempio, un controllo di testo si trova sopra un controllo Button solo per fornire l'etichettatura. In questo caso, i clic sul controllo di testo devono essere passati al controllo Button.

L'attributo **passThrough** non è supportato dagli elementi **VIEW**, **subview** e **playlist** . Non funzionerà con l'elemento **video** se *video*. senza **finestra** è impostato su false, né con l'elemento **Effects** se *Effects*. **windowed** è impostato su true.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





