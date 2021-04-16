---
title: Codice di notifica LVN_GETINFOTIP (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco icone grande con lo \_ stile esteso LVS ex \_ INFOTIP.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- Controlli di Windows per il codice di notifica LVN_GETINFOTIP
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519326"
---
# <a name="lvn_getinfotip-notification-code"></a>\_Codice di notifica GETINFOTIP di LVN

Inviato da un controllo di visualizzazione elenco icone grande con lo stile esteso [**LVS \_ ex \_ INFOTIP**](extended-list-view-styles.md) . Questo codice di notifica viene inviato quando il controllo elenco-visualizzazione richiede informazioni aggiuntive sul testo da visualizzare in una descrizione comando. Viene inviato sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato solo da controlli di visualizzazione elenco con stile esteso [**LVS \_ ex \_ INFOTIP**](extended-list-view-styles.md) . Il \_ codice di notifica GETINFOTIP di LVN viene inviato solo per l'elemento secondario 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVN \_ GETINFOTIPW** (Unicode) e **LVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





