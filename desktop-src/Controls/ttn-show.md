---
title: Codice di notifica TTN_SHOW (COMmctrl. h)
description: Notifica alla finestra del proprietario che un controllo ToolTip sta per essere visualizzato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- Controlli di Windows per il codice di notifica TTN_SHOW
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acb41d1145c176799dd7997b56a850bb45ece7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964288"
---
# <a name="ttn_show-notification-code"></a>TTN \_ Mostra il codice di notifica

Notifica alla finestra del proprietario che un controllo ToolTip sta per essere visualizzato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

[Versione 4,70](common-control-versions.md). Per visualizzare la descrizione comando nel percorso predefinito, restituire zero. Per personalizzare la posizione della descrizione comando, riposizionare la finestra della descrizione comando con la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) e restituire **true**.

> [!Note]  
> Per le versioni precedenti alla 4,70, non viene restituito alcun valore.

 

## <a name="remarks"></a>Commenti

Un rettangolo della finestra descrizione comando è leggermente più grande del rettangolo di visualizzazione del testo e l'origine viene sfalsata verso l'alto e verso sinistra. Se è necessario posizionare in modo accurato il rettangolo di visualizzazione del testo di una descrizione comando, il messaggio [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) converte un rettangolo di visualizzazione del testo nel rettangolo corrispondente della finestra della descrizione comando e viceversa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

