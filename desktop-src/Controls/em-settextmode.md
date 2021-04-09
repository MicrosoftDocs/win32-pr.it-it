---
title: Messaggio di EM_SETTEXTMODE (RichEdit. h)
description: Imposta la modalità testo o il livello di annullamento di un controllo Rich Edit. Il messaggio ha esito negativo se il controllo contiene testo.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- Controlli di Windows Message EM_SETTEXTMODE
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
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964387"
---
# <a name="em_settextmode-message"></a>\_Messaggio SETTEXTMODE em

Imposta la modalità testo o il livello di annullamento di un controllo Rich Edit. Il messaggio ha esito negativo se il controllo contiene testo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o più valori del tipo di enumerazione [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) . I valori specificano le nuove impostazioni per la modalità testo del controllo e i parametri del livello di annullamento.

Specificare uno dei valori seguenti per impostare il parametro della modalità testo. Se non si specifica un valore in modalità testo, la modalità testo rimane in corrispondenza dell'impostazione corrente. 

| Valore                                          | Significato                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_testo normale TM**](/windows/win32/api/richedit/ne-richedit-textmode) | Indica la modalità testo normale, in cui il controllo è simile a un controllo di modifica standard. Per ulteriori informazioni sulla modalità testo normale, vedere la sezione Osservazioni riportata di seguito. |
| [**TM \_ RichText**](/windows/win32/api/richedit/ne-richedit-textmode)   | Indica la modalità RTF, in cui il controllo ha una funzionalità di modifica avanzata standard. La modalità RTF è l'impostazione predefinita.                                           |



 

Specificare uno dei valori seguenti per impostare il parametro del livello di annullamento. Se non si specifica un valore del livello di annullamento, il livello di annullamento rimane in corrispondenza dell'impostazione corrente. 

| Valore                                                      | Significato                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLELEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode) | Il controllo consente all'utente di annullare solo l'ultima azione che può essere annullata.                                                                                                       |
| [**TM \_ MULTILEVELUNDO**](/windows/win32/api/richedit/ne-richedit-textmode)   | Il controllo supporta più operazioni di annullamento. Si tratta dell'impostazione predefinita. Usare il [**messaggio \_ SETUNDOLIMIT em**](em-setundolimit.md) per impostare il numero massimo di azioni di annullamento. |



 

Specificare uno dei valori seguenti per impostare il parametro della tabella codici. Se non si specifica un valore della tabella codici, la tabella codici rimane in corrispondenza dell'impostazione corrente. 

| Valore                                                    | Significato                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TM \_ SINGLECODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode) | Il controllo consente solo la tastiera inglese e una tastiera corrispondente al set di caratteri predefinito. Ad esempio, è possibile avere il greco e l'inglese. Si noti che in questo modo si impedisce al testo Unicode di immettere il controllo. Usare, ad esempio, questo valore se un controllo Rich Edit deve essere limitato al testo ANSI. |
| [**TM \_ MULTICODEPAGE**](/windows/win32/api/richedit/ne-richedit-textmode)   | Il controllo consente di accedere a più tabelle codici e testo Unicode. Si tratta dell'impostazione predefinita.                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è zero.

Se il messaggio ha esito negativo, il valore restituito è un valore diverso da zero.

## <a name="remarks"></a>Commenti

In modalità RTF, un controllo Rich Edit ha una funzionalità di modifica avanzata standard. Tuttavia, in modalità testo normale, il controllo è simile a un controllo di modifica standard:

-   Il testo in un controllo testo normale può avere un solo formato, ad esempio grassetto, 10pt Arial.
-   L'utente non può incollare formati RTF, ad esempio Rich Text Format (RTF) o oggetti incorporati in un controllo testo normale.
-   Per formattare i paragrafi, i controlli della modalità RTF hanno sempre un indicatore di fine del documento predefinito o un ritorno a capo. I controlli di testo normale, d'altra parte, non necessitano del marcatore di fine del documento predefinito, pertanto viene omesso.

Il controllo non deve contenere testo quando riceve il messaggio **\_ SETTEXTMODE em** . Per assicurarsi che non esistano testo, inviare un messaggio di [**\_ testo WM**](/windows/desktop/winmsg/wm-settext) con una stringa vuota ("").

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETTEXTMODE em**](em-gettextmode.md)
</dt> <dt>

[**\_SETUNDOLIMIT em**](em-setundolimit.md)
</dt> <dt>

[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[**\_testo WM**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

