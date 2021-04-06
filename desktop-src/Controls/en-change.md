---
title: Codice di notifica EN_CHANGE (winuser. h)
description: Inviato quando l'utente ha effettuato un'azione che potrebbe aver modificato il testo in un controllo di modifica.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- Controlli di Windows per il codice di notifica EN_CHANGE
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ef26d1ec4f8ec1dc93e54d46b88c4fe7cc872b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873585"
---
# <a name="en_change-notification-code"></a>\_Modifica del codice di notifica

Inviato quando l'utente ha effettuato un'azione che potrebbe aver modificato il testo in un controllo di modifica. A differenza del codice di notifica di [ \_ aggiornamento en](en-update.md) , questo codice di notifica viene inviato dopo l'aggiornamento dello schermo da parte del sistema. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_CHANGE

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

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per ricevere \_ i codici di notifica delle modifiche, specificare la [**\_ modifica ENM**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) . Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

Il \_ codice di notifica delle modifiche it non viene inviato quando si usa lo stile [**\_ multiriga es**](edit-control-styles.md) e il testo viene inviato tramite il testo [**WM \_**](/windows/desktop/winmsg/wm-settext).

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

[\_aggiornamento en](en-update.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

