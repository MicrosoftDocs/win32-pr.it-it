---
title: LVN_COLUMNCLICK di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco che è stato fatto clic su un'intestazione di colonna mentre il controllo visualizzazione elenco era in modalità report. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74cd88674b10a799f58fd0549a6711f3d00934f7b1baaf892cff86c6ef223d19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319811"
---
# <a name="lvn_columnclick-notification-code"></a>Codice di notifica LVN \_ COLUMNCLICK

Notifica alla finestra padre di un controllo visualizzazione elenco che è stato fatto clic su un'intestazione di colonna mentre il controllo visualizzazione elenco era in modalità report. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) Il **membro iItem** è -1 e il **membro iSubItem** identifica la colonna. Tutti gli altri membri sono zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'uso di formati di controllo intestazione come HDF CHECKBOX per modificare il formato delle intestazioni di colonna in un controllo visualizzazione elenco fa sì che il controllo invii il codice di notifica \_ [ \_ HDN ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) anziché LVN COLUMNCLICK quando si fa clic su un elemento di \_ intestazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





