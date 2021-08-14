---
title: Flag puntatore
description: Valori che possono essere visualizzati nel campo pointerFlags della POINTER_INFO struttura .
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 0ae56ebfc016b0e4497db7cc998753189ce36a87962c0305962800ad133e8bca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482037"
---
# <a name="pointer-flags"></a>Flag puntatore

Valori che possono essere visualizzati nel **campo pointerFlags** della [**POINTER_INFO**](/previous-versions/windows/desktop/api) struttura .

<dl> <dt>

<span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Predefinito


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica l'arrivo di un nuovo puntatore.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indica che il puntatore continua a esistere. Quando questo flag non è impostato, indica che il puntatore ha un intervallo di rilevamento a sinistra.

Questo flag non viene in genere impostato solo quando un puntatore al passaggio del mouse esce dall'intervallo di rilevamento **(è** impostato POINTER_FLAG_UPDATE) o quando un puntatore in contatto con una superficie della finestra lascia l'intervallo di rilevamento **(POINTER_FLAG_UP** è impostato).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica che questo puntatore è in contatto con la superficie del digitalizzatore. Quando questo flag non è impostato, indica un puntatore al passaggio del mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Indica un'azione principale, analoga a un pulsante sinistro del mouse verso il basso.

Un puntatore tocco ha questo flag impostato quando è in contatto con la superficie del digitalizzatore.

Un puntatore penna ha questo flag impostato quando è in contatto con la superficie del digitalizzatore senza pulsanti premuti.

Un puntatore del mouse ha questo flag impostato quando il pulsante sinistro del mouse è premuto.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica un'azione secondaria, analoga a un pulsante destro del mouse verso il basso.

Un puntatore tocco non usa questo flag.

Un puntatore della penna ha questo flag impostato quando è in contatto con la superficie del digitalizzatore con il pulsante della penna premuto.

Questo flag è impostato su un puntatore del mouse quando il pulsante destro del mouse è premuto.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Analogamente a un pulsante della rotellina del mouse verso il basso.

Un puntatore tocco non usa questo flag.

Un puntatore penna non usa questo flag.

Un puntatore del mouse ha questo flag impostato quando la rotellina del mouse è in giù.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Analogamente a un primo pulsante esteso del mouse (XButton1) verso il basso.

Un puntatore tocco non usa questo flag.

Un puntatore penna non usa questo flag.

Un puntatore del mouse ha questo flag impostato quando il primo pulsante esteso del mouse (XBUTTON1) è in basso.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Analogamente a un secondo pulsante esteso del mouse (XButton2) verso il basso.

Un puntatore tocco non usa questo flag.

Un puntatore penna non usa questo flag.

Un puntatore del mouse ha questo flag impostato quando il secondo pulsante esteso del mouse (XBUTTON2) è in basso.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica che questo puntatore è stato designato come puntatore primario. Un puntatore primario è un singolo puntatore che può eseguire azioni oltre a quelle disponibili per i puntatori non primari. Ad esempio, quando un puntatore principale contatta la superficie di una finestra, può offrire alla finestra la possibilità di attivarsi inviando un [**messaggio WM_POINTERACTIVATE**](wm-pointeractivate.md) finestra.

Il puntatore principale viene identificato da tutte le interazioni dell'utente correnti nel sistema (mouse, tocco, penna e così via). Di conseguenza, il puntatore principale potrebbe non essere associato all'app. Il primo contatto in un'interazione multitocchetto viene impostato come puntatore principale. Una volta identificato un puntatore primario, tutti i contatti devono essere eliminati prima che un nuovo contatto possa essere identificato come puntatore principale. Per le app che non elaborano l'input del puntatore, solo gli eventi del puntatore primario vengono promossi a eventi del mouse.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x000004000
</dt> <dt>



L'attendibilità è un suggerimento del dispositivo di origine che indica se il puntatore rappresenta un'interazione intenzionale o accidentale, particolarmente rilevante per i puntatori PT_TOUCH in cui un'interazione accidentale (ad esempio con il palmo della mano) può attivare l'input. La presenza di questo flag indica che il dispositivo di origine è molto sicuro che questo input fa parte di un'interazione prevista.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x000008000
</dt> <dt>



Indica che il puntatore si sta spostando in modo anomalo, ad esempio quando il sistema riceve un input non valido per il puntatore o quando un dispositivo con puntatori attivi si allontana improvvisamente. Se l'applicazione che riceve l'input è in grado di farlo, deve considerare l'interazione come non completata e invertire gli effetti del puntatore interessato.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Indica che il puntatore è stato spostato in uno stato verso il basso; ciò significa che è stato contattato con la superficie del digitalizzatore.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica che si tratta di un aggiornamento semplice che non include modifiche dello stato del puntatore.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Indica che il puntatore è stato spostato in uno stato verso l'alto; ciò significa che il contatto con la superficie del digitalizzatore è terminato.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Indica l'input associato a una rotellina del puntatore. Per i puntatori del mouse, equivale all'azione della rotellina del mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Indica l'input associato a una rotellina del puntatore. Per i puntatori del mouse, equivale all'azione della rotellina di scorrimento orizzontale del mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Indica che questo puntatore è stato acquisito da (associato a) un altro elemento e che l'elemento originale ha perso l'acquisizione (vedere [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Indica che a questo puntatore è associata una trasformazione.


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

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**POINTER_BUTTON_CHANGE_TYPE**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

