---
title: Codice di notifica STN_CLICKED (winuser. h)
description: "\\_Quando l'utente fa clic su un controllo statico con stile di notifica SS, viene inviato il codice di notifica con clic su STN \\_ . La finestra padre del controllo riceve questo codice di notifica tramite il \\_ messaggio di comando WM."
ms.assetid: deeac9e9-c23e-4ffb-a1d7-18782efb7a5c
keywords:
- Controlli di Windows per il codice di notifica STN_CLICKED
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
ms.openlocfilehash: 91f63bc496469f6edc26b4f9176f3f9157464bdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873365"
---
# <a name="stn_clicked-notification-code"></a>\_Codice di notifica fatto clic su STN

\_Quando l'utente fa clic su un controllo statico con stile di [**\_ notifica SS**](static-control-styles.md) , viene inviato il codice di notifica con clic su STN. La finestra padre del controllo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
STN_CLICKED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo statico. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo statico.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[\_DBLCLK STN](stn-dblclk.md)
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

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

