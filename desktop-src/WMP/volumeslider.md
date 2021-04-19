---
title: VOLUMESLIDER
description: Si tratta di un dispositivo di scorrimento predefinito con i seguenti valori predefiniti. | VOLUMESLIDER
ms.assetid: 7533863b-49de-4c1b-8750-fd333c573a17
keywords:
- Media Player Windows VOLUMESLIDER
topic_type:
- apiref
api_name:
- VOLUMESLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea872b55f6657d9cf1c9f67230cb3debd955fb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326706"
---
# <a name="volumeslider"></a>VOLUMESLIDER

Si tratta di un dispositivo di scorrimento predefinito con i seguenti valori predefiniti.

``` syntax
toolTip="Volume"
max="100"
min="0"
value="wmpprop:player.settings.volume"
value_onchange="jscript:player.settings.volume=value;
player.settings.mute=false;"
```

## <a name="remarks"></a>Commenti

Viene creato un controllo dispositivo di scorrimento che imposta il volume audio. Le descrizioni comandi sono localizzate. Per eseguire l'override di tutte le proprietà di questo dispositivo di scorrimento, è possibile specificarle in modo esplicito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 7,0 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> </dl>

 

 





