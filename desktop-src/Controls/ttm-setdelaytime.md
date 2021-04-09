---
title: Messaggio TTM_SETDELAYTIME (COMmctrl. h)
description: Imposta le durate iniziali, popup e reshow per un controllo ToolTip.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- Controlli di Windows Message TTM_SETDELAYTIME
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964235"
---
# <a name="ttm_setdelaytime-message"></a>\_Messaggio TTM SETDELAYTIME

Imposta le durate iniziali, popup e reshow per un controllo ToolTip.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag che specifica il valore di ora da impostare. Questo parametro può essere uno dei valori seguenti



| Valore                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**\_AUTOPOP TTDT**</dt> </dl>       | Imposta la quantità di tempo in cui una finestra della descrizione comando rimane visibile se il puntatore è fermo all'interno del rettangolo di delimitazione di uno strumento. Per restituire il valore predefinito di autopop delay, impostare *lParam* su-1.<br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ iniziale**</dt> </dl>       | Imposta la quantità di tempo in cui un puntatore deve rimanere fermo nel rettangolo di delimitazione di uno strumento prima che venga visualizzata la finestra della descrizione comando. Per restituire il valore predefinito dell'intervallo di ritardo iniziale, impostare *lParam* su-1.<br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ RImostra**</dt> </dl>          | Consente di impostare la quantità di tempo necessaria per la visualizzazione delle finestre di descrizione comando successive quando il puntatore passa da uno strumento all'altro. Per restituire il tempo di ritardo della rivisualizzazione al valore predefinito, impostare *lParam* su-1.<br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <dt>**TTDT \_ automatico**</dt> </dl> | Impostare tutte e tre le ore di ritardo sulle proporzioni predefinite. Il tempo di autopop sarà dieci volte l'ora iniziale e il tempo di ripresentazione sarà un quinto del tempo iniziale. Se questo flag è impostato, utilizzare un valore positivo di *lParam* per specificare il tempo iniziale, in millisecondi. Impostare *lParam* su un valore negativo per restituire i valori predefiniti per tutti e tre i tempi di ritardo.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il tempo di ritardo, in millisecondi. Il valore di [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="remarks"></a>Commenti

Le ore di ritardo predefinite sono basate sull'ora di doppio clic. Per l'ora di doppio clic predefinita di 500 ms, i tempi di ritardo iniziale, autopop e rimostrati sono rispettivamente 500 ms, 5000 ms e 100 ms. Il frammento di codice seguente usa la funzione [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) per determinare le tre ore di ritardo per qualsiasi sistema.


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETDELAYTIME TTM**](ttm-getdelaytime.md)
</dt> </dl>

 

