---
title: NM_RELEASEDCAPTURE (visualizzazione elenco) codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco che il controllo sta rilasciando mouse capture. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: a43879d9-1465-4c25-936f-cda9b8b8b465
keywords:
- NM_RELEASEDCAPTURE di notifica (visualizzazione elenco) Windows controlli
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d75717f937c94b4ba19cd78490b0cf9254394dfc7a6766352a9a535ee7405275
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319071"
---
# <a name="nm_releasedcapture-list-view-notification-code"></a>Codice di notifica NM \_ RELEASEDCAPTURE (visualizzazione elenco)

Notifica alla finestra padre di un controllo visualizzazione elenco che il controllo sta rilasciando mouse capture. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il controllo ignora il valore restituito da questo codice di notifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





