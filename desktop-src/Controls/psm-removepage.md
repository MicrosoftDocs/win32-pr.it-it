---
title: Messaggio PSM_REMOVEPAGE (Prsht. h)
description: Rimuove una pagina da una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet RemovePage.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- Controlli di Windows Message PSM_REMOVEPAGE
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874253"
---
# <a name="psm_removepage-message"></a>\_Messaggio REMOVEPAGE di PSM

Rimuove una pagina da una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della pagina da rimuovere.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle HPROPSHEETPAGE della pagina da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione può specificare l'indice o l'handle o entrambi. Se vengono specificati entrambi, *lParam* avrà la precedenza.

L'invio di **PSM \_ REMOVEPAGE** Elimina la pagina della finestra delle proprietà da rimuovere.

Un numero di messaggi e una chiamata di funzione si verificano durante la modifica dell'elenco di pagine da parte della finestra delle proprietà. Durante l'esecuzione di questa azione, il tentativo di modificare l'elenco di pagine avrà risultati imprevedibili. Di conseguenza, non usare il messaggio **PSM \_ REMOVEPAGE** nell'implementazione di [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o durante la gestione delle notifiche e dei messaggi di Windows seguenti.

-   [\_applica PSN](psn-apply.md)
-   [\_KILLACTIVE PSN](psn-killactive.md)
-   [ripristino di PSN \_](psn-reset.md)
-   [seactive PSN \_](psn-setactive.md)
-   [**eliminazione di WM \_**](/windows/desktop/winmsg/wm-destroy)
-   [**\_INITDIALOG WM**](/windows/desktop/dlgbox/wm-initdialog)

Se è necessario modificare una pagina della finestra delle proprietà mentre si gestisce uno di questi messaggi o mentre [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) è in esecuzione, pubblicare un messaggio di Windows privato. L'applicazione non riceverà il messaggio finché il gestore della finestra delle proprietà non avrà terminato le attività. È quindi possibile modificare l'elenco di pagine.

Anche le notifiche seguenti sono interessate dalla modifica della finestra delle proprietà.

-   [\_WIZBACK PSN](psn-wizback.md)
-   [\_WIZNEXT PSN](psn-wiznext.md)

È possibile aggiungere o rimuovere pagine in risposta a queste notifiche, a condizione che venga restituito (tramite DWL \_ MSGRESULT) un valore diverso da zero per specificare la nuova pagina desiderata. Si noti, tuttavia, che se si rimuove una pagina che si trova prima della pagina corrente (con un indice più piccolo rispetto alla pagina corrente), [PSN \_ KILLACTIVE](psn-killactive.md) potrebbe essere inviato alla pagina errata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

