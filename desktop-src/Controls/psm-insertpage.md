---
title: PSM_INSERTPAGE messaggio (Prsht.h)
description: Inserisce una nuova pagina in una finestra delle proprietà esistente. La pagina può essere inserita in corrispondenza di un indice specificato o dopo una pagina specificata. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro PropSheet InsertPage.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- PSM_INSERTPAGE dei messaggi Windows controllo
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
ms.openlocfilehash: 11c81869b1ca575efa960fc00eea09536ca4b6b2f43a5e637c5dc6a9d7632983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985663"
---
# <a name="psm_insertpage-message"></a>Messaggio \_ INSERTPAGE PSM

Inserisce una nuova pagina in una finestra delle proprietà esistente. La pagina può essere inserita in corrispondenza di un indice specificato o dopo una pagina specificata. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet InsertPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Posizione in cui deve essere inserita la pagina. Impostare questo parametro su **NULL** per impostare la nuova pagina come prima pagina. Per specificare dove inserire la nuova pagina, è possibile passare un indice o l'handle HPROPSHEETPAGE di una pagina esistente.



| Valore                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>index</dt> </dl>            | Se il *parametro wParam* è minore di MAXUSHORT (il valore short integer senza segno più grande), *wParam* specifica l'indice in base zero per la nuova pagina. Ad esempio, per impostare la pagina inserita come terza pagina nella finestra delle proprietà, impostare *wParam* su 2. Per impostarla come prima pagina, *impostare wParam* su 0. Se *wParam ha* un valore maggiore del numero di pagine e minore di MAXUSHORT, la pagina verrà aggiunta.<br/> |
| <dl> <dt></dt><dt>hpageInsertAfter</dt> </dl> | Se si imposta il *parametro wParam* sull'handle HPROPSHEETPAGE di una pagina esistente, la nuova pagina verrà inserita dopo di essa.<br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la pagina da inserire. La pagina deve prima essere creata da una chiamata alla [**funzione CreatePropertySheetPage.**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se la pagina è stata inserita correttamente oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Le pagine dopo il punto di inserimento vengono spostate a destra per contenere la nuova pagina.

La finestra delle proprietà non viene ridimensionata per adattarla alla nuova pagina. Non rendere la nuova pagina più grande della pagina più grande della finestra delle proprietà.

Un numero di messaggi e una chiamata di funzione si verificano mentre la finestra delle proprietà modifica l'elenco di pagine. Durante l'esecuzione di questa azione, il tentativo di modificare l'elenco di pagine avrà risultati imprevedibili. Di conseguenza, non è consigliabile usare il messaggio INSERTPAGE PSM nell'implementazione di \_ [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o durante la gestione delle notifiche e dei Windows seguenti.

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [REIMPOSTAZIONE PSN \_](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

Se è necessario modificare una pagina della finestra delle proprietà durante la gestione di uno di questi messaggi o durante il funzionamento di [*PropSheetPageProc,*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) pubblicare un messaggio Windows privato. L'applicazione non riceverà il messaggio fino a quando il gestore della finestra delle proprietà non avrà completato le attività. È quindi possibile modificare l'elenco di pagine.

Le notifiche seguenti sono interessate anche dalla modifica della finestra delle proprietà.

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

È possibile aggiungere o rimuovere pagine in risposta a queste notifiche, purché si restituisse (tramite DWL MSGRESULT) un valore diverso da zero per specificare la \_ nuova pagina desiderata. Si noti, tuttavia, che se si inserisce una pagina che si trova prima della pagina corrente (con un indice più piccolo rispetto alla pagina corrente), è possibile che [PSN \_ KILLACTIVE](psn-killactive.md) venga inviato alla pagina errata.

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

