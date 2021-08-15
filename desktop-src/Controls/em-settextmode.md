---
title: EM_SETTEXTMODE messaggio (Richedit.h)
description: Imposta la modalità testo o il livello di annullamento di un controllo Rich Edit. Il messaggio ha esito negativo se il controllo contiene testo.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- EM_SETTEXTMODE dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ea489dcdb60908cac8600188d40b9aae4b7e3e531c713094bb180e84ee24bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672370"
---
# <a name="em_settextmode-message"></a>Messaggio \_ EM SETTEXTMODE

Imposta la modalità testo o il livello di annullamento di un controllo Rich Edit. Il messaggio ha esito negativo se il controllo contiene testo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o più valori del tipo [**di enumerazione TEXTMODE.**](/windows/win32/api/richedit/ne-richedit-textmode) I valori specificano le nuove impostazioni per i parametri della modalità testo e del livello di annullamento del controllo.

Specificare uno dei valori seguenti per impostare il parametro della modalità testo. Se non si specifica un valore per la modalità testo, la modalità testo rimane all'impostazione corrente. 

| Valore                                          | Significato                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TESTO NON CRITTOGRAFATO TM \_**](/windows/win32/api/richedit/ne-richedit-textmode) | Indica la modalità testo normale, in cui il controllo è simile a un controllo di modifica standard. Per altre informazioni sulla modalità testo normale, vedere la sezione Osservazioni seguente. |
| [**TM \_ RICHTEXT**](/windows/win32/api/richedit/ne-richedit-textmode)   | Indica la modalità rtf, in cui il controllo dispone di funzionalità rich edit standard. La modalità RTF è l'impostazione predefinita.                                           |



 

Specificare uno dei valori seguenti per impostare il parametro del livello di annullamento. Se non si specifica un valore del livello di annullamento, il livello di annullamento rimane all'impostazione corrente. 

| Valore                                                      | Significato                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLELEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode) | Il controllo consente all'utente di annullare solo l'ultima azione che può essere annullata.                                                                                                       |
| [**TM \_ MULTILEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode)   | Il controllo supporta più operazioni di annullamento. Si tratta dell'impostazione predefinita. Usare il [**messaggio EM \_ SETUNDOLIMIT**](em-setundolimit.md) per impostare il numero massimo di azioni di annullamento. |



 

Specificare uno dei valori seguenti per impostare il parametro della tabella codici. Se non si specifica un valore di tabella codici, la tabella codici rimane in corrispondenza dell'impostazione corrente. 

| Valore                                                    | Significato                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLECODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode) | Il controllo consente solo la tastiera inglese e una tastiera corrispondente al set di caratteri predefinito. Ad esempio, è possibile avere greco e inglese. Si noti che in questo modo si impedisce l'immissione di testo Unicode nel controllo. Ad esempio, usare questo valore se un controllo Rich Edit deve essere limitato al testo ANSI. |
| [**TM \_ MULTICODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode)   | Il controllo consente più code pages e testo Unicode nel controllo . Si tratta dell'impostazione predefinita.                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è zero.

Se il messaggio ha esito negativo, il valore restituito è un valore diverso da zero.

## <a name="remarks"></a>Commenti

In modalità RTF, un controllo Rich Edit dispone di funzionalità rich edit standard. Tuttavia, in modalità testo normale, il controllo è simile a un controllo di modifica standard:

-   Il testo in un controllo di testo normale può avere un solo formato, ad esempio Grassetto, Arial 10pt.
-   L'utente non può incollare formati rtf, ad esempio RTF (Rich Text Format) o oggetti incorporati in un controllo di testo normale.
-   I controlli in modalità TESTO RTF hanno sempre un marcatore di fine documento o un ritorno a capo predefinito per formattare i paragrafi. I controlli di testo normale, d'altra parte, non necessitano dell'indicatore di fine documento predefinito, quindi viene omesso.

Il controllo non deve contenere testo quando riceve il **messaggio EM \_ SETTEXTMODE.** Per assicurarsi che non sia presente testo, inviare un [**messaggio \_ WM SETTEXT**](/windows/desktop/winmsg/wm-settext) con una stringa vuota ("").

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETTEXTMODE**](em-gettextmode.md)
</dt> <dt>

[**EM \_ SETUNDOLIMIT**](em-setundolimit.md)
</dt> <dt>

[**Textmode**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

