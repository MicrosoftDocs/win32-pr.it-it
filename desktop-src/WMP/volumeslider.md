---
title: VOLUMILIDER
description: Si tratta di un dispositivo di scorrimento predefinito con i valori predefiniti seguenti. | VOLUMILIDER
ms.assetid: 7533863b-49de-4c1b-8750-fd333c573a17
keywords:
- VOLUMILIDER Windows Media Player
topic_type:
- apiref
api_name:
- VOLUMESLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebc2e6ec82327be9cb423d05661a5a38bbcc445450fc6d4f56ceaf7caa8b270d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054009"
---
# <a name="volumeslider"></a>VOLUMILIDER

Si tratta di un dispositivo di scorrimento predefinito con i valori predefiniti seguenti.

``` syntax
toolTip="Volume"
max="100"
min="0"
value="wmpprop:player.settings.volume"
value_onchange="jscript:player.settings.volume=value;
player.settings.mute=false;"
```

## <a name="remarks"></a>Commenti

Verrà creato un controllo SLIDER che imposta il volume audio. Le descrizioni comandi sono localizzate. È possibile eseguire l'override di tutte le proprietà di questo slider specificandole in modo esplicito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 7.0 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> </dl>

 

 





