---
title: LVM_SETITEMSTATE messaggio (Commctrl.h)
description: Modifica lo stato di un elemento in un controllo visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usando la \_ macro ListView SetItemState.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- LVM_SETITEMSTATE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b7375ad7edb32459fe6029081ec0a872d3673c90003e34ca21cd795d3a79ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217416"
---
# <a name="lvm_setitemstate-message"></a>Messaggio \_ LVM SETITEMSTATE

Modifica lo stato di un elemento in un controllo visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView SetItemState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco. Se questo parametro è -1, la modifica dello stato viene applicata a tutti gli elementi.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Il **membro stateMask** specifica i bit di stato da modificare e il membro **di** stato contiene i nuovi valori per tali bit. Gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si invia questo messaggio in modo esplicito, restituisce **TRUE in caso** di esito positivo o FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

Il valore di stato di un elemento include un set di flag di bit che indicano lo stato dell'elemento. Il valore di stato può includere anche indici dell'elenco immagini che indicano l'immagine di stato dell'elemento e l'immagine di sovrapposizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





