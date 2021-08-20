---
title: PSM_CANCELTOCLOSE messaggio (Prsht.h)
description: Inviato da un'applicazione quando sono state apportate modifiche dopo la notifica PSN APPLY più recente \_ che non può essere annullata. È possibile inviare questo messaggio in modo esplicito o tramite la macro PropSheet \_ CancelToClose.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- PSM_CANCELTOCLOSE dei messaggi Windows controlli
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
ms.openlocfilehash: 65c37c46e1232d8f99b8666e86058a13b840fbc975d94355d75ef40a810ee23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169817"
---
# <a name="psm_canceltoclose-message"></a>Messaggio \_ CANCELTOCLOSE PSM

Inviato da un'applicazione quando sono state apportate modifiche dopo la notifica [PSN \_ APPLY](psn-apply.md) più recente che non può essere annullata. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**PropSheet \_ CancelToClose.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose)

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

**PSM \_ CANCELTOCLOSE** disabilita il **pulsante Annulla** e modifica il testo del **pulsante OK** in "Chiudi".

La maggior parte delle finestre delle proprietà attende di eseguire modifiche irreversibili fino a quando non viene ricevuta una notifica PSN \_ APPLY. In alcuni casi, tuttavia, una finestra delle proprietà può apportare modifiche irreversibili all'esterno della sequenza STANDARD PSN \_ APPLY/PSN \_ RESET. Un esempio è una finestra delle proprietà che contiene un **pulsante** Modifica usato per visualizzare una finestra di dialogo secondaria per la modifica di una proprietà. Quando l'utente fa **clic su OK** per inviare la modifica, nella pagina della finestra delle proprietà sono disponibili diverse opzioni.

-   Può registrare le modifiche, ma attendere che riceva una notifica PSN \_ APPLY per applicarle. Questo è l'approccio preferito.
-   Può applicare le modifiche immediatamente dopo l'uscita dalla finestra di dialogo secondaria, ma ricordare le impostazioni originali. Queste impostazioni possono essere usate per ripristinare lo stato originale se viene ricevuta una notifica PSN \_ RESET.
-   Può applicare le modifiche immediatamente e non tentare di ripristinare le impostazioni originali quando riceve una notifica [PSN \_ RESET.](psn-reset.md) Questo approccio non è consigliato, ma può essere necessario se le modifiche sono troppo di vasta portata perché le altre due opzioni siano pratiche.

Per la terza opzione, le applicazioni devono inviare un **messaggio PSM \_ CANCELTOCLOSE** alla finestra delle proprietà. Indica all'utente che le modifiche apportate con la finestra di dialogo secondaria non possono essere annullate facendo clic sul **pulsante** Annulla.

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





