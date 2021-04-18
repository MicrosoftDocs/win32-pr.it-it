---
title: EQUALIZERSETTINGS.gainLevel2
description: L'attributo gainLevel2 specifica o Recupera il livello di guadagno della banda 2.
ms.assetid: e602d9cc-42b3-402e-9df5-8b970d878904
keywords:
- Media Player Windows EQUALIZERSETTINGS. gainLevel2
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ca8619f4792b509c5c591c84d547fb7408f747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325252"
---
# <a name="equalizersettingsgainlevel2"></a>EQUALIZERSETTINGS.gainLevel2

L'attributo **gainLevel2** specifica o Recupera il livello di guadagno della banda 2.

``` syntax
        elementID.gainLevel2
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore normalmente compreso tra 20 e + 20. Il valore predefinito è zero.

## <a name="remarks"></a>Commenti

Questo attributo regola la parte dello spettro di frequenza audio centrata su 62Hz.

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

 

 





