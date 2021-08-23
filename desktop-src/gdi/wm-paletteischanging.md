---
description: Il messaggio WM \_ PALETTEISCHANGING informa le applicazioni che un'applicazione sta per realizzare il riquadro logico.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: WM_PALETTEISCHANGING messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b0de17e7957e4b03c0a8fb942e7c0e4f94a3329e53cb039ce1d7f0a8c33aa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717681"
---
# <a name="wm_paletteischanging-message"></a>Messaggio \_ WM PALETTEISCHANGING

Il **messaggio WM \_ PALETTEISCHANGING** informa le applicazioni che un'applicazione sta per realizzare il riquadro logico.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Handle per la finestra che sta per realizzare il riquadro logico.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

L'applicazione che modifica il riquadro non attende il riconoscimento di questo messaggio prima di modificare il riquadro e inviare il [**messaggio WM \_ PALETTECHANGED.**](wm-palettechanged.md) Di conseguenza, il riquadro potrebbe essere già stato modificato nel momento in cui un'applicazione riceve questo messaggio.

Se l'applicazione ignora o non riesce a elaborare questo messaggio e una seconda applicazione rileva la tavolozza mentre la prima usa gli indici della tavolozza, è possibile che l'utente veda colori imprevisti durante le operazioni di disegno successive.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica dei colori](colors.md)
</dt> <dt>

[Messaggi a colori](color-messages.md)
</dt> <dt>

[**WM \_ PALETTECHANGED**](wm-palettechanged.md)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md)
</dt> </dl>

 

 
