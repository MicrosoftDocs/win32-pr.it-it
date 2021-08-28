---
title: SBM_ENABLE_ARROWS messaggio (Winuser.h)
description: Un'applicazione invia il messaggio SBM ENABLE ARROWS per abilitare o disabilitare una o entrambe le \_ frecce di un controllo barra di \_ scorrimento.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- SBM_ENABLE_ARROWS dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e7f3ef8728befe72ec4f2c4afe39caeb10bc0b58984612a5db2445963dc549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770021"
---
# <a name="sbm_enable_arrows-message"></a>Messaggio SBM \_ ENABLE \_ ARROWS

Un'applicazione invia il **messaggio SBM \_ ENABLE \_ ARROWS** per abilitare o disabilitare una o entrambe le frecce di un controllo barra di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se le frecce della barra di scorrimento sono abilitate o disabilitate e indica quali frecce sono abilitate o disabilitate. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                   | Significato                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <dt>**ESB \_ \_ DISABILITARE ENTRAMBI**</dt> </dl> | Disabilita entrambe le frecce su una barra di scorrimento.<br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <dt>**DISABILITAZIONE \_ ESB \_**</dt> </dl> | Disabilita la freccia giù su una barra di scorrimento verticale.<br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <dt>**ESB \_ DISABLE \_ LTUP**</dt> </dl> | Disabilita la freccia sinistra su una barra di scorrimento orizzontale o la freccia su su una barra di scorrimento verticale.<br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <dt>**DISABILITAZIONE ESB \_ A \_ SINISTRA**</dt> </dl> | Disabilita la freccia sinistra su una barra di scorrimento orizzontale.<br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <dt>**ESB \_ DISABLE \_ RTDN**</dt> </dl> | Disabilita la freccia destra su una barra di scorrimento orizzontale o la freccia giù su una barra di scorrimento verticale.<br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <dt>**DISABILITAZIONE \_ ESB \_**</dt> </dl>       | Disabilita la freccia SU su una barra di scorrimento verticale.<br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <dt>**ESB \_ ABILITARE \_ ENTRAMBI**</dt> </dl>    | Abilita entrambe le frecce su una barra di scorrimento.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è **TRUE.** in caso contrario, è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

 





