---
title: Messaggio PSM_CANCELTOCLOSE (Prsht. h)
description: Inviato da un'applicazione quando ha eseguito modifiche dopo la notifica di applicazione PSN più recente \_ che non può essere annullata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet CancelToClose.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- Controlli di Windows Message PSM_CANCELTOCLOSE
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120835"
---
# <a name="psm_canceltoclose-message"></a>\_Messaggio CANCELTOCLOSE di PSM

Inviato da un'applicazione quando ha eseguito modifiche dopo la notifica di applicazione [PSN \_ ](psn-apply.md) più recente che non può essere annullata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

**PSM \_ CANCELTOCLOSE** Disabilita il pulsante **Annulla** e modifica il testo del pulsante **OK** in "close".

La maggior parte delle finestre delle proprietà attende di eseguire modifiche irreversibili fino a quando non \_ viene ricevuta una notifica di applicazione PSN. In alcune circostanze, tuttavia, una finestra delle proprietà può apportare modifiche irreversibili al di fuori della sequenza di reimpostazione di PSN \_ Apply/PSN standard \_ . Un esempio è una finestra delle proprietà che contiene un pulsante **modifica** utilizzato per visualizzare una finestra di dialogo per la modifica di una proprietà. Quando l'utente fa clic su **OK** per inviare la modifica, nella pagina della finestra delle proprietà sono disponibili diverse opzioni.

-   Può registrare le modifiche, ma attendere fino a quando non riceve una \_ notifica di applicazione PSN per applicarle. Si tratta dell'approccio preferito.
-   È possibile applicare le modifiche immediatamente dopo aver chiuso la finestra di dialogo, ma ricordare le impostazioni originali. Queste impostazioni possono essere usate per ripristinare lo stato originale se \_ viene ricevuta una notifica di reimpostazione di PSN.
-   Può applicare immediatamente le modifiche e non tentare di ripristinare le impostazioni originali quando riceve una notifica di [ \_ reimpostazione di PSN](psn-reset.md) . Questo approccio non è consigliato, ma potrebbe essere necessario se le modifiche sono troppo ampie perché le altre due opzioni siano pratiche.

Per la terza opzione, le applicazioni devono inviare un messaggio **PSM \_ CANCELTOCLOSE** alla finestra delle proprietà. Indica all'utente che le modifiche apportate con la finestra di dialogo subdialog non possono essere annullate facendo clic sul pulsante **Annulla** .

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





