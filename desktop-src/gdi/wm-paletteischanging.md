---
description: Il \_ messaggio WM PALETTEISCHANGING informa le applicazioni che un'applicazione sta per realizzare la relativa tavolozza logica.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: Messaggio WM_PALETTEISCHANGING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757877"
---
# <a name="wm_paletteischanging-message"></a>\_Messaggio PALETTEISCHANGING WM

Il messaggio **WM \_ PALETTEISCHANGING** informa le applicazioni che un'applicazione sta per realizzare la relativa tavolozza logica.

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

Handle per la finestra che renderà conto della tavolozza logica.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

L'applicazione che modifica la tavolozza non attende il riconoscimento del messaggio prima di modificare la tavolozza e di inviare il messaggio [**WM \_ PALETTECHANGED**](wm-palettechanged.md) . Di conseguenza, è possibile che la tavolozza sia già stata modificata dal momento in cui un'applicazione riceve il messaggio.

Se l'applicazione ignora o non riesce a elaborare il messaggio e una seconda applicazione ne realizza la tavolozza mentre la prima utilizza gli indici della tavolozza, è possibile che l'utente visualizzi colori imprevisti durante le successive operazioni di disegno.

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

[**\_QUERYNEWPALETTE WM**](wm-querynewpalette.md)
</dt> </dl>

 

 
