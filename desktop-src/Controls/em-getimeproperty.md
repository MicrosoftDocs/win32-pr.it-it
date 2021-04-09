---
title: Messaggio di EM_GETIMEPROPERTY (RichEdit. h)
description: Recupera la proprietà e le funzionalità dell'IME (Input Method Editor) associate alle impostazioni locali di input correnti.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- Controlli di Windows Message EM_GETIMEPROPERTY
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
ms.openlocfilehash: 94c081aa99c99f4cd0995c0f9d2f5256e2958dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120734"
---
# <a name="em_getimeproperty-message"></a>\_Messaggio GETIMEPROPERTY em

Recupera la proprietà e le funzionalità dell'IME (Input Method Editor) associate alle impostazioni locali di input correnti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il tipo di informazioni di proprietà da recuperare. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                     | Significato                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <dt>**\_Proprietà IGP**</dt> </dl>                | Informazioni sulle proprietà.<br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <dt>**\_conversione IGP**</dt> </dl>          | Funzionalità di conversione. <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <dt>**\_frase IGP**</dt> </dl>                | Funzionalità della modalità frase. <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <dt>**\_interfaccia utente IGP**</dt> </dl>                                  | Funzionalità dell'interfaccia utente. <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <dt>**\_SETCOMPSTR IGP**</dt> </dl>          | Funzionalità della stringa di composizione. <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <dt>**\_Select IGP**</dt> </dl>                      | Funzionalità di ereditarietà della selezione. <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <dt>**\_GETIMEVERSION IGP**</dt> </dl> | Recupera il numero di versione del sistema per il quale è stato creato l'IME specificato. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la proprietà o il valore della funzionalità, a seconda del valore del parametro *lParam* . Per ulteriori informazioni, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Se *wParam* è \_ la proprietà IGP, restituisce uno o più dei valori seguenti.



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_propt IME \_ al punto di \_ inserimento                | Se impostato, la finestra di conversione si trova nella posizione del punto di inserimento. Se è deselezionata, la finestra si trova vicino al punto di inserimento.                                                                                                                                                                  |
| \_ \_ interfaccia utente speciale di IME Prop \_              | Se impostato, l'IME ha un'interfaccia utente non standard. Impossibile creare l'applicazione nella finestra IME.                                                                                                                                                                  |
| \_ \_ \_ Inizio della pagina di inizio \_ della prop IME da \_ 1 | Se impostato, le stringhe nell'elenco candidato sono numerate a partire da 1. Se chiaro, le stringhe iniziano da zero.                                                                                                                                                                |
| \_Unicode Prop \_ IME                  | Se impostato, l'IME viene visualizzato come UnicodeIME. Il sistema e l'IME comunicheranno tramite l'interfaccia UnicodeIME. Se chiaro, l'IME utilizzerà l'interfaccia ANSI per comunicare con il sistema.                                                                    |
| l' \_ operazione di propulsione IME è stata \_ completata \_ in \_ Unselect   | Se impostato, la finestra di conversione si trova nella posizione del punto di inserimento. Se è deselezionata, la finestra si trova vicino al punto di inserimento.                                                                                                                                                                  |
| \_VKEY della prop IME \_ Accept \_ Wide \_       | Se impostato, l'IME elabora il formato Unicode inserito dalla funzione [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) usando il \_ pacchetto VK. Se chiaro, l'IME potrebbe non elaborare il formato Unicode inserito e il formato Unicode inserito potrebbe essere inviato direttamente all'applicazione. |



 

Se *wParam* è \_ un'interfaccia utente IGP, restituisce uno o più dei valori seguenti.



| Requisito | Valore |
|-----------------|-------------------------------------------------------------------------------------------------------|
| Estremità interfaccia utente \_ \_ 2700   | Supporta i valori di escape del testo 0 o 2700. Per ulteriori informazioni, vedere **lfEscapement**.             |
| Estremità interfaccia utente \_ \_ ROT90  | Supporta i valori di escape del testo 0, 900, 1800 o 2700. Per ulteriori informazioni, vedere **lfEscapement**. |
| estremità interfaccia utente \_ \_ ROTANY | Supporta qualsiasi valore di escape del testo. Per ulteriori informazioni, vedere **lfEscapement**.                       |



 

Se *wParam* è IGP \_ SETCOMPSTR, restituisce uno o più dei valori seguenti.



| Requisito | Valore |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_COMPSTR Cap \_ SCS            | È possibile creare la stringa di composizione chiamando la funzione [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con il \_ valore SCS SETSTR.                                                      |
| \_MAKEREAD Cap \_ SCS           | Consente di creare la stringa di lettura dalla stringa di composizione corrispondente quando si usa la funzione [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con SCS \_ SETSTR e senza impostare *lpRead*. |
| \_SETRECONVERTSTRING Cap \_ SCS | Questo IME può supportare la riconversione. Usare [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) per eseguire la riconversione.                                                                             |



 

Se *wParam* è IGP \_ Select, restituisce uno o più dei valori seguenti.



| Requisito | Valore |
|-----------------------|------------------------------------------------------|
| SELECT \_ Cap \_ CONVMODE | Eredita la modalità di conversione quando viene selezionato un nuovo IME. |
| Seleziona \_ \_ frase Cap | Eredita la modalità frase quando viene selezionato un nuovo IME.   |



 

Se *wParam* è IGP \_ GETIMEVERSION, restituisce uno o più dei valori seguenti.



| Requisito | Valore |
|--------------|---------------------------------------------|
| Immai \_ 0310 | L'IME è stato creato per Windows 3,1.        |
| Immai \_ 0400 | L'IME è stato creato per Windows 95 o versione successiva |



 

Questo messaggio è simile a [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), con la differenza che usa le impostazioni locali di input correnti. Prima di chiamare questa funzione, l'applicazione deve chiamare [**em \_ ISIME**](em-isime.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_ISIME em**](em-isime.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

