---
title: Messaggio TCM_GETITEM (COMmctrl. h)
description: Recupera le informazioni su una scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItem di TabCtrl.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- Controlli di Windows Message TCM_GETITEM
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
ms.openlocfilehash: b6f94f26a0893416847df052ff47731391a86f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302364"
---
# <a name="tcm_getitem-message"></a>TCM- \_ messaggio GETitem

Recupera le informazioni su una scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItem di TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della scheda.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) che specifica le informazioni per recuperare e ricevere informazioni sulla scheda. Quando il messaggio viene inviato, il membro **mask** specifica gli attributi da restituire. Se il membro **mask** specifica il \_ valore di testo TCIF, il membro **pszText** deve contenere l'indirizzo del buffer che riceve il testo dell'elemento e il membro **cchTextMax** deve specificare le dimensioni del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Se il \_ flag di testo TCIF è impostato nel membro **mask** della struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , il controllo può modificare il membro **pszText** della struttura in modo che punti al nuovo testo anziché riempire il buffer con il testo richiesto. Il controllo può impostare il membro **pszText** su **null** per indicare che all'elemento non è associato alcun testo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TCM \_ GETITEMW** (Unicode) e **TCM \_ getitema** (ANSI)<br/>                   |



 

 





