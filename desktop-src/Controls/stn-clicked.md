---
title: STN_CLICKED di notifica (Winuser.h)
description: Il codice di notifica STN CLICKED viene inviato quando l'utente fa clic su un controllo \_ statico con lo stile SS \_ NOTIFY. La finestra padre del controllo riceve questo codice di notifica tramite il messaggio WM \_ COMMAND.
ms.assetid: deeac9e9-c23e-4ffb-a1d7-18782efb7a5c
keywords:
- STN_CLICKED codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- STN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984bbe63444593707de7e410ebd9cb47fb60bac4766ea6ee57660f034e45924d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797871"
---
# <a name="stn_clicked-notification-code"></a>Codice di notifica \_ STN CLICKED

Il codice di notifica STN CLICKED viene inviato quando l'utente fa clic su un controllo \_ statico con lo stile [**SS \_ NOTIFY.**](static-control-styles.md) La finestra padre del controllo riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
STN_CLICKED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo statico. HIWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo statico.

</dd> </dl>

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

[STN \_ DBLCLK](stn-dblclk.md)
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

 

