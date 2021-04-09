---
title: Codice di notifica EN_IMECHANGE (RichEdit. h)
description: Notifica all'elemento padre di un controllo Rich Edit che lo stato di conversione IME è stato modificato.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- Controlli di Windows per il codice di notifica EN_IMECHANGE
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048397"
---
# <a name="en_imechange-notification-code"></a>\_Codice di notifica en IMECHANGE

Notifica all'elemento padre di un controllo Rich Edit che lo stato di conversione IME è stato modificato. Questo codice di notifica è disponibile *solo* per le versioni in lingua asiatica del sistema operativo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo Rich Edit. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica restituisce zero.

## <a name="remarks"></a>Commenti

Per ricevere \_ i codici di notifica en IMECHANGE, specificare [**ENM \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

> [!Note]  
> Questo codice di notifica è supportato solo nella versione asiatica di Rich Edit 1,0. Non è supportata nelle versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

