---
title: BN_UNHILITE di notifica (Winuser.h)
description: Inviato quando l'evidenziazione deve essere rimossa da un pulsante.
ms.assetid: 9839a55b-9e9c-4c9c-8e92-347007ea27be
keywords:
- BN_UNHILITE del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- BN_UNHILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d182baaa33ec3b3cc9dc905a7f65d71b8461265c406b28b0c6a0d5f9b59d12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827581"
---
# <a name="bn_unhilite-notification-code"></a>Codice di \_ notifica UNHILITE BN

Inviato quando l'evidenziazione deve essere rimossa da un pulsante.

> [!Note]  
> Questo codice di notifica viene fornito solo per la compatibilità con le versioni a 16 bit Windows precedente alla versione 3.0. Le applicazioni devono usare lo stile del pulsante [**BS \_ OWNERDRAW**](button-styles.md) e la [**struttura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) per questa attività.

 

La finestra padre del pulsante riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_UNHILITE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante. HIWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il pulsante.

</dd> </dl>

## <a name="remarks"></a>Commenti

BN \_ UNHILITE è uguale al codice di notifica [BN \_ UNPUSHED.](bn-unpushed.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

