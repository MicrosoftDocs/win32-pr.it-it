---
title: ICM_DRAW_CHANGEPALETTE messaggio (Vfw.h)
description: Il ICM \_ DRAW \_ CHANGEPALETTE notifica a un driver di rendering che la tavolozza dei film è in fase di modifica. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICDrawChangePalette.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- ICM_DRAW_CHANGEPALETTE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e936c7dce397910ef70a80e2efa7f3e031ab8a61b8f59fece158d5c28e9e1270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987597"
---
# <a name="icm_draw_changepalette-message"></a>\_ICM DRAW \_ CHANGEPALETTE message

Il **ICM \_ DRAW \_ CHANGEPALETTE** notifica a un driver di rendering che la tavolozza dei film è in fase di modifica. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICDrawChangePalette.**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette)


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntatore a una [**struttura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il nuovo formato e la tabella dei colori facoltativa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK in caso di esito positivo o FALSE in **caso** contrario.

## <a name="remarks"></a>Commenti

Questo messaggio deve essere supportato da gestori di rendering installabili che disegnano DIB con una struttura interna che include una tavolozza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

