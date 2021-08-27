---
title: LVN_MARQUEEBEGIN di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco l'inizio della selezione di un rettangolo di selezione. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8012981883564450603d11d0eb243375f48b46cdb14a14984a19415c84dab3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109531"
---
# <a name="lvn_marqueebegin-notification-code"></a>Codice di notifica \_ LVN MARQUEEBEGIN

Notifica alla finestra padre di un controllo visualizzazione elenco l'inizio della selezione di un rettangolo di selezione. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per accettare il codice di notifica, restituire zero. Per uscire dalla selezione del rettangolo di selezione, restituire un valore diverso da zero.

## <a name="remarks"></a>Commenti

La *selezione di un rettangolo di selezione* è il processo di selezione dell'area client della finestra di visualizzazione elenco e trascinamento per selezionare più elementi contemporaneamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





