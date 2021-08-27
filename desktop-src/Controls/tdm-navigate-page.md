---
title: TDM_NAVIGATE_PAGE messaggio (Commctrl.h)
description: Ricrea una finestra di dialogo attività con nuovo contenuto, simulando la funzionalità di una procedura guidata a più pagine.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- TDM_NAVIGATE_PAGE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7894bdc5831af2c1fe2e779679aaab38eab94f976cf9c586dfe64d26a051b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104631"
---
# <a name="tdm_navigate_page-message"></a>Messaggio TDM \_ NAVIGATE \_ PAGE

Ricrea una finestra di dialogo attività con nuovo contenuto, simulando la funzionalità di una procedura guidata a più pagine.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Non usato. Deve essere zero.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) che descrive la finestra di dialogo attività da creare. L'applicazione chiamante deve allocare questa struttura e impostarne i membri. I valori dei membri variano a seconda del tipo di pagina a cui l'utente passa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Per avviare una finestra di dialogo attività della procedura guidata, usare la [**funzione TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) Quando l'utente si sposta usando la procedura guidata, inviare questo messaggio alla finestra di dialogo dell'attività per visualizzare la pagina successiva. Viene creata una nuova finestra di dialogo attività (simile a una nuova pagina) con gli elementi specificati nella struttura a cui punta *lParam*. Al momento della creazione, l'intero contenuto del frame della finestra di dialogo viene eliminato e ricostruito. Di conseguenza, tutte le informazioni sullo stato contenute nei controlli (ad esempio, un indicatore di stato, un pulsante expando o una casella di controllo di verifica) nella finestra di dialogo vengono perse.

Il layout della finestra di dialogo dell'attività potrebbe non riuscire e ciò potrebbe non essere riflessa nel valore restituito. Il valore restituito S OK riflette solo che la finestra di dialogo \_ dell'attività ha ricevuto il messaggio e ha tentato di elaborarlo. Se il layout della finestra di dialogo attività ha esito negativo (la finestra di dialogo dell'attività non può essere visualizzata), la finestra di dialogo verrà chiusa e verrà restituito un **codice HRESULT** alla funzione di callback registrata. Per altre informazioni sulla sintassi della funzione di callback, vedere [*TaskDialogCallbackProc.*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

