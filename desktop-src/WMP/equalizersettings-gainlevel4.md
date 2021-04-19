---
title: EQUALIZERSETTINGS.gainLevel4
description: L'attributo gainLevel4 specifica o Recupera il livello di guadagno della banda 4.
ms.assetid: 01383171-f991-4d09-858a-ce21ce93e14e
keywords:
- Media Player Windows EQUALIZERSETTINGS. gainLevel4
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea5359a9dae8bac12f89effa8afbeceaef9f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326142"
---
# <a name="equalizersettingsgainlevel4"></a>EQUALIZERSETTINGS.gainLevel4

L'attributo **gainLevel4** specifica o Recupera il livello di guadagno della banda 4.

``` syntax
        elementID.gainLevel4
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore normalmente compreso tra 20 e + 20. Il valore predefinito è zero.

## <a name="remarks"></a>Commenti

Questo attributo regola la parte dello spettro di frequenza audio centrata su 250Hz.

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

 

 





