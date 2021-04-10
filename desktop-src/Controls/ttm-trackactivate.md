---
title: Messaggio TTM_TRACKACTIVATE (COMmctrl. h)
description: Attiva o disattiva una descrizione comando di rilevamento.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- Controlli di Windows Message TTM_TRACKACTIVATE
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964466"
---
# <a name="ttm_trackactivate-message"></a>\_Messaggio TTM TRACKACTIVATE

Attiva o disattiva una descrizione comando di rilevamento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica se è in corso l'attivazione o la disattivazione del rilevamento. I valori validi sono i seguenti:



| Valore                                                                                                                                | Significato                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**TRUE**</dt> </dl>    | Attivare il rilevamento.<br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**FALSE**</dt> </dl> | Disattiva il rilevamento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) che identifica lo strumento a cui si applica questo messaggio. I membri **HWND** e **UID** identificano lo strumento e il membro **cbSize** specifica le dimensioni della struttura. Tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_TRACKPOSITION TTM**](ttm-trackposition.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso di controlli ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 





