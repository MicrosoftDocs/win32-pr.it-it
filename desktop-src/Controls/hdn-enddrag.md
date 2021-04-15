---
title: Codice di notifica HDN_ENDDRAG (COMmctrl. h)
description: Inviato da un controllo intestazione al termine di un'operazione di trascinamento su uno dei relativi elementi. Questo codice di notifica viene inviato come un \_ messaggio di notifica WM. Solo i controlli intestazione impostati sullo \_ stile DragDrop di HDS inviano il codice di notifica.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- Controlli di Windows per il codice di notifica HDN_ENDDRAG
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479456"
---
# <a name="hdn_enddrag-notification-code"></a>\_Codice di notifica ENDDRAG di HDN

Inviato da un controllo intestazione al termine di un'operazione di trascinamento su uno dei relativi elementi. Questo codice di notifica viene inviato come un messaggio di [**\_ notifica WM**](wm-notify.md) . Solo i controlli intestazione impostati sullo stile [**\_ DragDrop di HDS**](header-control-styles.md) inviano il codice di notifica.


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sull'elemento dell'intestazione trascinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per consentire al controllo di posizionare e riordinare automaticamente l'elemento, restituire **false**. Per impedire che l'elemento venga inserito, restituire **true**.

## <a name="remarks"></a>Commenti

Se il proprietario sta eseguendo la gestione del trascinamento della selezione esterna (manuale), deve restituire **false**. Il proprietario deve quindi riordinare manualmente gli elementi di intestazione inviando [**HDM \_ SetItem**](hdm-setitem.md) o [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





