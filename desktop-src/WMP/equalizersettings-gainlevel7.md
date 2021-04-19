---
title: EQUALIZERSETTINGS.gainLevel7
description: L'attributo gainLevel7 specifica o Recupera il livello di guadagno della banda 7.
ms.assetid: f39e1475-b0c8-4204-b2d8-943bc8b4f830
keywords:
- Media Player Windows EQUALIZERSETTINGS. gainLevel7
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel7
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5ef5177decd983ae8365090caac5c5bbd510b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326133"
---
# <a name="equalizersettingsgainlevel7"></a>EQUALIZERSETTINGS.gainLevel7

L'attributo **gainLevel7** specifica o Recupera il livello di guadagno della banda 7.

``` syntax
        elementID.gainLevel7
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore normalmente compreso tra 20 e + 20. Il valore predefinito è zero.

## <a name="remarks"></a>Commenti

Questo attributo regola la parte dello spettro di frequenza audio centrata su 2kHz.

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

 

 





