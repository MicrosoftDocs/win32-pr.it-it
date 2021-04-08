---
title: Codice di notifica TVN_GETINFOTIP (COMmctrl. h)
description: Inviato da un controllo di visualizzazione albero con lo \_ stile INFOTIP TV. Questo codice di notifica viene inviato quando il controllo richiede la visualizzazione di informazioni aggiuntive sul testo in una descrizione comando. Il codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- Controlli di Windows per il codice di notifica TVN_GETINFOTIP
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742255"
---
# <a name="tvn_getinfotip-notification-code"></a>\_Codice di notifica GETINFOTIP di TVN

Inviato da un controllo di visualizzazione albero con lo stile [**\_ INFOTIP TV**](tree-view-control-window-styles.md) . Questo codice di notifica viene inviato quando il controllo richiede la visualizzazione di informazioni aggiuntive sul testo in una descrizione comando. Il codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il controllo Ignora il valore restituito per questo codice di notifica.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato solo da controlli di visualizzazione albero con lo [**stile \_ INFOTIP TV**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ GETINFOTIPW** (Unicode) e **TVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





