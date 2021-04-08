---
title: Codice di notifica LVN_COLUMNCLICK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata fatto clic su un'intestazione di colonna mentre il controllo elenco-visualizzazione era in modalità report. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- Controlli di Windows per il codice di notifica LVN_COLUMNCLICK
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
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047926"
---
# <a name="lvn_columnclick-notification-code"></a>\_Codice di notifica COLUMNCLICK di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata fatto clic su un'intestazione di colonna mentre il controllo elenco-visualizzazione era in modalità report. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Il membro **iItem** è-1 e il membro **iSubItem** identifica la colonna. Tutti gli altri membri sono pari a zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'uso di formati di controllo intestazione, ad esempio HDF \_ CheckBox per modificare il formato delle intestazioni di colonna in un controllo visualizzazione elenco, fa sì che il controllo invii il codice di notifica [ \_ ITEMSTATEICONCLICK HDN](hdn-itemstateiconclick.md) anziché LVN \_ COLUMNCLICK quando si fa clic su un elemento di intestazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





