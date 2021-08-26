---
title: EN_IMECHANGE di notifica (Richedit.h)
description: Notifica all'elemento padre di un controllo Rich Edit che lo stato di conversione IME è stato modificato.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4974c4126606b8ed95ffa645778469b6fc897488533b81498347de1c1995e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047681"
---
# <a name="en_imechange-notification-code"></a>Codice \_ di notifica EN IMECHANGE

Notifica all'elemento padre di un controllo Rich Edit che lo stato di conversione IME è stato modificato. Questo codice di notifica è *disponibile solo* per le versioni in lingua asia del sistema operativo. Un controllo Rich Edit invia questo codice di notifica sotto forma di [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo Rich Edit. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica restituisce zero.

## <a name="remarks"></a>Commenti

Per ricevere i codici di notifica EN \_ IMECHANGE, specificare [**ENM \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**EM \_ SETEVENTMASK.**](em-seteventmask.md)

> [!Note]  
> Questo codice di notifica è supportato solo nella versione asia orientale di Rich Edit 1.0. Non è supportato nelle versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

