---
title: SEEKSLIDER
description: Si tratta di un dispositivo di scorrimento predefinito con i seguenti valori predefiniti. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- Media Player Windows SEEKSLIDER
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325829"
---
# <a name="seekslider"></a>SEEKSLIDER

Si tratta di un **dispositivo di scorrimento** predefinito con i seguenti valori predefiniti.

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a>Commenti

Viene creato un controllo **dispositivo di scorrimento** che cerca il file multimediale in qualsiasi posizione. Le descrizioni comandi sono localizzate. Per eseguire l'override di tutte le proprietà di questo **dispositivo di scorrimento** , è possibile specificarle in modo esplicito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 7,0 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> </dl>

 

 





