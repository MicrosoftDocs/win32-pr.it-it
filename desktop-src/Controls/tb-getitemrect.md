---
title: TB_GETITEMRECT messaggio (Commctrl.h)
description: Recupera il rettangolo di delimitazione di un pulsante in una barra degli strumenti.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- TB_GETITEMRECT controlli di Windows messaggio
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6dbfa4c7e305c4e2dfe53b45edaac1d6601631c920fa266c64292fd7e6d97e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829706"
---
# <a name="tb_getitemrect-message"></a>TB \_ GETITEMRECT message

Recupera il rettangolo di delimitazione di un pulsante in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero del pulsante per il quale recuperare informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura RECT**](/previous-versions//dd162897(v=vs.85)) che riceve le coordinate client del rettangolo di delimitazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio non recupera il rettangolo di delimitazione per i pulsanti il cui stato è impostato sul [**valore TBSTATE \_ HIDDEN.**](toolbar-button-states.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

