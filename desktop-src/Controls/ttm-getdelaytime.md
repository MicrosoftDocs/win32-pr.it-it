---
title: TTM_GETDELAYTIME messaggio (Commctrl.h)
description: Recupera le durate iniziali, popup e di nuova visualizzazione attualmente impostate per un controllo descrizione comando.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- TTM_GETDELAYTIME di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0e63eca126477a6f602e6e23be75495319d30aa2814d2d72b8426a96c078326
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769261"
---
# <a name="ttm_getdelaytime-message"></a>Messaggio \_ TTM GETDELAYTIME

Recupera le durate iniziali, popup e di nuova visualizzazione attualmente impostate per un controllo descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag che specifica il valore della durata che verrà recuperato. Per il parametro è possibile specificare uno dei valori riportati di seguito:



| Valore                                                                                                                                                      | Significato                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**TTDT \_ AUTOPOP**</dt> </dl> | Recuperare la quantità di tempo per cui la finestra della descrizione comando rimane visibile se il puntatore è fermo all'interno del rettangolo di delimitazione di uno strumento.<br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ INITIAL**</dt> </dl> | Recuperare la quantità di tempo per cui il puntatore deve rimanere fermo all'interno del rettangolo di delimitazione di uno strumento prima che venga visualizzata la finestra della descrizione comando.<br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ RESHOW**</dt> </dl>    | Recuperare il tempo necessario per visualizzare le finestre della descrizione comando successive quando il puntatore si sposta da uno strumento a un altro.<br/>         |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce e il valore INT con la durata specificata in millisecondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md)
</dt> </dl>

 

 





