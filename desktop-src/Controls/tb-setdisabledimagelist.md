---
title: TB_SETDISABLEDIMAGELIST messaggio (Commctrl.h)
description: Imposta l'elenco di immagini che verrà utilizzato dal controllo barra degli strumenti per visualizzare i pulsanti disabilitati.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- TB_SETDISABLEDIMAGELIST dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9125c5e5ac742f4692fc5464cd51c89e111558c4d0004e08d7cef9c862d03cbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167491"
---
# <a name="tb_setdisabledimagelist-message"></a>TB \_ SETDISABLEDIMAGELIST message

Imposta l'elenco di immagini che verrà utilizzato dal controllo barra degli strumenti per visualizzare i pulsanti disabilitati.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini che verrà impostato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini usato in precedenza per visualizzare i pulsanti disabilitati oppure **NULL** se in precedenza non è stato impostato alcun elenco di immagini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





