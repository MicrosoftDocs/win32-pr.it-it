---
title: TDM_UPDATE_ICON messaggio (Commctrl.h)
description: Aggiorna l'icona di una finestra di dialogo attività.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- TDM_UPDATE_ICON dei controlli Windows messaggio
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
ms.openlocfilehash: 644e214a3edbc420a7aed3d4ba5bc688e6b7af1ed097be325006bb9481e00620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104501"
---
# <a name="tdm_update_icon-message"></a>Messaggio ICONA DI AGGIORNAMENTO TDM \_ \_

Aggiorna l'icona di una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Indica l'elemento icona da aggiornare. Questo parametro deve essere uno dei valori seguenti:



| Valore                                                                                                                                                                   | Significato                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <dt>**ICONA TDIE \_ \_ MAIN**</dt> </dl>       | Icona principale.<br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <dt>**PIÈ DI PAGINA ICONA TDIE \_ \_**</dt> </dl> | Icona piè di pagina.<br/> |



 

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa (PCWSTR) o handle a un'icona (HICON) da visualizzare. Se *lParam* è **NULL,** non viene visualizzata alcuna icona, indipendentemente dal valore di *wParam*.

Se il valore di *wParam* è TDIE ICON MAIN e il flag TDF USE HICON MAIN è impostato sul membro dwFlags della struttura TASKDIALOGCONFIG usata per creare la finestra di dialogo dell'attività, lParam deve contenere un handle per \_ \_ \_ \_ un'icona \_ (HICON)  [](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)  da visualizzare.

Se il valore di *wParam* è TDIE ICON FOOTER e il flag TDF USE HICON FOOTER è impostato sul membro dwFlags della struttura TASKDIALOGCONFIG usata per creare la finestra di dialogo dell'attività, lParam deve contenere un handle per \_ \_ \_ \_ un'icona \_ (HICON)  [](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)  da visualizzare.

Se i flag TDF USE HICON MAIN o TDF USE HICON FOOTER non sono impostati nel membro \_ \_ \_ \_ \_ \_ **dwFlags,** *lParam*  [](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) deve puntare a una stringa Unicode con terminazione Null (PCWSTR) contenente un identificatore di risorsa valido passato tramite la macro MAKEINTRESOURCE. L'icona viene visualizzata in base al valore di *wParam*: se il valore è TDIE ICON MAIN, l'icona viene visualizzata nell'intestazione. Se il valore è TDIE ICON FOOTER, l'icona viene visualizzata nel piè di \_ \_ \_ \_ pagina. La risorsa deve essere dal modulo di risorse dell'applicazione (specificato nel membro **hInstance** della struttura [**TASKDIALOGCONFIG)**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) o se **hInstance** è **NULL** dal modulo di risorse del sistema (imageres.dll). Per identificare una risorsa di sistema, usare un identificatore di sistema valido passato tramite la macro **MAKEINTRESOURCE** o uno dei valori predefiniti seguenti da commctrl.h:



| Valore                                                                                                                                                                            | Significato                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <dt>**ICONA DI ERRORE TD \_ \_**</dt> </dl>                   | Icona del segno di arresto.<br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <dt>**ICONA \_ AVVISO TD \_**</dt> </dl>             | Icona del punto esclamativo.<br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <dt>**ICONA \_ INFORMAZIONI TD \_**</dt> </dl> | Lettera minuscola "i" in un'icona a forma di cerchio.<br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <dt>**ICONA DELLO SCHERMO TD \_ \_**</dt> </dl>                | Icona dello schermo di sicurezza.<br/>                  |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Il layout della finestra di dialogo dell'attività con l'icona potrebbe non riuscire e questo potrebbe non essere riflessa nel valore restituito. Il valore restituito S OK riflette solo che la finestra di dialogo \_ dell'attività ha ricevuto il messaggio e ha tentato di elaborarlo. Se il layout della finestra di dialogo dell'attività ha esito negativo, la finestra di dialogo verrà chiusa e verrà restituito un **codice HRESULT** alla funzione di callback registrata. Per altre informazioni sulla sintassi della funzione di callback, vedere [*TaskDialogCallbackProc.*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)

Se la finestra di dialogo attività viene creata senza piè di pagina, ovvero i membri del piè di pagina appropriati della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usata per creare la finestra di dialogo attività sono **NULL** e questo messaggio viene inviato, non viene aggiunto dinamicamente un piè di pagina alla finestra di dialogo attività. Lo stesso vale per l'invio di questo messaggio per aggiornare un'icona di intestazione quando viene creata una finestra di dialogo attività senza intestazione. Per aggiungere un'intestazione o un piè di pagina in fase di esecuzione, usare la [**funzionalità \_ TDM NAVIGATE \_ PAGE.**](tdm-navigate-page.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

