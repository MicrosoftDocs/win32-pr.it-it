---
title: PGM_GETBUTTONSTATE messaggio (Commctrl.h)
description: Recupera lo stato del pulsante specificato in un controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Pager GetButtonState.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- PGM_GETBUTTONSTATE controlli Windows messaggio
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
ms.openlocfilehash: 2014b6e36a0ab883155d786760ef54f02c89ee0d17192d6082d40ad19eec95a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830192"
---
# <a name="pgm_getbuttonstate-message"></a>Messaggio \_ GETBUTTONSTATE PGM

Recupera lo stato del pulsante specificato in un controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager GetButtonState.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Indica il pulsante per il quale recuperare lo stato. I valori possibili sono i seguenti:



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <dt>**PGB \_ TOPORLEFT**</dt> </dl>             | Indica il pulsante superiore in un controllo [**pager \_ PGS VERT**](pager-control-styles.md) o il pulsante sinistro in un controllo pager [**\_ HORZ PGS.**](pager-control-styles.md) <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <dt>**PGB \_ BOTTOMORRIGHT**</dt> </dl> | Indica il pulsante inferiore in un controllo [**pager \_ PGS VERT**](pager-control-styles.md) o il pulsante destro in un controllo pager [**\_ HOBUTTON di PGS.**](pager-control-styles.md) <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce lo stato del pulsante specificato in *lParam.* Si tratta di uno o più dei valori seguenti (se viene restituito più di un valore, verranno combinati usando un OR bit per bit):



| Codice restituito                                                                                   | Descrizione                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**PGF \_ INVISIBILE**</dt> </dl> | Il pulsante non è visibile. <br/>      |
| <dl> <dt>**PGF \_ NORMAL**</dt> </dl>    | Il pulsante è in stato normale. <br/>  |
| <dl> <dt>**PGF \_ IN GRIGIO**</dt> </dl>    | Il pulsante è in grigio. <br/>  |
| <dl> <dt>**PGF \_ ESPRESSO**</dt> </dl> | Il pulsante è nello stato premuto. <br/> |
| <dl> <dt>**PGF \_ HOT**</dt> </dl>       | Il pulsante è in stato attivo. <br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





