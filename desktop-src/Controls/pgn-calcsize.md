---
title: PGN_CALCSIZE codice di notifica (Commctrl.h)
description: Inviato da un controllo pager per ottenere le dimensioni scorrevoli della finestra contenuta.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- PGN_CALCSIZE codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c2f6da5153457a871918afea60ac1251496454831a09426f16579ac47342406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078875"
---
# <a name="pgn_calcsize-notification-code"></a>Codice di \_ notifica PGN CALCSIZE

Inviato da un controllo pager per ottenere le dimensioni scorrevoli della finestra contenuta. Queste dimensioni vengono usate dal controllo pager per determinare le dimensioni scorrevoli della finestra contenuta. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) che contiene e riceve informazioni sul codice di notifica. Il **membro dwFlag** di questa struttura indica quale dimensione viene calcolata. A seconda del valore **di dwFlag**, è necessario inserire la dimensione desiderata nel membro **iWidth** o **iHeight** di questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





