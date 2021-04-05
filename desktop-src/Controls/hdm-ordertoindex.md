---
title: Messaggio HDM_ORDERTOINDEX (COMmctrl. h)
description: Recupera un valore di indice per un elemento in base al relativo ordine nel controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro OrderToIndex dell'intestazione.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- Controlli di Windows Message HDM_ORDERTOINDEX
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b65d10fb27c9a07639ebbd5770a53d72cbf0aba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048300"
---
# <a name="hdm_ordertoindex-message"></a>\_Messaggio HDM ORDERTOINDEX

Recupera un valore di indice per un elemento in base al relativo ordine nel controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ OrderToIndex dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ordine in cui l'elemento viene visualizzato all'interno del controllo intestazione, da sinistra a destra. Il valore di indice dell'elemento nella colonna all'estrema sinistra, ad esempio, è 0. Il valore per l'elemento successivo a destra è 1 e così via.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che indica l'indice dell'elemento. Se *wParam* non è valido (negativo o troppo grande), restituisce uguale a *wParam*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





