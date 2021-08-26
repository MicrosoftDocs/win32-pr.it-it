---
title: LVM_GETEDITCONTROL messaggio (Commctrl.h)
description: Ottiene l'handle per il controllo di modifica utilizzato per modificare il testo di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView GetEditControl.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- LVM_GETEDITCONTROL dei messaggi Windows controlli
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
ms.openlocfilehash: 29f7e7ac31b3d429ab32ac6564a47f859f0e5dc2207d991cb580173838a4c366
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968311"
---
# <a name="lvm_geteditcontrol-message"></a>Messaggio LVM \_ GETEDITCONTROL

Ottiene l'handle per il controllo di modifica utilizzato per modificare il testo di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView GetEditControl.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle al controllo di modifica in caso di esito positivo oppure NULL in caso **contrario.**

## <a name="remarks"></a>Commenti

Quando inizia la modifica delle etichette, viene creato, posizionato e inizializzato un controllo di modifica. Prima della visualizzazione, il controllo visualizzazione elenco invia alla finestra padre un codice di notifica [LVN \_ BEGINLABELEDIT.](lvn-beginlabeledit.md)

Per personalizzare la modifica delle etichette, implementare un gestore per [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) e fare in modo che invii un messaggio **LVM \_ GETEDITCONTROL** al controllo visualizzazione elenco. Se un'etichetta viene modificata, il valore restituito sarà un handle per il controllo di modifica. Usare questo handle per personalizzare il controllo di modifica inviando i normali **messaggi EM \_ XXX.**

Quando l'utente completa o annulla la modifica, il controllo di modifica viene eliminato e l'handle non è più valido. È possibile creare una sottoclasse del controllo di modifica, ma non eliminare il controllo. Per annullare la modifica, inviare al controllo visualizzazione elenco un [**messaggio WM \_ CANCELMODE.**](/windows/desktop/winmsg/wm-cancelmode)

L'elemento della visualizzazione elenco in fase di modifica è l'elemento con lo stato attivo corrente, l'elemento nello stato attivo. Per trovare un elemento in base al relativo stato, usare il [**messaggio LVM \_ GETNEXTITEM.**](lvm-getnextitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ListView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

