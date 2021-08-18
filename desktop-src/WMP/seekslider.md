---
title: SEEKSLIDER
description: Si tratta di un dispositivo di scorrimento predefinito con i valori predefiniti seguenti. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SEEKSLIDER Windows Media Player
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a294eede05ec2b2f0f84e925aa299c9bcb2388ee2151385e48f2c68e6b4c1328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833340"
---
# <a name="seekslider"></a>SEEKSLIDER

Si tratta di un dispositivo **di scorrimento predefinito** con i valori predefiniti seguenti.

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

Verrà creato un **controllo SLIDER** che cerca il file multimediale in qualsiasi posizione. Le descrizioni comandi sono localizzate. È possibile eseguire l'override di tutte le proprietà di **questo slider** specificandole in modo esplicito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 7.0 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> </dl>

 

 





