---
title: MCIWNDM_REALIZE messaggio (Vfw.h)
description: Il messaggio MCIWNDM REALIZE rende disponibile la tavolozza attualmente usata dal dispositivo \_ MCI in una finestra MCIWnd. Questa macro viene definita con il messaggio REALIZE \_ MCIWNDM. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndRealize.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE messaggio Windows Multimediali
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
ms.openlocfilehash: 1d3fdbee3757e1fd3aada5292b86cc37577ccb718315c5b81140ceb14278c37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012619"
---
# <a name="mciwndm_realize-message"></a>Messaggio DI MCIWNDM \_ REALIZE

Il **messaggio MCIWNDM \_ REALIZE** rende disponibile la tavolozza attualmente usata dal dispositivo MCI in una finestra MCIWnd. Questa macro viene definita con il **messaggio REALIZE \_ MCIWNDM.** È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndRealize.**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*
</dt> <dd>

Flag di sfondo. Specificare **TRUE** per questo parametro se la finestra è un'applicazione in background.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

**MCIWNDM \_ REALIZE** usa la tavolozza del dispositivo MCI e chiama la [**funzione RealizePalette.**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) Se l'applicazione gestisce in modo esplicito i messaggi [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE,**](/windows/desktop/gdi/wm-querynewpalette) è necessario usare questo messaggio nell'applicazione anziché **RealizePalette.** Se il corpo di uno di questi gestori di messaggi contiene solo **RealizePalette,** inoltrare il messaggio alla finestra MCIWnd, che realizza automaticamente la tavolozza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

