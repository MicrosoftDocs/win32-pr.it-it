---
title: Messaggio PSM_SHOWWIZBUTTONS (Prsht. h)
description: Consente di visualizzare o nascondere i pulsanti in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet ShowWizButtons.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- Controlli di Windows Message PSM_SHOWWIZBUTTONS
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e8d1fc54d556240ef3fa6d6b6185a669978b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301181"
---
# <a name="psm_showwizbuttons-message"></a>\_Messaggio SHOWWIZBUTTONS di PSM

Consente di visualizzare o nascondere i pulsanti in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o più dei valori seguenti che specificano i pulsanti della finestra delle proprietà da visualizzare. Se il valore di un pulsante è incluso sia in questo parametro che in *lParam*, viene visualizzato.



| Valore                                                                                                                                                                                 | Significato                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ indietro**</dt> </dl>                               | Pulsante **indietro** .<br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**\_annullamento PSWIZB**</dt> </dl>                         | Pulsante **Annulla** .<br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**\_DISABLEDFINISH PSWIZB**</dt> </dl> | Pulsante **fine** .<br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**\_fine PSWIZB**</dt> </dl>                         | Pulsante **fine** .<br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ successivo**</dt> </dl>                               | Pulsante **Avanti** .<br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <dt>**PSWIZB \_ Show**</dt> </dl>                               | Impostare solo questo flag (definito come zero) per nascondere tutti i pulsanti specificati in *lParam*.<br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <dt>**\_ripristino PSWIZB**</dt> </dl>                      | Non implementato.<br/>                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uno o più degli stessi valori utilizzati in *wParam*, che specificano quali pulsanti sono interessati da questa chiamata. Se il valore di un pulsante viene visualizzato in questo parametro ma non in *wParam*, il pulsante è nascosto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le procedure guidate visualizzano tre o quattro pulsanti sotto ogni pagina. Questo messaggio viene usato per specificare quali pulsanti sono visibili. Le procedure guidate di solito visualizzano **indietro**, **Annulla** e un pulsante **Avanti** o **fine** . Il pulsante **Annulla** è sempre visibile.

In genere, **impostare \_ PSWIZB Finish** o **PSWIZB \_ DISABLEDFINISH** per sostituire il pulsante **Avanti** con il pulsante **fine** . Per visualizzare contemporaneamente i pulsanti **Avanti** e **fine** , impostare il flag **PSH \_ WIZARDHASFINISH** nel membro **dwFlags** della struttura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) quando si crea la procedura guidata. Ogni pagina visualizzerà quindi tutti i quattro pulsanti: **indietro**, **Avanti**, **Annulla** e **fine**.

Se si usa la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) per inviare questo messaggio, verrà pubblicato. In qualsiasi altro momento, è possibile usare [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per inviare **PSM \_ SHOWWIZBUTTONS**.

Se il gestore di notifiche utilizza [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) per inviare un messaggio **PSM \_ SHOWWIZBUTTONS** , non eseguire alcuna operazione che influirà sullo stato attivo della finestra fino a quando il gestore non viene restituito. Se, ad esempio, si chiama [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediatamente dopo aver usato **PostMessage** per inviare **PSM \_ SHOWWIZBUTTONS**, la finestra di messaggio riceve lo stato attivo. Poiché i messaggi inviati non vengono recapitati fino a quando non raggiungono l'intestazione della coda di messaggi, il messaggio **PSM \_ SHOWWIZBUTTONS** non verrà recapitato fino al termine della procedura guidata per la finestra di messaggio. Di conseguenza, la finestra delle proprietà non sarà in grado di impostare correttamente lo stato attivo per i pulsanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

