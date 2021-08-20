---
title: TTM_ACTIVATE messaggio (Commctrl.h)
description: Attiva o disattiva un controllo descrizione comando.
ms.assetid: f37da001-748c-4c51-bb32-dc49031ff2fb
keywords:
- TTM_ACTIVATE del messaggio Windows controlli
topic_type:
- apiref
api_name:
- TTM_ACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1b2a0c67fec22b11adc54f04ed7a6e4f3cb299ad67018b29f1239cebe0f8604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166394"
---
# <a name="ttm_activate-message"></a>Messaggio TTM \_ ACTIVATE

Attiva o disattiva un controllo descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di attivazione. Se questo parametro è **TRUE,** il controllo descrizione comando viene attivato. Se è **FALSE, il** controllo descrizione comando viene disattivato.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





