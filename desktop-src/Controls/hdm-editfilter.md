---
title: HDM_EDITFILTER messaggio (Commctrl.h)
description: Sposta lo stato attivo per l'input nella casella di modifica quando un pulsante di filtro ha lo stato attivo.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- HDM_EDITFILTER dei messaggi Windows controlli
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
ms.openlocfilehash: 8636c17bfa9043891e5037df79be9c72c1ddc8f3aa2b4d13520f4289205b5099
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006161"
---
# <a name="hdm_editfilter-message"></a>Messaggio \_ HDM EDITFILTER

Sposta lo stato attivo per l'input nella casella di modifica quando un pulsante di filtro ha lo stato attivo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica la colonna da modificare.

</dd> <dt>

*lParam* 
</dt> <dd>

Flag che specifica come gestire le modifiche apportate dall'utente. Usare questo flag per specificare le operazioni da eseguire se l'utente sta modificando il filtro quando viene inviato il messaggio.



| Valore                                                                                                                                      | Significato                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt></dt><dt> **TRUE**</dt> </dl>  | Rimuovere le modifiche apportate dall'utente. <br/> |
| <dl> <dt></dt><dt> **FALSE**</dt> </dl> | Accettare le modifiche apportate dall'utente. <br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un numero intero. Viene eseguito il cast di **LRESULT** a un numero intero che indica **TRUE**(1) o **FALSE**(0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**HDM \_ CLEARFILTER**](hdm-clearfilter.md)
</dt> </dl>

 

 





