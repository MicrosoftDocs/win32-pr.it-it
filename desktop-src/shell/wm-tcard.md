---
description: Inviato a un'applicazione che ha avviato una scheda di training con Windows guida.
title: WM_TCARD messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85435c5674ad6a2ac4e05edaa5d450dc61de9eac6dae05d3b19662aec91a61f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856986"
---
# <a name="wm_tcard-message"></a>Messaggio \_ TCARD WM

Inviato a un'applicazione che ha avviato una scheda di training con Windows guida. Il messaggio informa l'applicazione quando l'utente fa clic su un pulsante autorevole. Un'applicazione avvia una scheda di training specificando il comando HELP \_ TCARD in una chiamata alla [**funzione WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)

## <a name="parameters"></a>Parametri

<dl> <dt>

*idAction* 
</dt> <dd>

Valore che indica l'azione eseguita dall'utente. Può essere uno dei valori seguenti.

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span id="IDABORT"></span><span id="idabort"></span>**IDABORT**


</dt> <dd>

L'utente ha fatto clic su un pulsante **Abort (Interrompi)** autorevole.

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span id="IDCANCEL"></span><span id="idcancel"></span>**Idcancel**


</dt> <dd>

L'utente ha fatto clic su un pulsante **Annulla** autorevole.

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**


</dt> <dd>

L'utente ha chiuso la scheda di training.

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**


</dt> <dd>

L'utente ha fatto clic su un Windows **guida.**

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**


</dt> <dd>

L'utente ha fatto clic su un **pulsante Ignora** autorevole.

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span id="IDOK"></span><span id="idok"></span>**Idok**


</dt> <dd>

L'utente ha fatto clic su un pulsante **OK** autorevole.

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span id="IDNO"></span><span id="idno"></span>**Idno**


</dt> <dd>

L'utente ha fatto clic su un pulsante **No autorevole.**

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**


</dt> <dd>

L'utente ha fatto clic su un pulsante **Riprova** autorevole.

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**HELP \_ TCARD \_ DATA**


</dt> <dd>

L'utente ha fatto clic su un pulsante autorevole. Il *parametro dwActionData* contiene un long integer specificato dall'autore della Guida.

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**HELP \_ TCARD \_ OTHER \_ CALLER**


</dt> <dd>

Un'altra applicazione ha richiesto schede di training.

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span id="IDYES"></span><span id="idyes"></span>**IDYES**


</dt> <dd>

L'utente ha fatto clic su un **pulsante Sì** autorevole.

</dd> </dl> </dd> <dt>

*dwActionData* 
</dt> <dd>

Se *idAction* specifica HELP \_ TCARD \_ DATA, questo parametro è un **valore long** specificato dall'autore della Guida. In caso contrario, questo parametro è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato. usare zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



 

 




