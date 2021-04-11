---
title: Messaggio PSM_ADDPAGE (Prsht. h)
description: Aggiunge una nuova pagina alla fine di una finestra delle proprietà esistente. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro PropSheet di AddPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- Controlli di Windows Message PSM_ADDPAGE
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874258"
---
# <a name="psm_addpage-message"></a>\_Messaggio ADDPAGE di PSM

Aggiunge una nuova pagina alla fine di una finestra delle proprietà esistente. È possibile inviare questo messaggio in modo esplicito o usando la macro [**PropSheet di \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la pagina da aggiungere. La pagina deve essere stata creata da una chiamata precedente alla funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

La nuova pagina non deve essere maggiore della pagina più grande attualmente nella finestra delle proprietà perché la finestra delle proprietà non viene ridimensionata per adattarsi alla nuova pagina.

Un numero di messaggi e una chiamata di funzione si verificano durante la modifica dell'elenco di pagine da parte della finestra delle proprietà. Durante l'esecuzione di questa azione, il tentativo di modificare l'elenco di pagine avrà risultati imprevedibili. Di conseguenza, non è consigliabile usare il \_ messaggio ADDPAGE di PSM nell'implementazione di [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o durante la gestione delle notifiche e dei messaggi di Windows seguenti.

-   [\_applica PSN](psn-apply.md)
-   [\_KILLACTIVE PSN](psn-killactive.md)
-   [ripristino di PSN \_](psn-reset.md)
-   [seactive PSN \_](psn-setactive.md)
-   [**eliminazione di WM \_**](/windows/desktop/winmsg/wm-destroy)
-   [**\_INITDIALOG WM**](/windows/desktop/dlgbox/wm-initdialog)

Se è necessario modificare una pagina della finestra delle proprietà mentre si gestisce uno di questi messaggi o mentre [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) è in esecuzione, pubblicare un messaggio di Windows privato. L'applicazione non riceverà il messaggio finché il gestore della finestra delle proprietà non avrà terminato le attività. È quindi possibile modificare l'elenco di pagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

