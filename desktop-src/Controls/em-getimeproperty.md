---
title: EM_GETIMEPROPERTY messaggio (Richedit.h)
description: Recupera la proprietà e le funzionalità dell'IME (Input Method Editor) associato alle impostazioni locali di input correnti.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- EM_GETIMEPROPERTY di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b96ad255d9d68cc76869b6f9163aedf549da19ff0c3ddba756f8da42267135c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541111"
---
# <a name="em_getimeproperty-message"></a>Messaggio EM \_ GETIMEPROPERTY

Recupera la proprietà e le funzionalità dell'IME (Input Method Editor) associato alle impostazioni locali di input correnti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il tipo di informazioni sulla proprietà da recuperare. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                     | Significato                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <dt>**PROPRIETÀ \_ IGP**</dt> </dl>                | Informazioni sulle proprietà.<br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <dt>**CONVERSIONE IGP \_**</dt> </dl>          | Funzionalità di conversione. <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <dt>**FRASE \_ IGP**</dt> </dl>                | Funzionalità della modalità frase. <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <dt>**Interfaccia \_ utente IGP**</dt> </dl>                                  | Funzionalità dell'interfaccia utente. <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <dt>**IGP \_ SETCOMPSTR**</dt> </dl>          | Funzionalità della stringa di composizione. <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <dt>**IGP \_ SELECT**</dt> </dl>                      | Funzionalità di ereditarietà della selezione. <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <dt>**IGP \_ GETIMEVERSION**</dt> </dl> | Recupera il numero di versione del sistema per il quale è stato creato l'IME specificato. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore della proprietà o della funzionalità, a seconda del valore del *parametro lParam.* Per ulteriori informazioni, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Se *wParam* è IGP \_ PROPERTY, restituisce uno o più dei valori seguenti.



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROPRIETÀ IME \_ \_ AT \_ CARET                | Se impostata, la finestra di conversione si trova nella posizione del cursore. Se deselezionata, la finestra si trova vicino alla posizione del cursore.                                                                                                                                                                  |
| INTERFACCIA UTENTE SPECIALE DI IME \_ PROP \_ \_              | Se impostato, L'IME ha un'interfaccia utente non standard. L'applicazione non deve disegnare nella finestra IME.                                                                                                                                                                  |
| IME \_ PROP \_ CANDLIST \_ INIZIA DA \_ \_ 1 | Se impostato, le stringhe nell'elenco dei candidati vengono numerate a partire da 1. Se è deselezionata, le stringhe iniziano da zero.                                                                                                                                                                |
| IME \_ PROP \_ UNICODE                  | Se impostato, l'IME viene visualizzato come UnicodeIME. Il sistema e l'IME comunicheranno tramite l'interfaccia UnicodeIME. Se non è chiaro, IME userà l'interfaccia ANSI per comunicare con il sistema.                                                                    |
| PROPRIETÀ IME \_ \_ COMPLETATA \_ \_ ALL'ANNULLAMENTO DELLA SELEZIONE   | Se impostata, la finestra di conversione si trova nella posizione del cursore. Se deselezionata, la finestra si trova vicino alla posizione del cursore.                                                                                                                                                                  |
| IME \_ PROP \_ ACCEPT \_ WIDE \_ VKEY       | Se impostato, l'IME elabora il valore Unicode inserito che deriva dalla [**funzione SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) usando VK \_ PACKET. Se non è chiaro, l'IME potrebbe non elaborare il codice Unicode inserito e il valore Unicode inserito potrebbe essere inviato direttamente all'applicazione. |



 

Se *wParam è* un'interfaccia utente IGP, \_ restituisce uno o più dei valori seguenti.



| Requisito | Valore |
|-----------------|-------------------------------------------------------------------------------------------------------|
| UI \_ CAP \_ 2700   | Supporta valori di escape del testo 0 o 2700. Per altre informazioni, vedere **lfEscapement**.             |
| CAP \_ \_ DELL'interfaccia utente ROT90  | Supporta i valori di escape del testo 0, 900, 1800 o 2700. Per altre informazioni, vedere **lfEscapement**. |
| CAP \_ \_ ROTANY dell'interfaccia utente | Supporta qualsiasi valore di escape del testo. Per altre informazioni, vedere **lfEscapement**.                       |



 

Se *wParam* è IGP \_ SETCOMPSTR, restituisce uno o più dei valori seguenti.



| Requisito | Valore |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCS \_ CAP \_ COMPSTR            | È possibile creare la stringa di composizione chiamando la [**funzione ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con il valore \_ SCS SETSTR.                                                      |
| SCS \_ CAP \_ MAKEREAD           | Può creare la stringa di lettura dalla stringa di composizione corrispondente quando si usa la [**funzione ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con SCS \_ SETSTR e senza impostare *lpRead*. |
| SCS \_ CAP \_ SETRECONVERTSTRING | Questo IME può supportare la riconversione. Usare [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) per eseguire la riconversione.                                                                             |



 

Se *wParam* è IGP \_ SELECT, restituisce uno o più dei valori seguenti.



| Requisito | Valore |
|-----------------------|------------------------------------------------------|
| SELEZIONARE \_ CAP \_ CONVMODE | Eredita la modalità di conversione quando viene selezionato un nuovo IME. |
| SELEZIONARE \_ CAP \_ SENTENCE | Eredita la modalità frase quando viene selezionato un nuovo IME.   |



 

Se *wParam* è IGP \_ GETIMEVERSION, restituisce uno o più dei valori seguenti.



| Requisito | Valore |
|--------------|---------------------------------------------|
| IMEVER \_ 0310 | L'IME è stato creato per Windows 3.1.        |
| IMEVER \_ 0400 | L'IME è stato creato per Windows 95 o versione successiva |



 

Questo messaggio è simile a [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), ad eccezione del fatto che usa le impostazioni locali di input correnti. L'applicazione deve chiamare [**EM \_ ISIME**](em-isime.md) prima di chiamare questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

