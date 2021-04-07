---
title: Codice di notifica EN_HSCROLL (winuser. h)
description: Inviato quando l'utente fa clic sulla barra di scorrimento orizzontale di un controllo di modifica. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un \_ messaggio di comando WM. La finestra padre riceve una notifica prima che lo schermo venga aggiornato.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- Controlli di Windows per il codice di notifica EN_HSCROLL
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f90f6e781409419e39390e64251506b4cc915a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874026"
---
# <a name="en_hscroll-notification-code"></a>\_Codice di notifica en HSCROLL

Inviato quando l'utente fa clic sulla barra di scorrimento orizzontale di un controllo di modifica. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) . La finestra padre riceve una notifica prima che lo schermo venga aggiornato.


```C++
EN_HSCROLL

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

Questo codice di notifica viene inviato per gli eventi del mouse seguenti sulla barra di scorrimento orizzontale: facendo clic su un pulsante freccia o facendo clic tra il pulsante freccia e il cursore. Tuttavia, il codice di notifica non viene inviato quando si fa clic sul cursore della barra di scorrimento. Il codice di notifica viene inviato anche quando un evento della tastiera causa una modifica nell'area di visualizzazione del controllo di modifica, ad esempio premendo HOME, fine, freccia sinistra o freccia destra.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per ricevere i codici di notifica **en \_ HSCROLL** , specificare [**ENM \_ Scroll**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) . Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

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

[EN \_ VSCROLL](en-vscroll.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

