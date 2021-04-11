---
title: Messaggio PSM_SETWIZBUTTONS (Prsht. h)
description: Abilita o Disabilita i pulsanti indietro, avanti e fine in una procedura guidata. È anche possibile usare la \_ macro PropSheet SetWizButtons per inviare il messaggio.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- Controlli di Windows Message PSM_SETWIZBUTTONS
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120114"
---
# <a name="psm_setwizbuttons-message"></a>\_Messaggio SETWIZBUTTONS di PSM

Abilita o Disabilita i pulsanti **indietro**, **Avanti** e **fine** in una procedura guidata. È anche possibile usare la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) per inviare il messaggio.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Impostare questo parametro su PSWIZBF \_ ELEVATIONREQUIRED per visualizzare l'icona con privilegi elevati nei pulsanti specificati in *lParam*. L'icona con privilegi elevati (o l'icona dello scudo UAC) indica che la richiesta di elevazione dei privilegi verrà usata per richiedere l'approvazione o le credenziali dell'utente. Per ulteriori informazioni, vedere [progettazione di applicazioni UAC per Windows Vista]( /previous-versions/bb756973(v=msdn.10)).

> [!Note]  
> La visualizzazione dell'icona dello scudo del controllo dell'account utente è supportata solo in AeroWizards (PSH \_ AEROWIZARD).

 

</dd> <dt>

*lParam* 
</dt> <dd>

Valore che specifica quali pulsanti della finestra delle proprietà sono abilitati. È possibile combinare uno o più dei flag seguenti.



| Valore                                                                                                                                                                                 | Significato                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ indietro**</dt> </dl>                               | Abilita il pulsante **indietro** . Se questo flag non è impostato, il pulsante **indietro** viene visualizzato come disabilitato.<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**\_DISABLEDFINISH PSWIZB**</dt> </dl> | Visualizza un pulsante **fine** disabilitato.<br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**\_fine PSWIZB**</dt> </dl>                         | Visualizza un pulsante **fine** abilitato.<br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ successivo**</dt> </dl>                               | Abilita il pulsante **Avanti**. Se questo flag non è impostato, il pulsante **Avanti** viene visualizzato come disabilitato.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se il gestore di notifiche utilizza [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) per inviare un messaggio **PSM \_ SETWIZBUTTONS** , non eseguire alcuna operazione che influirà sullo stato attivo della finestra fino a quando il gestore non viene restituito. Se, ad esempio, si chiama [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediatamente dopo aver usato **PostMessage** per inviare **PSM \_ SETWIZBUTTONS**, la finestra di messaggio riceve lo stato attivo. Poiché i messaggi inviati non vengono recapitati fino a quando non raggiungono l'intestazione della coda di messaggi, il messaggio **PSM \_ SETWIZBUTTONS** non verrà recapitato fino al termine della procedura guidata per la finestra di messaggio. Di conseguenza, la finestra delle proprietà non sarà in grado di impostare correttamente lo stato attivo per i pulsanti.

Se si invia il \_ messaggio SETWIZBUTTONS di PSM durante la gestione della [notifica \_ seattiva PSN](psn-setactive.md) , usare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) anziché la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) . In caso contrario, i pulsanti non vengono aggiornati correttamente dal sistema. Se si usa la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) per inviare questo messaggio, verrà pubblicato. In qualsiasi altro momento, è possibile usare **SendMessage** per inviare **PSM \_ SETWIZBUTTONS**.

Le procedure guidate visualizzano tre o quattro pulsanti sotto ogni pagina. Questo messaggio viene usato per specificare quali pulsanti sono abilitati. Le procedure guidate di solito visualizzano **indietro**, **Annulla** e un pulsante **Avanti** o **fine** . In genere è possibile abilitare solo il pulsante **Avanti** per la pagina iniziale, **Avanti** e **indietro** per le pagine interne, quindi **tornare** alla pagina di completamento e **terminarla** . Il pulsante **Annulla** è sempre abilitato. In genere, \_ l'impostazione di PSWIZB Finish o PSWIZB \_ DISABLEDFINISH sostituisce il pulsante **Avanti** con il pulsante **fine** . Per visualizzare contemporaneamente i pulsanti **Avanti** e **fine** , impostare il \_ flag PSH WIZARDHASFINISH nel membro **dwFlags** della struttura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) della procedura guidata quando si crea la procedura guidata. Ogni pagina visualizzerà quindi tutti e quattro i pulsanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

