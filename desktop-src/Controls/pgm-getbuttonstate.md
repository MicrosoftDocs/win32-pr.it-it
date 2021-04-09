---
title: Messaggio PGM_GETBUTTONSTATE (COMmctrl. h)
description: Recupera lo stato del pulsante specificato in un controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro GetButtonState del cercapersone.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- Controlli di Windows Message PGM_GETBUTTONSTATE
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8c9eebbc0aa91651a01de1fe193544f0c8afcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964559"
---
# <a name="pgm_getbuttonstate-message"></a>\_Messaggio GETBUTTONSTATE PGM

Recupera lo stato del pulsante specificato in un controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetButtonState del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Indica il pulsante per il quale recuperare lo stato. I valori possibili sono i seguenti:



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <dt>**\_TOPORLEFT PGB**</dt> </dl>             | Indica il pulsante in alto in un controllo pager [**PGS \_ Vert**](pager-control-styles.md) o il pulsante sinistro in un controllo pager [**\_ orizzontalmente**](pager-control-styles.md) . <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <dt>**\_BOTTOMORRIGHT PGB**</dt> </dl> | Indica il pulsante in basso in un controllo pager [**PGS \_ Vert**](pager-control-styles.md) o il pulsante destro in un controllo pager [**\_ orizzontalmente**](pager-control-styles.md) . <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce lo stato del pulsante specificato in *lParam*. Si tratta di uno o più dei valori seguenti (se viene restituito più di un valore, questi verranno combinati usando un operatore OR bit per bit):



| Codice restituito                                                                                   | Descrizione                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**PGF \_ invisibile**</dt> </dl> | Il pulsante non è visibile. <br/>      |
| <dl> <dt>**PGF \_ normale**</dt> </dl>    | Il pulsante è nello stato normale. <br/>  |
| <dl> <dt>**PGF \_ grigio**</dt> </dl>    | Il pulsante è in stato grigio. <br/>  |
| <dl> <dt>**PGF \_ premuto**</dt> </dl> | Il pulsante è nello stato premuto. <br/> |
| <dl> <dt>**PGF \_ Hot**</dt> </dl>       | Il pulsante è nello stato attivo. <br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





