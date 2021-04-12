---
title: Messaggio HDM_GETITEM (COMmctrl. h)
description: Ottiene informazioni su un elemento in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetItem dell'intestazione.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- Controlli di Windows Message HDM_GETITEM
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
ms.openlocfilehash: c2073602121480930e0f7d9d2e5a904c0dea77ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119835"
---
# <a name="hdm_getitem-message"></a>HDM \_ messaggio GETitem

Ottiene informazioni su un elemento in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetItem dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento per il quale devono essere recuperate le informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Quando il messaggio viene inviato, il membro **mask** indica il tipo di informazioni richieste. Quando il messaggio viene restituito, gli altri membri ricevono le informazioni richieste. Se il membro **mask** specifica zero, il messaggio restituisce **true** , ma non copia alcuna informazione nella struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Se il \_ flag di testo HDI è impostato nel membro **mask** della struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , il controllo può modificare il membro **pszText** della struttura in modo che punti al nuovo testo anziché riempire il buffer con il testo richiesto. Le applicazioni non devono presupporre che il testo venga sempre inserito nel buffer richiesto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HDM \_ GETITEMW** (Unicode) e **HDM \_ getitema** (ANSI)<br/>                   |



 

 





