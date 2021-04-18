---
title: EQUALIZERSETTINGS.gainLevel1
description: L'attributo gainLevel1 specifica o Recupera il livello di guadagno della banda 1.
ms.assetid: 3d681ade-3fd4-432d-ae92-c083d927346f
keywords:
- Media Player Windows EQUALIZERSETTINGS. gainLevel1
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel1
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3299c2b9275eabb4812c83670f28bcbb3d2aeef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330895"
---
# <a name="equalizersettingsgainlevel1"></a>EQUALIZERSETTINGS.gainLevel1

L'attributo **gainLevel1** specifica o Recupera il livello di guadagno della banda 1.

``` syntax
        elementID.gainLevel1
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore normalmente compreso tra 20 e + 20. Il valore predefinito è zero.

## <a name="remarks"></a>Commenti

Questo attributo regola la parte dello spettro di frequenza audio centrata su 31Hz.

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

 

 





