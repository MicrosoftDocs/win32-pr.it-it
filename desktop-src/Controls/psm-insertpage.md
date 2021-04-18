---
title: Messaggio PSM_INSERTPAGE (Prsht. h)
description: Inserisce una nuova pagina in una finestra delle proprietà esistente. La pagina può essere inserita in corrispondenza di un indice specificato o dopo una pagina specificata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet InsertPage.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- Controlli di Windows Message PSM_INSERTPAGE
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301937"
---
# <a name="psm_insertpage-message"></a>\_Messaggio INSERTPAGE di PSM

Inserisce una nuova pagina in una finestra delle proprietà esistente. La pagina può essere inserita in corrispondenza di un indice specificato o dopo una pagina specificata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Posizione in cui deve essere inserita la pagina. Impostare questo parametro su **null** per impostare la nuova pagina come prima pagina. Per specificare dove deve essere inserita la nuova pagina, è possibile passare un indice o un handle HPROPSHEETPAGE della pagina esistente.



| Valore                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>Indice</dt> di </dl>            | Se il parametro *wParam* è minore di MAXUSHORT (il valore integer short senza segno più grande), il *wParam* specifica l'indice in base zero per la nuova pagina. Ad esempio, per rendere la pagina inserita la terza pagina nella finestra delle proprietà, impostare *wParam* su 2. Per impostarla come prima pagina, impostare *wParam* su 0. Se *wParam* ha un valore maggiore del numero di pagine e minore di MAXUSHORT, la pagina verrà accodata.<br/> |
| <dl> <dt></dt><dt>hpageInsertAfter</dt> </dl> | Se si imposta il parametro *wParam* su un handle HPROPSHEETPAGE della pagina esistente, la nuova pagina verrà inserita dopo questa.<br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la pagina da inserire. La pagina deve prima essere creata da una chiamata alla funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se la pagina è stata inserita correttamente oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Le pagine dopo il punto di inserimento vengono spostate verso destra per adattarsi alla nuova pagina.

La finestra delle proprietà non viene ridimensionata per adattarsi alla nuova pagina. Non rendere la nuova pagina più grande della pagina più grande della finestra delle proprietà.

Un numero di messaggi e una chiamata di funzione si verificano durante la modifica dell'elenco di pagine da parte della finestra delle proprietà. Durante l'esecuzione di questa azione, il tentativo di modificare l'elenco di pagine avrà risultati imprevedibili. Di conseguenza, non usare il messaggio PSM \_ INSERTPAGE nell'implementazione di [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o durante la gestione delle notifiche e dei messaggi di Windows seguenti.

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

È possibile aggiungere o rimuovere pagine in risposta a queste notifiche, a condizione che venga restituito (tramite DWL \_ MSGRESULT) un valore diverso da zero per specificare la nuova pagina desiderata. Si noti, tuttavia, che se si inserisce una pagina che si trova prima della pagina corrente (con un indice più piccolo rispetto alla pagina corrente), [PSN \_ KILLACTIVE](psn-killactive.md) potrebbe essere inviato alla pagina errata.

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

