---
title: TCM_SETITEM messaggio (Commctrl.h)
description: Imposta alcuni o tutti gli attributi di una scheda. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TabCtrl SetItem.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- TCM_SETITEM controlli Windows messaggio
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27f93e2743e5676c0fcca932cfa1936bb72667ef4fa4a5334eaae3e78d2be08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876327"
---
# <a name="tcm_setitem-message"></a>Messaggio \_ SETITEM TCM

Imposta alcuni o tutti gli attributi di una scheda. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TabCtrl SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) che contiene i nuovi attributi dell'elemento. Il **membro mask** specifica gli attributi da impostare. Se il **membro mask** specifica il valore TCIF TEXT, il membro pszText è l'indirizzo di una stringa con terminazione Null e il membro \_ **cchTextMax** viene ignorato. 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TCM \_ SETITEMW** (Unicode) e **TCM \_ SETITEMA** (ANSI)<br/>                   |



 

 





