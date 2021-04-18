---
title: Messaggio TTM_GETDELAYTIME (COMmctrl. h)
description: Recupera le durate iniziali, popup e reshow attualmente impostate per un controllo ToolTip.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- Controlli di Windows Message TTM_GETDELAYTIME
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
ms.openlocfilehash: 4ff8c75f078465646333cae1f519049733a0c9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301656"
---
# <a name="ttm_getdelaytime-message"></a>\_Messaggio TTM GETDELAYTIME

Recupera le durate iniziali, popup e reshow attualmente impostate per un controllo ToolTip.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag che specifica quale valore Duration verrà recuperato. Per il parametro è possibile specificare uno dei valori riportati di seguito:



| Valore                                                                                                                                                      | Significato                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**\_AUTOPOP TTDT**</dt> </dl> | Recuperare la quantità di tempo in cui la finestra della descrizione comando rimane visibile se il puntatore è fermo all'interno del rettangolo di delimitazione di uno strumento.<br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ iniziale**</dt> </dl> | Recuperare l'intervallo di tempo in cui il puntatore deve rimanere fermo nel rettangolo di delimitazione di uno strumento prima che venga visualizzata la finestra della descrizione comando.<br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ RImostra**</dt> </dl>    | Recuperare la quantità di tempo necessaria per la visualizzazione delle finestre di descrizione comando successive quando il puntatore passa da uno strumento all'altro.<br/>         |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce e il valore INT con la durata specificata in millisecondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETDELAYTIME TTM**](ttm-setdelaytime.md)
</dt> </dl>

 

 





