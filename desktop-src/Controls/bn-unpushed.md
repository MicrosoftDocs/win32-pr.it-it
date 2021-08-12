---
title: BN_UNPUSHED di notifica (Winuser.h)
description: Inviato quando lo stato di push di un pulsante è impostato su unpushed.
ms.assetid: 1ae7311d-f067-41fe-a117-e0c70d239e9d
keywords:
- BN_UNPUSHED del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- BN_UNPUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 418cb2cacc872fd1e1dfcd86778fddf35939c8e022510a4e0df7e00cf7718bc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674115"
---
# <a name="bn_unpushed-notification-code"></a>Codice di \_ notifica UNPUSHED BN

Inviato quando lo stato di push di un pulsante è impostato su unpushed.

> [!Note]  
> Questo codice di notifica viene fornito solo per la compatibilità con le versioni a 16 bit Windows precedente alla versione 3.0. Le applicazioni devono usare lo stile del pulsante [**BS \_ OWNERDRAW**](button-styles.md) e la [**struttura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) per questa attività.

 

La finestra padre del pulsante riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_UNPUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

LoWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) l'identificatore del controllo del pulsante. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il pulsante.

</dd> </dl>

## <a name="remarks"></a>Commenti

BN \_ UNPUSHED corrisponde al codice di notifica [ \_ BN UNHILITE.](bn-unhilite.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PUSH \_ BN](bn-pushed.md)
</dt> </dl>

 

