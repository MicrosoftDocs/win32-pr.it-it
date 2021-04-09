---
title: Codice di notifica NM_RETURN (visualizzazione elenco) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto INVIO. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 21a8d308-d747-4020-8925-d982234bcf81
keywords:
- Codice di notifica NM_RETURN (visualizzazione elenco) controlli Windows
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b221189ced0e351f088493f00fa7b8849717668
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964644"
---
# <a name="nm_return-list-view-notification-code"></a>\_Codice di notifica restituito da Nm (visualizzazione elenco)

Notifica alla finestra padre di un controllo di visualizzazione elenco che il controllo ha lo stato attivo per l'input e che l'utente ha premuto il tasto INVIO. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





