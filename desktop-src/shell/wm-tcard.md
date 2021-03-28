---
description: Inviato a un'applicazione che ha avviato una carta di formazione con la Guida di Windows.
title: Messaggio WM_TCARD (winuser. h)
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
ms.openlocfilehash: 5eb6a3b5a4b840549b75e152f0420bfa055138c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227422"
---
# <a name="wm_tcard-message"></a>\_Messaggio TCARD WM

Inviato a un'applicazione che ha avviato una carta di formazione con la Guida di Windows. Il messaggio informa l'applicazione quando l'utente fa clic su un pulsante modificabile. Un'applicazione avvia una scheda di training specificando il \_ comando help TCARD in una chiamata alla funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*idAction* 
</dt> <dd>

Valore che indica l'azione eseguita dall'utente. Può corrispondere a uno dei valori seguenti.

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span id="IDABORT"></span><span id="idabort"></span>**IDABORT**


</dt> <dd>

L'utente ha fatto clic su un pulsante **Interrompi** modificabile.

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**


</dt> <dd>

L'utente ha fatto clic su un pulsante **Annulla** modificabile.

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**


</dt> <dd>

L'utente ha chiuso la scheda di training.

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**


</dt> <dd>

L'utente ha fatto clic su un pulsante della **Guida** di Windows modificabile.

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**


</dt> <dd>

L'utente ha fatto clic su un pulsante **Ignora** modificabile.

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span id="IDOK"></span><span id="idok"></span>**IDOK**


</dt> <dd>

L'utente ha fatto clic su un pulsante **OK** modificabile.

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span id="IDNO"></span><span id="idno"></span>**IDNO**


</dt> <dd>

L'utente ha fatto clic su un pulsante **non** modificabile.

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**


</dt> <dd>

L'utente ha fatto clic su un pulsante di **ripetizione dei tentativi** modificabile.

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**Guida \_ ai \_ dati di TCARD**


</dt> <dd>

L'utente ha fatto clic su un pulsante modificabile. Il parametro *dwActionData* contiene un valore long integer specificato dall'autore della guida.

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**Guida \_ TCARD \_ altro \_ chiamante**


</dt> <dd>

Un'altra applicazione ha richiesto le schede di formazione.

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span id="IDYES"></span><span id="idyes"></span>**IDYES**


</dt> <dd>

L'utente ha fatto clic su un pulsante **Sì** modificabile.

</dd> </dl> </dd> <dt>

*dwActionData* 
</dt> <dd>

Se *idAction* specifica Help \_ TCARD \_ data, questo parametro è un valore **Long** specificato dall'autore della guida. In caso contrario, questo parametro è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato; usare zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

 




