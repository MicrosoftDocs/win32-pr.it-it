---
title: SB_SIMPLE messaggio (Commctrl.h)
description: Specifica se una finestra di stato visualizza testo semplice o tutte le parti della finestra impostate da un messaggio SETPARTS SB \_ precedente.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- SB_SIMPLE dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f0a896c9adcab6886151753761c62aefb8f4dc6ee21b7e85bb7507bda11f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132211"
---
# <a name="sb_simple-message"></a>Messaggio SB \_ SIMPLE

Specifica se una finestra di stato visualizza testo semplice o tutte le parti della finestra impostate da un messaggio [**\_ SETPARTS SB**](sb-setparts.md) precedente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag del tipo di visualizzazione. Se questo parametro è **TRUE,** nella finestra viene visualizzato testo semplice. Se è **FALSE,** vengono visualizzate più parti.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

Se la finestra di stato viene modificata da non semplice a semplice o viceversa, la finestra viene ridisegnata immediatamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





