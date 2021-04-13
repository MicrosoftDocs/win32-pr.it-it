---
title: Codice di notifica BN_PUSHED (winuser. h)
description: Inviato quando lo stato di push di un pulsante è impostato su push.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- Controlli di Windows per il codice di notifica BN_PUSHED
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18a27599c770eb55d889a21956312512ca804cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340503"
---
# <a name="bn_pushed-notification-code"></a>\_Codice di notifica push di BN

Inviato quando lo stato di push di un pulsante è impostato su push.

> [!Note]  
> Questo codice di notifica viene fornito solo per la compatibilità con le versioni di Windows a 16 bit precedenti alla versione 3,0. Le applicazioni devono utilizzare lo stile del pulsante [**BS \_ OWNERDRAW**](button-styles.md) e la struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) per questa attività.

 

La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_PUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il pulsante.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il \_ push di BN è uguale al codice di notifica [ \_ HILITE di BN](bn-hilite.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BN non \_ push**](bn-unpushed.md)
</dt> </dl>

 

