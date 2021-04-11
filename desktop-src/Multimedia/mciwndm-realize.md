---
title: Messaggio di MCIWNDM_REALIZE (VFW. h)
description: Il \_ messaggio MCIWNDM realizza la tavolozza attualmente usata dal dispositivo MCI in una finestra di MCIWnd. Questa macro viene definita con il \_ messaggio MCIWNDM realizz. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndRealize.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963825"
---
# <a name="mciwndm_realize-message"></a>MCIWNDM \_ realizzare un messaggio

Il messaggio **MCIWNDM \_ realizza** la tavolozza attualmente usata dal dispositivo MCI in una finestra di MCIWnd. Questa macro viene definita con il messaggio **MCIWNDM \_ realizz** . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*
</dt> <dd>

Flag di sfondo. Specificare **true** per questo parametro se la finestra è un'applicazione in background.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

**MCIWNDM \_ REALIZZARE** usa la tavolozza del dispositivo MCI e chiama la funzione [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) . Se l'applicazione gestisce in modo esplicito i messaggi [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) , è necessario usare questo messaggio nell'applicazione invece di usare **RealizePalette**. Se il corpo di uno di questi gestori di messaggi contiene solo **RealizePalette**, il messaggio viene trasmesso alla finestra MCIWnd, che rende automaticamente disponibile la tavolozza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**\_PALETTECHANGED WM**](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[**\_QUERYNEWPALETTE WM**](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

