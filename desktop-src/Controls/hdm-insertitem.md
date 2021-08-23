---
title: HDM_INSERTITEM messaggio (Commctrl.h)
description: Inserisce un nuovo elemento in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Header InsertItem.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- HDM_INSERTITEM dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30a07637afae1a3efcf71b3b556c32bebf96775bb2a5cbdf6e92513d33ec5c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544741"
---
# <a name="hdm_insertitem-message"></a>Messaggio \_ INSERTITEM HDM

Inserisce un nuovo elemento in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Header InsertItem.**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento dopo il quale deve essere inserito il nuovo elemento. Il nuovo elemento viene inserito alla fine del controllo intestazione se *wParam* è maggiore o uguale al numero di elementi nel controllo. Se *wParam è* zero, il nuovo elemento viene inserito all'inizio del controllo intestazione.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) che contiene informazioni sul nuovo elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice del nuovo elemento in caso di esito positivo oppure -1 in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDM \_ INSERTITEMW** (Unicode) e **HDM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





