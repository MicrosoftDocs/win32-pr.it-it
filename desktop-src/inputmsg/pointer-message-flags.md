---
title: Flag messaggi puntatore
description: Valori utilizzati in diverse macro del puntatore (vedere macro).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302078"
---
# <a name="pointer-message-flags"></a>Flag messaggi puntatore

Valori utilizzati in diverse macro del puntatore (vedere [macro](macros.md)).

<dl> <dt>

<span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica l'arrivo di un nuovo puntatore.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indica che il puntatore continua a esistere. Quando questo flag non è impostato, indica che il puntatore ha un intervallo di rilevamento sinistro.

Questo flag non viene in genere impostato solo quando un puntatore del mouse lascia un intervallo di rilevamento (**POINTER_FLAG_UPDATE** è impostato) o quando un puntatore in contatto con una superficie della finestra lascia un intervallo di rilevamento (**POINTER_FLAG_UP** è impostato).


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica che il puntatore è in contatto con la superficie del digitalizzatore. Quando questo flag non è impostato, indica un puntatore al passaggio del mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Indica un'azione primaria, analoga a un pulsante sinistro del mouse.

Questo flag è impostato in un puntatore tocco quando è in contatto con la superficie del digitalizzatore.

Questo flag è impostato in un puntatore di penna quando è in contatto con la superficie del digitalizzatore senza pulsanti premuti.

Questo flag è impostato su un puntatore del mouse quando il pulsante sinistro del mouse è premuto.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica un'azione secondaria, analoga a un pulsante destro del mouse.

Un puntatore tocco non utilizza questo flag.

Questo flag è impostato in un puntatore di penna quando è in contatto con la superficie del digitalizzatore con il pulsante della penna premuto.

Questo flag è impostato da un puntatore del mouse quando il pulsante destro del mouse è premuto.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Analogo al pulsante della rotellina del mouse.

Un puntatore tocco non utilizza questo flag.

Un puntatore penna non utilizza questo flag.

Questo flag è impostato da un puntatore del mouse quando il pulsante della rotellina del mouse è inattivo.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Analogo a un primo pulsante del mouse esteso (XButton1).

Un puntatore tocco non utilizza questo flag.

Un puntatore penna non utilizza questo flag.

Questo flag è impostato da un puntatore del mouse quando il primo pulsante del mouse esteso (XBUTTON1) è inattivo.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Analogo a un secondo pulsante del mouse esteso (XButton2).

Un puntatore tocco non utilizza questo flag.

Un puntatore penna non utilizza questo flag.

Questo flag è impostato da un puntatore del mouse quando il secondo pulsante del mouse esteso (XBUTTON2) è inattivo.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica che il puntatore è stato designato come puntatore primario. Un puntatore primario è un puntatore singolo che può eseguire azioni oltre a quelle disponibili per i puntatori non primari. Ad esempio, quando un puntatore primario mette in contatto con una superficie della finestra, può fornire alla finestra la possibilità di attivare inviando una WM_POINTERACTIVATE messaggio.

Il puntatore primario viene identificato da tutte le interazioni utente correnti nel sistema (mouse, tocco, penna e così via). Di conseguenza, il puntatore primario potrebbe non essere associato all'app. Il primo contatto in un'interazione multitocco viene impostato come puntatore primario. Una volta identificato un puntatore primario, è necessario rimuovere tutti i contatti prima che un nuovo contatto possa essere identificato come puntatore primario. Per le app che non elaborano l'input del puntatore, solo gli eventi del puntatore primario vengono promossi agli eventi del mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Un suggerimento dal dispositivo di origine indica se il puntatore rappresenta un'interazione intenzionale o accidentale, che è particolarmente rilevante per PT_TOUCH puntatori in cui un'interazione accidentale (ad esempio con il Palm della mano) può attivare l'input. La presenza di questo flag indica che il dispositivo di origine ha una sicurezza elevata che questo input fa parte di un'interazione prevista.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Indica che il puntatore viene ripartito in modo anomalo, ad esempio quando il sistema riceve un input non valido per il puntatore o quando un dispositivo con puntatori attivi viene ripartito in modo improvviso. Se l'applicazione che riceve l'input è in una posizione a tale scopo, deve considerare l'interazione come non completata e invertire gli effetti del puntatore interessato.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

XBUTTON1 e XBUTTON2 sono pulsanti aggiuntivi usati in molti dispositivi mouse. Restituiscono gli stessi dati dei pulsanti del mouse standard.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti](constants.md)
</dt> <dt>

[Macro](macros.md)
</dt> </dl>

 

 





