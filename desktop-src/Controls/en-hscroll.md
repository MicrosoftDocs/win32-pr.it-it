---
title: EN_HSCROLL codice di notifica (Winuser.h)
description: Inviato quando l'utente fa clic sulla barra di scorrimento orizzontale di un controllo di modifica. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio WM \_ COMMAND. La finestra padre viene notificata prima dell'aggiornamento della schermata.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- EN_HSCROLL codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e5b0f42d08977f7a1be68a5010aa7403b10fc2e5a126aa542bb25a644a7b70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436771"
---
# <a name="en_hscroll-notification-code"></a>Codice \_ di notifica HSCROLL EN

Inviato quando l'utente fa clic sulla barra di scorrimento orizzontale di un controllo di modifica. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) La finestra padre viene notificata prima dell'aggiornamento della schermata.


```C++
EN_HSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica. HIWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo di modifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato per gli eventi del mouse seguenti sulla barra di scorrimento orizzontale: facendo clic su un pulsante freccia o facendo clic tra il pulsante freccia e il cursore. Tuttavia, il codice di notifica non viene inviato quando si fa clic sul cursore della barra di scorrimento. Il codice di notifica viene inviato anche quando un evento della tastiera provoca una modifica nell'area di visualizzazione del controllo di modifica, ad esempio premendo HOME, FINE, FRECCIA SINISTRA o FRECCIA DESTRA.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per ricevere **i codici di notifica EN \_ HSCROLL,** specificare [**ENM \_ SCROLL**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio EM \_ SETEVENTMASK.**](em-seteventmask.md) Per informazioni sulla compatibilità delle versioni rich edit con le diverse versioni del sistema, vedere [Informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[EN \_ VSCROLL](en-vscroll.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

