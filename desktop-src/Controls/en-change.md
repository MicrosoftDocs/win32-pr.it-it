---
title: EN_CHANGE di notifica (Winuser.h)
description: Inviato quando l'utente ha intrapreso un'azione che potrebbe aver modificato il testo in un controllo di modifica.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- EN_CHANGE del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86dbfb90376a85df09cad854882fa2616e6b7cb247cab4106850608a4b96ad4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437051"
---
# <a name="en_change-notification-code"></a>Codice \_ di notifica EN CHANGE

Inviato quando l'utente ha intrapreso un'azione che potrebbe aver modificato il testo in un controllo di modifica. A differenza [del codice di notifica EN \_ UPDATE,](en-update.md) questo codice di notifica viene inviato dopo l'aggiornamento dello schermo da parte del sistema. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_CHANGE

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

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per ricevere i \_ codici di notifica EN CHANGE, specificare [**ENM \_ CHANGE**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio EM \_ SETEVENTMASK.**](em-seteventmask.md) Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

Il codice di notifica EN CHANGE non viene inviato quando si usa lo stile \_ [**\_ MULTILINE ES**](edit-control-styles.md) e il testo viene inviato tramite [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext).

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

[EN \_ UPDATE](en-update.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

