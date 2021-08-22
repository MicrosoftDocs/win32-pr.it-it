---
title: STN_ENABLE di notifica (Winuser.h)
description: Il codice di notifica \_ STN ENABLE viene inviato quando è abilitato un controllo statico.
ms.assetid: daac2ed3-c7cd-46f8-abfa-78754b277ef4
keywords:
- STN_ENABLE del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- STN_ENABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c1ffea3e3bf4deda67a0ea950ded7e4f16718ace502d16922e50d3750d90bc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642541"
---
# <a name="stn_enable-notification-code"></a>Codice di notifica STN \_ ENABLE

Il codice di notifica \_ STN ENABLE viene inviato quando è abilitato un controllo statico. Per ricevere questo codice di notifica, il controllo statico deve avere lo stile [**\_ SS NOTIFY.**](static-control-styles.md) La finestra padre del controllo riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
STN_ENABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo statico. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo statico.

</dd> </dl>

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

[STN \_ DISABLE](stn-disable.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Controlli statici](static-controls.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

