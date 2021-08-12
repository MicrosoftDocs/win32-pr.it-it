---
title: EQUALIZERSETTINGS.gainLevel4
description: L'attributo gainLevel4 specifica o recupera il livello di guadagno della banda 4.
ms.assetid: 01383171-f991-4d09-858a-ce21ce93e14e
keywords:
- EQUALIZERSETTINGS.gainLevel4 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b1479d1be95895f124c5150d17a281fec5fc95fcbbedd65ca2ce9887678fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578169"
---
# <a name="equalizersettingsgainlevel4"></a>EQUALIZERSETTINGS.gainLevel4

**L'attributo gainLevel4** specifica o recupera il livello di guadagno della banda 4.

``` syntax
        elementID.gainLevel4
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un numero **di** lettura/scrittura (**float**) con un valore in genere compreso tra 20 e +20. Ha un valore predefinito pari a zero.

## <a name="remarks"></a>Commenti

Questo attributo regola la parte dello spettro di frequenza audio centrata su 250Hz.

Se questo attributo non viene specificato, il valore precedente verrà mantenuto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS. gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 





