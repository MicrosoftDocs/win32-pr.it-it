---
title: EQUALIZERSETTINGS.gainLevel2
description: L'attributo gainLevel2 specifica o recupera il livello di guadagno della banda 2.
ms.assetid: e602d9cc-42b3-402e-9df5-8b970d878904
keywords:
- EQUALIZERSETTINGS.gainLevel2 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe4979cb44fbd39b37acd29fe8e3303c879c45b40dfafc554180dad5301f0b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339831"
---
# <a name="equalizersettingsgainlevel2"></a>EQUALIZERSETTINGS.gainLevel2

**L'attributo gainLevel2** specifica o recupera il livello di guadagno della banda 2.

``` syntax
        elementID.gainLevel2
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un numero **di** lettura/scrittura (**float**) con un valore in genere compreso tra 20 e +20. Ha un valore predefinito pari a zero.

## <a name="remarks"></a>Commenti

Questo attributo regola la parte dello spettro di frequenza audio centrata su 62 Hz.

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

 

 





