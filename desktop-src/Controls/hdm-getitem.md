---
title: HDM_GETITEM messaggio (Commctrl.h)
description: Ottiene informazioni su un elemento in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Header GetItem.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- HDM_GETITEM di controllo Windows messaggio
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 566f8b8e3bdf4e92abfb1fdd5874b8514814792e1d7aae169cc2aca4b2e8d101
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436191"
---
# <a name="hdm_getitem-message"></a>Messaggio \_ GETITEM HDM

Ottiene informazioni su un elemento in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Header GetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento per il quale devono essere recuperate le informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura HDITEM.**](/windows/win32/api/commctrl/ns-commctrl-hditema) Quando il messaggio viene inviato, il **membro mask** indica il tipo di informazioni richieste. Quando il messaggio viene restituito, gli altri membri ricevono le informazioni richieste. Se il **membro mask** specifica zero, il messaggio restituisce **TRUE** ma non copia alcuna informazione nella struttura .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Se il flag HDI TEXT è impostato nel membro mask della struttura HDITEM, il controllo può modificare il membro \_ **pszText**  della struttura in modo che punti al nuovo testo anziché riempire il buffer con il testo richiesto. [](/windows/win32/api/commctrl/ns-commctrl-hditema) Le applicazioni non devono presupporre che il testo verrà sempre inserito nel buffer richiesto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDM \_ GETITEMW** (Unicode) e **HDM \_ GETITEMA** (ANSI)<br/>                   |



 

 





