---
title: LVN_COLUMNOVERFLOWCLICK di notifica (Commctrl.h)
description: Inviato da un controllo di visualizzazione elenco quando si fa clic sul pulsante di overflow. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- LVN_COLUMNOVERFLOWCLICK codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb28deb3dd98542791b4c8daf350e618e43db57d5090a93d49af5e55e8b39ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077121"
---
# <a name="lvn_columnoverflowclick-notification-code"></a>Codice di notifica LVN \_ COLUMNOVERFLOWCLICK

Inviato da un controllo di visualizzazione elenco quando si fa clic sul pulsante di overflow. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a [**una struttura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) che descrive il codice di notifica. Il chiamante è responsabile dell'allocazione di questa struttura, inclusa la [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenuta. Impostare i membri della **struttura NMHDR.** Il **membro di** codice deve essere impostato su LVN \_ COLUMNOVERFLOWCLICK.

Impostare il **membro iItem** della [**struttura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) su -1. Impostare il **membro iSubItem** sull'indice dell'elemento secondario. Impostare i **membri uNewState**, **uOldState** e **lParam** su zero. I membri rimanenti della **struttura NMLISTVIEW** non vengono usati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore della notifica esegue il cast *di lParam* per recuperare la [**struttura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) Il *parametro wParam* contiene l'ID del controllo che invia il codice di notifica.

Se un controllo intestazione è un elemento figlio del controllo listview, il controllo intestazione deve inviare questo codice di notifica al controllo listview quando il controllo intestazione riceve il codice di notifica [HDN \_ OVERFLOWCLICK.](hdn-overflowclick.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





