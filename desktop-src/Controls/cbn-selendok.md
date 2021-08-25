---
title: CBN_SELENDOK di notifica (Winuser.h)
description: Inviato quando l'utente seleziona un elemento dell'elenco o seleziona un elemento e quindi chiude l'elenco. Indica che la selezione dell'utente deve essere elaborata. La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio WM \_ COMMAND.
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- CBN_SELENDOK codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad6b8a7d8449a646e7b95fd154fb219a9a8087593dcd432da27b9703ebfd28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053991"
---
# <a name="cbn_selendok-notification-code"></a>Codice di notifica \_ CBN SELENDOK

Inviato quando l'utente seleziona un elemento dell'elenco o seleziona un elemento e quindi chiude l'elenco. Indica che la selezione dell'utente deve essere elaborata. La finestra padre della casella combinata riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
CBN_SELENDOK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata. HIWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la casella combinata.

</dd> </dl>

## <a name="remarks"></a>Commenti

In una casella combinata con lo stile [**CBS \_ SIMPLE,**](combo-box-styles.md) il codice di notifica CBN SELENDOK viene inviato immediatamente prima di ogni codice di notifica \_ [CBN \_ SELCHANGE.](cbn-selchange.md)

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

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

[CBN \_ SELENDCANCEL](cbn-selendcancel.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

