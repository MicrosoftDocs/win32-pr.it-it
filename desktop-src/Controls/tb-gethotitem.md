---
title: TB_GETHOTITEM messaggio (Commctrl.h)
description: Recupera l'indice dell'elemento di accesso rapido in una barra degli strumenti.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- TB_GETHOTITEM dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f33566a586ceaa524f720a9d688897f132ee227950f1f786093150955eafa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918831"
---
# <a name="tb_gethotitem-message"></a>TB \_ GETHOTITEM message

Recupera l'indice dell'elemento di accesso rapido in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento a caldo oppure -1 se non è impostato alcun elemento a caldo. I controlli barra degli strumenti che non hanno lo stile [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) non hanno elementi hot.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





