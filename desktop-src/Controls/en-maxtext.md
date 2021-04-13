---
title: Codice di notifica EN_MAXTEXT (winuser. h)
description: Inviato quando l'inserimento di testo corrente supera il numero di caratteri specificato per il controllo di modifica.
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- Controlli di Windows per il codice di notifica EN_MAXTEXT
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518658"
---
# <a name="en_maxtext-notification-code"></a>\_Codice di notifica en MAXTEXT

Inviato quando l'inserimento di testo corrente supera il numero di caratteri specificato per il controllo di modifica. L'inserimento del testo è stato troncato.

Questo codice di notifica viene inviato anche quando un controllo di modifica non ha lo stile [**es \_ AUTOHSCROLL**](edit-control-styles.md) e il numero di caratteri da inserire supera la larghezza del controllo di modifica.

Questo codice di notifica viene inviato anche quando un controllo di modifica non ha lo stile [**es \_ AUTOVSCROLL**](edit-control-styles.md) e il numero totale di righe risultante da un inserimento di testo supera l'altezza del controllo di modifica.

La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_MAXTEXT

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo di modifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

La finestra padre riceve sempre un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) per questo evento, ma non richiede una maschera di notifica inviata con [**em \_ SETEVENTMASK**](em-seteventmask.md).

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

