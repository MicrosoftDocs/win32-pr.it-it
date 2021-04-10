---
title: Codice di notifica TVN_ITEMEXPANDING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che l'elenco degli elementi figlio di un elemento padre sta per espandersi o comprimere. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- Controlli di Windows per il codice di notifica TVN_ITEMEXPANDING
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964843"
---
# <a name="tvn_itemexpanding-notification-code"></a>\_Codice di notifica ITEMEXPANDING di TVN

Notifica alla finestra padre di un controllo di visualizzazione albero che l'elenco degli elementi figlio di un elemento padre sta per espandersi o comprimere. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Il membro **itemNew** è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni valide sull'elemento padre nei membri **Hite**, **state** e **lParam** . Il membro dell' **azione** indica se l'elenco deve essere espanso o compresso. Per un elenco di valori possibili, vedere la descrizione del messaggio [**di \_ espansione TVM**](tvm-expand.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per impedire l'espansione o la compressione dell'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ ITEMEXPANDINGW** (Unicode) e **TVN \_ ITEMEXPANDINGA** (ANSI)<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_ITEMEXPANDED TVN](tvn-itemexpanded.md)
</dt> </dl>

 

 





