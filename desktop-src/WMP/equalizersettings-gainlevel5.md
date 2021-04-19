---
title: EQUALIZERSETTINGS.gainLevel5
description: L'attributo gainLevel5 specifica o Recupera il livello di guadagno della banda 5.
ms.assetid: 6077a4dc-b9b8-4e00-8b29-14afe5a44321
keywords:
- Media Player Windows EQUALIZERSETTINGS. gainLevel5
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel5
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b68e3567b4064a650a9f69cc4608e2b69600cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326141"
---
# <a name="equalizersettingsgainlevel5"></a>EQUALIZERSETTINGS.gainLevel5

L'attributo **gainLevel5** specifica o Recupera il livello di guadagno della banda 5.

``` syntax
        elementID.gainLevel5
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore normalmente compreso tra 20 e + 20. Il valore predefinito è zero.

## <a name="remarks"></a>Commenti

Questo attributo regola la parte dello spettro di frequenza audio centrata su 500Hz.

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

 

 





