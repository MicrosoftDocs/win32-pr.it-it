---
title: TCM_GETITEM messaggio (Commctrl.h)
description: Recupera informazioni su una scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro TabCtrl \_ GetItem.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- TCM_GETITEM controlli di Windows messaggio
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5403bb85e1b2747d1ab6081d33c25ec20a3b2099fc83b2b15e66b014f558584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876581"
---
# <a name="tcm_getitem-message"></a>Messaggio \_ TCM GETITEM

Recupera informazioni su una scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**TabCtrl \_ GetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della scheda.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) che specifica le informazioni da recuperare e ricevere informazioni sulla scheda. Quando il messaggio viene inviato, il **membro mask** specifica gli attributi da restituire. Se il membro **mask** specifica il valore TCIF TEXT, il membro pszText deve contenere l'indirizzo del buffer che riceve il testo dell'elemento e il membro \_  **cchTextMax** deve specificare le dimensioni del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Se il flag TEXT di TCIF è impostato nel membro mask della struttura \_ [**TCITEM,**](/windows/win32/api/commctrl/ns-commctrl-tcitema) il controllo può modificare il membro **pszText** della struttura in modo che punti al nuovo testo anziché riempire il buffer con il testo richiesto.  Il controllo può impostare il **membro pszText** su **NULL** per indicare che all'elemento non è associato alcun testo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TCM \_ GETITEMW** (Unicode) e **TCM \_ GETITEMA** (ANSI)<br/>                   |



 

 





