---
title: Messaggio TDM_NAVIGATE_PAGE (COMmctrl. h)
description: Ricrea una finestra di dialogo attività con nuovo contenuto, simulando la funzionalità di una procedura guidata a più pagine.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- Controlli di Windows Message TDM_NAVIGATE_PAGE
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
ms.openlocfilehash: 56fc86e0e4fe457a43e035ed5d568e91303c7fcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964849"
---
# <a name="tdm_navigate_page-message"></a>Messaggio della pagina di \_ spostamento TDM \_

Ricrea una finestra di dialogo attività con nuovo contenuto, simulando la funzionalità di una procedura guidata a più pagine.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Non usato. Deve essere zero.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) che descrive la finestra di dialogo attività da creare. L'applicazione chiamante deve allocare questa struttura e impostare i relativi membri. I valori dei membri variano a seconda del tipo di pagina a cui l'utente accede.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Per avviare una finestra di dialogo attività procedura guidata, usare la funzione [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Quando l'utente accede tramite la procedura guidata, invia questo messaggio alla finestra di dialogo attività per visualizzare la pagina successiva. Viene creata una nuova finestra di dialogo attività (simile a una nuova pagina) con gli elementi specificati nella struttura a cui punta *lParam*. Al momento della creazione, l'intero contenuto del frame della finestra di dialogo viene eliminato e ricostruito. Di conseguenza, tutte le informazioni sullo stato contenute nei controlli (ad esempio, un indicatore di stato, un pulsante expando o una casella di controllo di verifica) nella finestra di dialogo andranno perse.

Il layout della finestra di dialogo attività potrebbe non riuscire e questo potrebbe non essere riflesso nel valore restituito. Un valore restituito di S \_ OK riflette solo il fatto che la finestra di dialogo attività ha ricevuto il messaggio e ha tentato di elaborarlo. Se il layout della finestra di dialogo attività ha esito negativo (non è possibile visualizzare la finestra di dialogo attività), la finestra di dialogo verrà chiusa e viene restituito un codice **HRESULT** nella funzione di callback registrata. Per ulteriori informazioni sulla sintassi della funzione di callback, vedere [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

