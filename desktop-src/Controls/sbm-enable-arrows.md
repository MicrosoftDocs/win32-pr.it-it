---
title: Messaggio SBM_ENABLE_ARROWS (winuser. h)
description: Un'applicazione invia il \_ messaggio di abilitazione della \_ freccia SBM per abilitare o disabilitare una o entrambe le frecce di un controllo barra di scorrimento.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- Controlli di Windows Message SBM_ENABLE_ARROWS
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
ms.openlocfilehash: 78895b43ec7908172a6164917b33ac8549088db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964635"
---
# <a name="sbm_enable_arrows-message"></a>\_Messaggio di abilitazione delle frecce di SBM \_

Un'applicazione invia il messaggio di **\_ Abilitazione della \_ freccia SBM** per abilitare o disabilitare una o entrambe le frecce di un controllo barra di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se le frecce della barra di scorrimento sono abilitate o disabilitate e indicano quali frecce sono abilitate o disabilitate. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                   | Significato                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <dt>**ESB \_ Disabilita \_ entrambi**</dt> </dl> | Disabilita entrambe le frecce su una barra di scorrimento.<br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <dt>**\_disabilitazione \_ ESB**</dt> </dl> | Disabilita la freccia giù su una barra di scorrimento verticale.<br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <dt>**ESB \_ disabilitare \_ LTUP**</dt> </dl> | Disabilita la freccia sinistra su una barra di scorrimento orizzontale o la freccia su su una barra di scorrimento verticale.<br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <dt>**ESB \_ Disable \_ Left**</dt> </dl> | Disabilita la freccia sinistra su una barra di scorrimento orizzontale.<br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <dt>**ESB \_ disabilitare \_ RTDN**</dt> </dl> | Disabilita la freccia destra su una barra di scorrimento orizzontale o sulla freccia in giù su una barra di scorrimento verticale.<br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <dt>**\_disabilitazione \_ ESB**</dt> </dl>       | Disabilita la freccia su su una barra di scorrimento verticale.<br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <dt>**ESB \_ Abilita \_ entrambi**</dt> </dl>    | Abilita entrambe le frecce su una barra di scorrimento.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è **true**; in caso contrario, è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



 

 





