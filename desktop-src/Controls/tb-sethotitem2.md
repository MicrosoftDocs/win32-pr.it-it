---
title: TB_SETHOTITEM2 messaggio (Commctrl.h)
description: "TB_SETHOTITEM2 messaggio: imposta l'elemento di accesso rapido in una barra degli strumenti."
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 messaggio Controlli Windows
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7daf67839837adccfbec99bf03fc4dfff97738db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104139"
---
# <a name="tb_sethotitem2-message"></a>TB \_ SETHOTITEM2 message

Imposta l'elemento di accesso rapido in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento che verrà reso a caldo. Se questo valore è -1, nessuno degli elementi sarà a caldo.

</dd> <dt>

*lParam* 
</dt> <dd>Combinazione di flag HICF \_ xxx. Vedere <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento a caldo precedente oppure -1 se non è presente alcun elemento a caldo.

## <a name="remarks"></a>Commenti

Il comportamento di questo messaggio non è definito per le barre degli strumenti che non hanno lo [**stile TBSTYLE \_ FLAT.**](toolbar-control-and-button-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





