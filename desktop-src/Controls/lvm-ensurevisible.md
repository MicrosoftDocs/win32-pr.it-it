---
title: LVM_ENSUREVISIBLE messaggio (Commctrl.h)
description: Garantisce che un elemento della visualizzazione elenco sia completamente o parzialmente visibile, scorrendo il controllo di visualizzazione elenco, se necessario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro EnsureVisible di ListView.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- LVM_ENSUREVISIBLE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baeefaf90f0a4562fb187024b2c6f8676c68fb9d46377a4ced900bda6cfd3dfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920301"
---
# <a name="lvm_ensurevisible-message"></a>Messaggio LVM \_ ENSUREVISIBLE

Garantisce che un elemento della visualizzazione elenco sia completamente o parzialmente visibile, scorrendo il controllo di visualizzazione elenco, se necessario. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EnsureVisible di ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore che specifica se l'elemento deve essere completamente visibile. Se questo parametro è **TRUE,** non si verifica alcuno scorrimento se l'elemento è almeno parzialmente visibile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Il messaggio ha esito negativo se lo stile della finestra include [**LVS \_ NOSCROLL.**](list-view-window-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





