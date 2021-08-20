---
description: Il messaggio WM PALETTECHANGED viene inviato a tutte le finestre di primo livello e sovrapposte dopo che la finestra con lo stato attivo della tastiera ha realizzato la tavolozza logica, modificando così la tavolozza \_ di sistema.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: WM_PALETTECHANGED messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb706452e357f2e322b1f4e2618f0fd59c5c4d9a6606c07d18fae7c3b346323e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977921"
---
# <a name="wm_palettechanged-message"></a>Messaggio WM \_ PALETTECHANGED

Il **messaggio WM \_ PALETTECHANGED** viene inviato a tutte le finestre di primo livello e sovrapposte dopo che la finestra con lo stato attivo della tastiera ha realizzato la tavolozza logica, modificando così la tavolozza di sistema. Questo messaggio consente a una finestra che utilizza una tavolozza dei colori, ma non ha lo stato attivo della tastiera, di realizzare la tavolozza logica e aggiornare la relativa area client.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Questo messaggio deve essere inviato a tutte le finestre di primo livello e sovrapposte, inclusa quella che ha modificato la tavolozza di sistema. Se una finestra figlio usa una tavolozza dei colori, anche questo messaggio deve essere passato a tali finestre.

Per evitare la creazione di un ciclo infinito, una finestra che riceve questo messaggio non deve realizzare la tavolozza, a meno che non venga determinato che *wParam* non contiene il proprio handle di finestra.

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

[Messaggi di colore](color-messages.md)
</dt> <dt>

[**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md)
</dt> </dl>

 

 
