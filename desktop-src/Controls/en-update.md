---
title: EN_UPDATE codice di notifica (Winuser.h)
description: Inviato quando un controllo di modifica sta per essere ridisegnato.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c126122336fd878dda633620c395cb86c112de1f5dc89e8e25d2c4e08bd93ebd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436430"
---
# <a name="en_update-notification-code"></a>Codice di notifica EN \_ UPDATE

Inviato quando un controllo di modifica sta per essere ridisegnato. Questo codice di notifica viene inviato dopo che il controllo ha formattato il testo, ma prima di visualizzare il testo. In questo modo è possibile ridimensionare la finestra del controllo di modifica, se necessario. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_UPDATE

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

**Rich Edit 1.0:** Per ricevere i \_ codici di notifica EN UPDATE, specificare [**ENM \_ UPDATE**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio EM \_ SETEVENTMASK.**](em-seteventmask.md)

**Rich Edit 2.0 e versioni successive:** Il flag [**ENM \_ UPDATE**](rich-edit-control-event-mask-flags.md) viene ignorato. Il codice di notifica EN \_ UPDATE viene sempre ricevuto. Tuttavia, quando Microsoft Rich Edit 3.0 emula Microsoft Rich Edit 1.0, per ricevere i codici di notifica EN UPDATE è necessario specificare ENM UPDATE nella maschera inviata con il messaggio \_ [**EM \_ SETEVENTMASK.**](em-seteventmask.md) **\_**

Per informazioni sulla compatibilità delle versioni rich edit con le diverse versioni del sistema, vedere [Informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

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

[MODIFICA \_ EN](en-change.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

