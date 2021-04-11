---
title: Codice di notifica EN_UPDATE (winuser. h)
description: Inviato quando un controllo di modifica sta per essere ridisegnato.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- Controlli di Windows per il codice di notifica EN_UPDATE
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121018"
---
# <a name="en_update-notification-code"></a>\_Codice di notifica dell'aggiornamento en

Inviato quando un controllo di modifica sta per essere ridisegnato. Questo codice di notifica viene inviato dopo che il controllo ha formattato il testo, ma prima di visualizzare il testo. In questo modo è possibile ridimensionare la finestra di controllo di modifica, se necessario. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_UPDATE

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

**Modifica dettagliata 1,0:** Per ricevere \_ i codici di notifica degli aggiornamenti, specificare l' [**\_ aggiornamento di ENM**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

**Rich Edit 2,0 e versioni successive:** Il flag di [**\_ aggiornamento ENM**](rich-edit-control-event-mask-flags.md) viene ignorato. Il \_ codice di notifica dell'aggiornamento it viene sempre ricevuto. Tuttavia, quando Microsoft Rich Edit 3,0 emula Microsoft Rich Edit 1,0, per ricevere \_ i codici di notifica di aggiornamento en, è necessario specificare l' **\_ aggiornamento di ENM** nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

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

[\_modifica en](en-change.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

