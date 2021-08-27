---
title: LVM_GETNUMBEROFWORKAREAS messaggio (Commctrl.h)
description: Recupera il numero di aree di lavoro in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView GetNumberOfWorkAreas.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- LVM_GETNUMBEROFWORKAREAS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 735dbb808755857df3dec4c5e8a021b9fe873e555607dc547bc77e67e123b948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088881"
---
# <a name="lvm_getnumberofworkareas-message"></a>Messaggio LVM \_ GETNUMBEROFWORKAREAS

Recupera il numero di aree di lavoro in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView GetNumberOfWorkAreas.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un valore UINT che riceve il numero di aree di lavoro nel controllo visualizzazione elenco. Se zero viene inserito in questa variabile, non è attualmente impostata alcuna area di lavoro. Questo valore non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene usato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso dei List-View personalizzati](using-list-view-controls.md)
</dt> </dl>

 

 





