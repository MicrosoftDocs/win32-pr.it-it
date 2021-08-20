---
title: PSM_ADDPAGE messaggio (Prsht.h)
description: Aggiunge una nuova pagina alla fine di una finestra delle proprietà esistente. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro PropSheet AddPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- PSM_ADDPAGE dei controlli Windows messaggio
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
ms.openlocfilehash: d17e9da965e5e45c6fe11bc319436c00663fdc6348d3d2457b3c15472f6f3868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169827"
---
# <a name="psm_addpage-message"></a>Messaggio \_ ADDPAGE PSM

Aggiunge una nuova pagina alla fine di una finestra delle proprietà esistente. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet AddPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la pagina da aggiungere. La pagina deve essere stata creata da una chiamata precedente alla [**funzione CreatePropertySheetPage.**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

La nuova pagina non deve essere più grande della pagina più grande attualmente nella finestra delle proprietà perché la finestra delle proprietà non viene ridimensionata per adattarsi alla nuova pagina.

Durante la modifica dell'elenco di pagine nella finestra delle proprietà vengono eseguiti diversi messaggi e una chiamata di funzione. Durante l'esecuzione di questa azione, il tentativo di modificare l'elenco di pagine avrà risultati imprevedibili. Di conseguenza, è consigliabile non usare il messaggio ADDPAGE PSM nell'implementazione di \_ [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o durante la gestione delle notifiche e dei messaggi Windows seguenti.

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [PSN \_ RESET](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

Se è necessario modificare una pagina della finestra delle proprietà mentre si gestisce uno di questi messaggi o mentre [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) è in esecuzione, inviare a se stessi un messaggio Windows privato. L'applicazione non riceverà il messaggio fino a quando la gestione della finestra delle proprietà non avrà completato le attività. È quindi possibile modificare l'elenco delle pagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

