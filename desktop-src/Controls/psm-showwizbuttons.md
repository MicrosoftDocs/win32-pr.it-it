---
title: PSM_SHOWWIZBUTTONS messaggio (Prsht.h)
description: Mostra o nasconde i pulsanti in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro PropSheet ShowWizButtons.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- PSM_SHOWWIZBUTTONS dei messaggi Windows controlli
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
ms.openlocfilehash: 86bbad4d6f0ce8a084709c04110d093e4d79b806226bdc1fa651278b4054fa8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088481"
---
# <a name="psm_showwizbuttons-message"></a>Messaggio PSM \_ SHOWWIZBUTTONS

Mostra o nasconde i pulsanti in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet ShowWizButtons.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o più dei valori seguenti che specificano i pulsanti della finestra delle proprietà da visualizzare. Se il valore di un pulsante è incluso sia in questo parametro che *in lParam*, viene visualizzato.



| Valore                                                                                                                                                                                 | Significato                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ BACK**</dt> </dl>                               | Pulsante  Indietro.<br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIZB \_ CANCEL**</dt> </dl>                         | Pulsante  Annulla.<br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | Pulsante **Fine.**<br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ FINISH**</dt> </dl>                         | Pulsante **Fine.**<br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ NEXT**</dt> </dl>                               | Pulsante  Avanti.<br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <dt>**PSWIZB \_ SHOW**</dt> </dl>                               | Impostare solo questo flag (definito come zero) per nascondere tutti i pulsanti specificati in *lParam*.<br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <dt>**PSWIZB \_ RESTORE**</dt> </dl>                      | Non implementato.<br/>                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uno o più degli stessi valori utilizzati in *wParam*, specificando i pulsanti interessati da questa chiamata. Se il valore di un pulsante viene visualizzato in questo parametro ma non in *wParam*, il pulsante è nascosto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le procedure guidate visualizzano tre o quattro pulsanti sotto ogni pagina. Questo messaggio viene usato per specificare quali pulsanti sono visibili. Le procedure guidate visualizzano in **genere Indietro,** **Annulla** e un **pulsante** Avanti **o** Fine. Il **pulsante** Annulla è sempre visibile.

In genere, **impostare PSWIZB \_ FINISH** o **PSWIZB \_ DISABLEDFINISH** per sostituire il **pulsante** Avanti con un **pulsante** Fine. Per visualizzare  **i** pulsanti Avanti e Fine contemporaneamente, impostare il flag **PSH \_ WIZARDHASFINISH** nel membro **dwFlags** della struttura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) quando si crea la procedura guidata. Ogni pagina visualizza quindi tutti e quattro i pulsanti: **Indietro,** **Avanti,** **Annulla** e **Fine.**

Se si usa la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) per inviare questo messaggio, verrà pubblicato. In qualsiasi altro momento, è possibile usare [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per **inviare PSM \_ SHOWWIZBUTTONS**.

Se il gestore di notifica usa [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) per inviare un **messaggio \_ SHOWWIZBUTTONS PSM,** non eseguire alcuna operazione che influisca sull'attivazione della finestra fino alla fine del gestore. Ad esempio, se si chiama [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediatamente dopo aver utilizzato **PostMessage** per **inviare PSM \_ SHOWWIZBUTTONS,** la finestra di messaggio riceverà lo stato attivo. Poiché i messaggi inseriti non vengono recapitati fino a quando non raggiungono l'inizio della coda di messaggi, il messaggio **PSM \_ SHOWWIZBUTTONS** non verrà recapitato fino a quando la procedura guidata non ha perso lo stato attivo nella finestra di messaggio. Di conseguenza, la finestra delle proprietà non sarà in grado di impostare correttamente lo stato attivo per i pulsanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

