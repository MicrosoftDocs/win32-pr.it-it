---
title: EQUALIZERSETTINGS.gainLevel3
description: L'attributo gainLevel3 specifica o Recupera il livello di guadagno della banda 3.
ms.assetid: 508d00c6-2429-4f35-b7ab-bf30f774e614
keywords:
- Media Player Windows EQUALIZERSETTINGS. gainLevel3
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29665777596541f1938360ce057b00c6718d1d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327778"
---
# <a name="equalizersettingsgainlevel3"></a>EQUALIZERSETTINGS.gainLevel3

L'attributo **gainLevel3** specifica o Recupera il livello di guadagno della banda 3.

``` syntax
        elementID.gainLevel3
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore normalmente compreso tra 20 e + 20. Il valore predefinito è zero.

## <a name="remarks"></a>Commenti

Questo attributo regola la parte dello spettro di frequenza audio centrata su 125Hz.

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

 

 





