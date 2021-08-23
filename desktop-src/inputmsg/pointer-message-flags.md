---
title: Flag di messaggio puntatore
description: Valori usati in diverse macro puntatore (vedere Macro).
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
ms.openlocfilehash: 70d329c6a48eb92f6f50ff49d5543c2aaf5cfc3ce9ef23b48290c7aa029eecf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602352"
---
# <a name="pointer-message-flags"></a>Flag di messaggio puntatore

Valori usati in diverse macro puntatore (vedere [Macro).](macros.md)

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



Indica che il puntatore continua a esistere. Quando questo flag non è impostato, indica che il puntatore ha un intervallo di rilevamento a sinistra.

Questo flag non viene in genere impostato solo quando un puntatore al passaggio del mouse esce dall'intervallo di rilevamento **(è** impostato POINTER_FLAG_UPDATE) o quando un puntatore in contatto con una superficie della finestra lascia l'intervallo di rilevamento **(POINTER_FLAG_UP** è impostato ).


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica che questo puntatore è in contatto con la superficie del digitalizzatore. Quando questo flag non è impostato, indica un puntatore al passaggio del mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Indica un'azione principale, analoga a un pulsante sinistro del mouse verso il basso.

Un puntatore tocco ha questo flag impostato quando è in contatto con la superficie del digitalizzatore.

Un puntatore penna ha questo flag impostato quando è in contatto con la superficie del digitalizzatore senza pulsanti premuti.

Un puntatore del mouse ha questo flag impostato quando il pulsante sinistro del mouse è premuto.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica un'azione secondaria, analoga a un pulsante destro del mouse verso il basso.

Un puntatore tocco non usa questo flag.

Un puntatore della penna ha questo flag impostato quando è in contatto con la superficie del digitalizzatore con il pulsante della penna premuto.

Questo flag è impostato su un puntatore del mouse quando il pulsante destro del mouse è premuto.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Analogamente a un pulsante della rotellina del mouse verso il basso.

Un puntatore tocco non usa questo flag.

Un puntatore penna non usa questo flag.

Un puntatore del mouse ha questo flag impostato quando la rotellina del mouse è in giù.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Analogamente a un primo pulsante esteso del mouse (XButton1) verso il basso.

Un puntatore tocco non usa questo flag.

Un puntatore penna non usa questo flag.

Un puntatore del mouse ha questo flag impostato quando il primo pulsante esteso del mouse (XBUTTON1) è in basso.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Analogamente a un secondo pulsante esteso del mouse (XButton2) verso il basso.

Un puntatore tocco non usa questo flag.

Un puntatore penna non usa questo flag.

Un puntatore del mouse ha questo flag impostato quando il secondo pulsante esteso del mouse (XBUTTON2) è in basso.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica che questo puntatore è stato designato come puntatore primario. Un puntatore primario è un singolo puntatore che può eseguire azioni oltre a quelle disponibili per i puntatori non primari. Ad esempio, quando un puntatore principale contatta la superficie di una finestra, può offrire alla finestra la possibilità di attivarsi inviando un messaggio WM_POINTERACTIVATE finestra.

Il puntatore principale viene identificato da tutte le interazioni dell'utente correnti nel sistema (mouse, tocco, penna e così via). Di conseguenza, il puntatore principale potrebbe non essere associato all'app. Il primo contatto in un'interazione multitocchetto viene impostato come puntatore principale. Una volta identificato un puntatore primario, tutti i contatti devono essere eliminati prima che un nuovo contatto possa essere identificato come puntatore principale. Per le app che non elaborano l'input del puntatore, solo gli eventi del puntatore primario vengono promossi a eventi del mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



L'attendibilità è un suggerimento del dispositivo di origine che indica se il puntatore rappresenta un'interazione intenzionale o accidentale, particolarmente rilevante per i puntatori PT_TOUCH in cui un'interazione accidentale (ad esempio con il palmo della mano) può attivare l'input. La presenza di questo flag indica che il dispositivo di origine è molto sicuro che questo input fa parte di un'interazione prevista.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Indica che il puntatore si sta spostando in modo anomalo, ad esempio quando il sistema riceve un input non valido per il puntatore o quando un dispositivo con puntatori attivi si allontana improvvisamente. Se l'applicazione che riceve l'input è in grado di farlo, deve considerare l'interazione come non completata e invertire gli effetti del puntatore interessato.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

XBUTTON1 e XBUTTON2 sono pulsanti aggiuntivi usati in molti dispositivi mouse. Restituiscono gli stessi dati dei pulsanti standard del mouse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti](constants.md)
</dt> <dt>

[Macro](macros.md)
</dt> </dl>

 

 





