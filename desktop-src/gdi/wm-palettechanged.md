---
description: Il \_ messaggio WM PALETTECHANGED viene inviato a tutte le finestre di primo livello e sovrapposte dopo che la finestra con lo stato attivo della tastiera ha realizzato la relativa tavolozza logica, modificando quindi la tavolozza di sistema.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: Messaggio WM_PALETTECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755823"
---
# <a name="wm_palettechanged-message"></a>\_Messaggio PALETTECHANGED WM

Il messaggio **WM \_ PALETTECHANGED** viene inviato a tutte le finestre di primo livello e sovrapposte dopo che la finestra con lo stato attivo della tastiera ha realizzato la relativa tavolozza logica, modificando quindi la tavolozza di sistema. Questo messaggio consente a una finestra che utilizza una tavolozza dei colori ma non ha lo stato attivo per realizzare la tavolozza logica e aggiornare la relativa area client.

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

Handle per la finestra che ha causato la modifica della tavolozza di sistema.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio deve essere inviato a tutte le finestre di primo livello e sovrapposte, incluso quello che ha modificato la tavolozza di sistema. Se le finestre figlio utilizzano una tavolozza dei colori, è necessario passare anche questo messaggio.

Per evitare la creazione di un ciclo infinito, una finestra che riceve questo messaggio non deve realizzare la propria tavolozza, a meno che il *wParam* non contenga il proprio handle della finestra.

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

[**\_PALETTEISCHANGING WM**](wm-paletteischanging.md)
</dt> <dt>

[**\_QUERYNEWPALETTE WM**](wm-querynewpalette.md)
</dt> </dl>

 

 
