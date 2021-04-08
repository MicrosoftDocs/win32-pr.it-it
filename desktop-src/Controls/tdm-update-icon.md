---
title: Messaggio TDM_UPDATE_ICON (COMmctrl. h)
description: Aggiorna l'icona di una finestra di dialogo attività.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- Controlli di Windows Message TDM_UPDATE_ICON
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964936"
---
# <a name="tdm_update_icon-message"></a>Messaggio dell'icona di \_ aggiornamento TDM \_

Aggiorna l'icona di una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Indica l'elemento icona da aggiornare. Questo parametro deve essere uno dei valori seguenti:



| Valore                                                                                                                                                                   | Significato                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <dt>**icona di TDIE \_ \_ principale**</dt> </dl>       | Icona principale.<br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <dt>**piè di pagina \_ icona TDIe \_**</dt> </dl> | Icona piè di pagina.<br/> |



 

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una stringa (PCWSTR) o handle a un'icona (HICON) da visualizzare. Se *lParam* è **null**, non viene visualizzata alcuna icona, indipendentemente dal valore di *wParam*.

Se il valore di *wParam* è TDIe \_ icona \_ principale e il TDF \_ usare \_ il \_ flag principale HICON è impostato sul membro **dwFlags** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizzata per creare la finestra di dialogo attività, *lParam* deve contenere un handle per un'icona (HICON) da visualizzare.

Se il valore di *wParam* è il piè di pagina dell' \_ icona TDIe \_ e il TDF usa il flag di piè di pagina di \_ \_ HICON \_ è impostato sul membro **dwFlags** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizzata per creare la finestra di dialogo attività, *lParam* deve contenere un handle per un'icona (HICON) da visualizzare.

Se il TDF \_ Usa \_ HICON \_ Main o TDF \_ usare \_ i \_ flag del piè di pagina HICON **non** sono impostati per il membro **dwFlags** , *lParam* deve puntare a una stringa Unicode con terminazione null (PCWSTR) che contiene un identificatore di risorsa valido passato attraverso la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) . L'icona viene visualizzata in base al valore di *wParam*: se il valore è TDIe \_ icona \_ principale, l'icona viene visualizzata nell'intestazione; se il valore è TDIe \_ icona \_ piè di pagina, l'icona viene visualizzata nel piè di pagina. La risorsa deve essere dal modulo delle risorse dell'applicazione (specificato nel membro **HINSTANCE** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) ) oppure, se **HINSTANCE** è **null**, dal modulo Resource del sistema (imageres.dll). Per identificare una risorsa di sistema, usare un identificatore di sistema valido passato attraverso la macro **MAKEINTRESOURCE** o uno dei valori predefiniti seguenti da COMmctrl. h:



| Valore                                                                                                                                                                            | Significato                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <dt>**\_icona di errore TD \_**</dt> </dl>                   | Icona del segno di arresto.<br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <dt>**\_icona di avviso TD \_**</dt> </dl>             | Icona di punto esclamativo.<br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <dt>**\_icona informazioni \_ TD**</dt> </dl> | Lettera minuscola "i" in un'icona a cerchio.<br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <dt>**\_icona scudo \_ TD**</dt> </dl>                | Icona dello scudo di sicurezza.<br/>                  |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Il layout della finestra di dialogo attività con l'icona potrebbe non riuscire e questo potrebbe non essere riflesso nel valore restituito. Un valore restituito di S \_ OK riflette solo il fatto che la finestra di dialogo attività ha ricevuto il messaggio e ha tentato di elaborarlo. Se il layout della finestra di dialogo attività ha esito negativo, la finestra di dialogo verrà chiusa e viene restituito un codice **HRESULT** nella funzione di callback registrata. Per ulteriori informazioni sulla sintassi della funzione di callback, vedere [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

Se la finestra di dialogo attività viene creata senza un piè di pagina (ovvero i membri del piè di pagina appropriati della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usata per creare la finestra di dialogo attività sono **null**) e questo messaggio viene inviato, un piè di pagina non viene aggiunto dinamicamente alla finestra di dialogo attività. Lo stesso vale per l'invio di questo messaggio per aggiornare un'icona di intestazione quando viene creata una finestra di dialogo attività senza un'intestazione. Per aggiungere un'intestazione o un piè di pagina in fase di esecuzione, utilizzare la funzionalità [**TDM \_ Navigate \_ Page**](tdm-navigate-page.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

