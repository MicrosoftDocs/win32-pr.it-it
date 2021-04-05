---
title: Codice di notifica EN_VSCROLL (winuser. h)
description: Inviato quando l'utente fa clic sulla barra di scorrimento verticale di un controllo di modifica o quando l'utente scorre la rotellina del mouse sul controllo di modifica.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- Controlli di Windows per il codice di notifica EN_VSCROLL
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874570"
---
# <a name="en_vscroll-notification-code"></a>\_Codice di notifica en VSCROLL

Inviato quando l'utente fa clic sulla barra di scorrimento verticale di un controllo di modifica o quando l'utente scorre la rotellina del mouse sul controllo di modifica. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) . La finestra padre riceve una notifica prima che lo schermo venga aggiornato.


```C++
EN_VSCROLL

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

Questo messaggio viene inviato per gli eventi del mouse seguenti sulla barra di scorrimento verticale: facendo clic su un pulsante freccia o facendo clic tra il pulsante freccia e il cursore. Tuttavia, il messaggio non viene inviato quando si fa clic sul mouse della barra di scorrimento. Il messaggio viene inviato anche quando un evento della tastiera causa una modifica nell'area di visualizzazione del controllo di modifica, ad esempio, premendo HOME, fine, PGSU, PGGIÙ, freccia su o freccia giù.

La rotellina del mouse è un mouse con una rotellina centrale che scorre. Per ulteriori informazioni, vedere la sezione "rotellina del mouse" in [informazioni sull'input del mouse](/windows/desktop/inputdev/about-mouse-input).

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per ricevere \_ i codici di notifica en VSCROLL, specificare [**ENM \_ Scroll**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) . Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

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

[EN \_ HSCROLL](en-hscroll.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso di controlli di modifica](using-edit-controls.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

