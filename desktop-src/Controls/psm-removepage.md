---
title: PSM_REMOVEPAGE messaggio (Prsht.h)
description: Rimuove una pagina da una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la macro PropSheet \_ RemovePage.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- PSM_REMOVEPAGE di controllo Windows messaggio
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
ms.openlocfilehash: 5e1493fe8a4f6a3b8e8ac93103d27e67ae984221bdc6efd584130879d17249c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088611"
---
# <a name="psm_removepage-message"></a>Messaggio \_ REMOVEPAGE PSM

Rimuove una pagina da una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**PropSheet \_ RemovePage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage)

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

Un'applicazione può specificare l'indice, l'handle o entrambi. Se vengono specificati entrambi, *lParam* ha la precedenza.

**L'invio di \_ REMOVEPAGE PSM** elimina definitivamente la pagina della finestra delle proprietà che viene rimossa.

Un numero di messaggi e una chiamata di funzione si verificano mentre la finestra delle proprietà modifica l'elenco di pagine. Durante l'esecuzione di questa azione, il tentativo di modificare l'elenco di pagine avrà risultati imprevedibili. Di conseguenza, non è consigliabile usare il messaggio **\_ REMOVEPAGE PSM** nell'implementazione di [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o durante la gestione delle notifiche e dei messaggi Windows seguenti.

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [REIMPOSTAZIONE PSN \_](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

Se è necessario modificare una pagina della finestra delle proprietà durante la gestione di uno di questi messaggi o durante il funzionamento di [*PropSheetPageProc,*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) pubblicare un messaggio Windows privato. L'applicazione non riceverà il messaggio fino al termine delle attività da parte del gestore della finestra delle proprietà. È quindi possibile modificare l'elenco di pagine.

Le notifiche seguenti sono interessate anche dalla modifica della finestra delle proprietà.

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

È possibile aggiungere o rimuovere pagine in risposta a queste notifiche, purché si restituisse (tramite DWL MSGRESULT) un valore diverso da zero per specificare la \_ nuova pagina desiderata. Si noti, tuttavia, che se si rimuove una pagina che si trova prima della pagina corrente (con un indice inferiore rispetto alla pagina corrente), è possibile che [PSN \_ KILLACTIVE](psn-killactive.md) venga inviato alla pagina errata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

