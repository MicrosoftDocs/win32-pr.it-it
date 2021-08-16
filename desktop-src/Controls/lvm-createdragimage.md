---
title: LVM_CREATEDRAGIMAGE messaggio (Commctrl.h)
description: Crea un elenco di immagini di trascinamento per l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro CreateDragImage di ListView.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- LVM_CREATEDRAGIMAGE controlli di Windows messaggio
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d551dfa7b14ecff8c9fd1efe015e173403c1b5981f294a18b3180a42cc03de63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411997"
---
# <a name="lvm_createdragimage-message"></a>Messaggio LVM \_ CREATEDRAGIMAGE

Crea un elenco di immagini di trascinamento per l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ CreateDragImage di ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura POINT**](/previous-versions//dd162805(v=vs.85)) che riceve la posizione iniziale dell'angolo superiore sinistro dell'immagine, nelle coordinate di visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini di trascinamento in caso di esito positivo oppure **NULL in caso** contrario.

## <a name="remarks"></a>Commenti

L'applicazione è responsabile dell'eliminazione dell'elenco di immagini quando non è più necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

