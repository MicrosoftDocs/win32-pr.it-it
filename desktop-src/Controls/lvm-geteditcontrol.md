---
title: Messaggio LVM_GETEDITCONTROL (COMmctrl. h)
description: Ottiene l'handle per il controllo di modifica utilizzato per modificare il testo di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetEditControl di ListView.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- Controlli di Windows Message LVM_GETEDITCONTROL
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047861"
---
# <a name="lvm_geteditcontrol-message"></a>\_Messaggio GETEDITCONTROL LVM

Ottiene l'handle per il controllo di modifica utilizzato per modificare il testo di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetEditControl di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo di modifica, se ha esito positivo, oppure **null** in caso contrario.

## <a name="remarks"></a>Commenti

Quando viene avviata la modifica dell'etichetta, viene creato, posizionato e inizializzato un controllo di modifica. Prima che venga visualizzato, il controllo elenco-visualizzazione Invia la finestra padre di un codice di notifica [ \_ BEGINLABELEDIT LVN](lvn-beginlabeledit.md) .

Per personalizzare la modifica delle etichette, implementare un gestore per [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) e inviare un messaggio **LVM \_ GETEDITCONTROL** al controllo List-View. Se è in corso la modifica di un'etichetta, il valore restituito sarà un handle per il controllo di modifica. Utilizzare questo handle per personalizzare il controllo di modifica inviando i normali messaggi **em \_ xxx** .

Quando l'utente completa o Annulla la modifica, il controllo di modifica viene eliminato definitivamente e l'handle non è più valido. È possibile sottoclassare il controllo di modifica, ma non eliminarlo. Per annullare la modifica, inviare il controllo elenco-visualizzazione di un messaggio [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) .

L'elemento della visualizzazione elenco da modificare è l'elemento attualmente attivo, ovvero l'elemento nello stato attivo. Per trovare un elemento in base al relativo stato, usare il messaggio [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GetEditControl ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

