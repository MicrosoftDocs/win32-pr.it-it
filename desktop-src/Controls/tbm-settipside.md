---
title: Messaggio TBM_SETTIPSIDE (COMmctrl. h)
description: Posiziona un controllo ToolTip utilizzato da un controllo TrackBar. I controlli TrackBar che usano le descrizioni comandi di TBS \_ visualizzano le descrizioni comandi.
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- Controlli di Windows Message TBM_SETTIPSIDE
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400426"
---
# <a name="tbm_settipside-message"></a>\_Messaggio SETTIPSIDE TBM

Posiziona un controllo ToolTip utilizzato da un controllo TrackBar. I controlli TrackBar che usano le descrizioni comandi di [**TBS \_**](trackbar-control-styles.md) visualizzano le descrizioni comandi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che rappresenta la posizione in cui visualizzare il controllo ToolTip. I valori validi sono i seguenti:



| Valore                                                                                                                                                   | Significato                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <dt>**TBTS \_ Top**</dt> </dl>          | Il controllo ToolTip verrà posizionato sopra l'oggetto TrackBar. Questo flag viene utilizzato con gli TrackBar orizzontali.<br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <dt>**TBTS a \_ sinistra**</dt> </dl>       | Il controllo ToolTip verrà posizionato a sinistra del controllo TrackBar. Questo flag viene utilizzato con gli TrackBar verticali.<br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <dt>**TBTS in \_ basso**</dt> </dl> | Il controllo ToolTip verrà posizionato al di sotto del TrackBar. Questo flag viene utilizzato con gli TrackBar orizzontali.<br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <dt>**TBTS a \_ destra**</dt> </dl>    | Il controllo ToolTip verrà posizionato a destra dell'oggetto TrackBar. Questo flag viene utilizzato con gli TrackBar verticali.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore che rappresenta la posizione precedente del controllo ToolTip. Il valore restituito è uguale a uno dei valori possibili per *wParam*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





