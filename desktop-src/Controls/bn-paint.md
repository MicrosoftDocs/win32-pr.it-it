---
title: BN_PAINT di notifica (Winuser.h)
description: Inviato quando deve essere di colore un pulsante.
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- BN_PAINT del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c3a412dac84fb5e65c7feb652588d6f16af0f49a8f61723ba48447dbbb2b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827601"
---
# <a name="bn_paint-notification-code"></a>Codice di notifica \_ BN PAINT

Inviato quando deve essere di colore un pulsante.

> [!Note]  
> Questo codice di notifica viene fornito solo per la compatibilità con le versioni a 16 bit di Windows precedenti alla versione 3.0. Le applicazioni devono usare lo stile del pulsante [**BS \_ OWNERDRAW**](button-styles.md) e la [**struttura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) per questa attività.

 

La finestra padre del pulsante riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_PAINT

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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

