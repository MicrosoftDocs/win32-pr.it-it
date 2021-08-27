---
title: EN_VSCROLL di notifica (Winuser.h)
description: Inviato quando l'utente fa clic sulla barra di scorrimento verticale di un controllo di modifica o quando l'utente scorre la rotellina del mouse sul controllo di modifica.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c716ecb36c0d27b445446a30eb0a026edf3fd88641f469e50daef1763cd6ca66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047381"
---
# <a name="en_vscroll-notification-code"></a>Codice \_ di notifica EN VSCROLL

Inviato quando l'utente fa clic sulla barra di scorrimento verticale di un controllo di modifica o quando l'utente scorre la rotellina del mouse sul controllo di modifica. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) La finestra padre viene notificata prima dell'aggiornamento della schermata.


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo di modifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato per gli eventi del mouse seguenti sulla barra di scorrimento verticale: facendo clic sul pulsante freccia o facendo clic tra il pulsante freccia e il cursore. Tuttavia, il messaggio non viene inviato quando si fa clic con il mouse sulla barra di scorrimento. Il messaggio viene inviato anche quando un evento della tastiera causa una modifica nell'area di visualizzazione del controllo di modifica, ad esempio premendo HOME, FINE, PGGI SU, PGGI GIÙ, FRECCIA SU o FRECCIA GIÙ.

La rotellina del mouse è un mouse con una rotellina centrale che scorre. Per altre informazioni, vedere "Rotellina del mouse" in [Informazioni sull'input del mouse.](/windows/desktop/inputdev/about-mouse-input)

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per ricevere i codici di notifica EN \_ VSCROLL, specificare [**ENM \_ SCROLL**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio EM \_ SETEVENTMASK.**](em-seteventmask.md) Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[EN \_ HSCROLL](en-hscroll.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso dei controlli di modifica](using-edit-controls.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

