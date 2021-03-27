---
description: Il \_ messaggio WM QUERYNEWPALETTE informa una finestra che sta per ricevere lo stato attivo della tastiera, offrendo alla finestra la possibilità di realizzare la propria tavolozza logica quando riceve lo stato attivo.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: Messaggio WM_QUERYNEWPALETTE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979354"
---
# <a name="wm_querynewpalette-message"></a>\_Messaggio QUERYNEWPALETTE WM

Il messaggio **WM \_ QUERYNEWPALETTE** informa una finestra che sta per ricevere lo stato attivo della tastiera, offrendo alla finestra la possibilità di realizzare la propria tavolozza logica quando riceve lo stato attivo.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la finestra comprende la tavolozza logica, deve restituire **true**; in caso contrario, deve restituire **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica sui colori](colors.md)
</dt> <dt>

[Messaggi colori](color-messages.md)
</dt> <dt>

[**\_PALETTECHANGED WM**](wm-palettechanged.md)
</dt> <dt>

[**\_PALETTEISCHANGING WM**](wm-paletteischanging.md)
</dt> </dl>

 

 
