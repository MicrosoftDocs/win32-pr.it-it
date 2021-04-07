---
title: Messaggio HDM_SETFILTERCHANGETIMEOUT (COMmctrl. h)
description: Imposta l'intervallo di timeout tra l'ora in cui viene apportata una modifica negli attributi di filtro e la pubblicazione di una \_ notifica FILTERCHANGE HDN. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetFilterChangeTimeout dell'intestazione.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- Controlli di Windows Message HDM_SETFILTERCHANGETIMEOUT
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048613"
---
# <a name="hdm_setfilterchangetimeout-message"></a>\_Messaggio HDM SETFILTERCHANGETIMEOUT

Imposta l'intervallo di timeout tra l'ora in cui viene apportata una modifica negli attributi di filtro e la pubblicazione di una notifica [ \_ FILTERCHANGE HDN](hdn-filterchange.md) . È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetFilterChangeTimeout dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di timeout in millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice del controllo filtro da modificare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_FILTERCHANGE HDN](hdn-filterchange.md)
</dt> </dl>

 

 





