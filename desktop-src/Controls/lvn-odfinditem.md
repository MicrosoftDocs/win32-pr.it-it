---
title: Messaggio LVN_ODFINDITEM (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco virtuale quando è necessario che il proprietario trovi un particolare elemento di callback.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- Controlli di Windows Message LVN_ODFINDITEM
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120526"
---
# <a name="lvn_odfinditem-message"></a>\_Messaggio LVN ODFINDITEM

Inviato da un controllo di [visualizzazione elenco virtuale](list-view-controls-overview.md) quando è necessario che il proprietario trovi un particolare elemento di callback. Ad esempio, il controllo invierà questo codice di notifica quando riceverà un input da tastiera di scelta rapida o quando riceve un messaggio [**\_ FINDITEM LVM**](lvm-finditem.md) . Il \_ codice di notifica ODFINDITEM di LVN viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) che include le informazioni da utilizzare per la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento trovato oppure-1 se non viene trovato alcun elemento.

## <a name="remarks"></a>Commenti

Le informazioni di ricerca vengono inviate sotto forma di una struttura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , che è un membro della struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVN \_ ODFINDITEMW** (Unicode) e **LVN \_ ODFINDITEMA** (ANSI)<br/>             |



 

 





