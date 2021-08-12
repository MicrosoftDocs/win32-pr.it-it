---
title: TB_GETDISABLEDIMAGELIST messaggio (Commctrl.h)
description: Recupera l'elenco di immagini utilizzato da un controllo barra degli strumenti per visualizzare i pulsanti inattivi.
ms.assetid: 8f6782d5-488b-4906-908a-e4bf8d512e0a
keywords:
- TB_GETDISABLEDIMAGELIST controlli Windows messaggio
topic_type:
- apiref
api_name:
- TB_GETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eec9285e9a516547aece30d059f1fabd9d590e445d2124e9bccad5cb6cfc354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669944"
---
# <a name="tb_getdisabledimagelist-message"></a>TB \_ GETDISABLEDIMAGELIST message

Recupera l'elenco di immagini utilizzato da un controllo barra degli strumenti per visualizzare i pulsanti inattivi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini inattive oppure **NULL se** non è impostato alcun elenco di immagini inattive.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





