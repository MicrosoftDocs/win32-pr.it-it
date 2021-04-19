---
title: EQUALIZERSETTINGS.gainLevel10
description: L'attributo gainLevel10 specifica o Recupera il livello di guadagno della banda 10.
ms.assetid: 0d645719-86aa-4475-8e87-ea6c20e4fed7
keywords:
- Media Player Windows EQUALIZERSETTINGS. gainLevel10
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel10
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512819d4c01524e82a92fee9849a9589366a36ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332601"
---
# <a name="equalizersettingsgainlevel10"></a>EQUALIZERSETTINGS.gainLevel10

L'attributo **gainLevel10** specifica o Recupera il livello di guadagno della banda 10.

``` syntax
        elementID.gainLevel10
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore normalmente compreso tra 20 e + 20. Il valore predefinito è zero.

## <a name="remarks"></a>Commenti

Questo attributo regola la parte dello spettro di frequenza audio centrata su 16kHz.

Se questo attributo non viene specificato, il valore precedente verrà mantenuto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS. gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 





