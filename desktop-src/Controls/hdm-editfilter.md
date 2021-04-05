---
title: Messaggio HDM_EDITFILTER (COMmctrl. h)
description: Sposta lo stato attivo per l'input nella casella di modifica quando un pulsante di filtro dispone dello stato attivo.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- Controlli di Windows Message HDM_EDITFILTER
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733c79bf747d3b55aa8dd38eb8fad8fdc83601e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742282"
---
# <a name="hdm_editfilter-message"></a>\_Messaggio HDM EDITFILTER

Sposta lo stato attivo per l'input nella casella di modifica quando un pulsante di filtro dispone dello stato attivo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica la colonna da modificare.

</dd> <dt>

*lParam* 
</dt> <dd>

Flag che specifica come gestire le modifiche apportate alla modifica dell'utente. Utilizzare questo flag per specificare le operazioni da eseguire se l'utente è in corso di modifica del filtro quando viene inviato il messaggio.



| Valore                                                                                                                                      | Significato                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt></dt>Valore <dt> **true**</dt> </dl>  | Annullare le modifiche apportate dall'utente. <br/> |
| <dl> <dt></dt><dt> **False**</dt> </dl> | Accettare le modifiche apportate dall'utente. <br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un Integer. Viene eseguito il cast di **LRESULT** a un Integer che indica **true**(1) o **false**(0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CLEARFILTER HDM**](hdm-clearfilter.md)
</dt> </dl>

 

 





