---
title: Messaggio di EM_STREAMIN (RichEdit. h)
description: Sostituisce il contenuto di un controllo Rich Edit con un flusso di dati fornito da un'applicazione definita \ 8211; Funzione di callback EditStreamCallback.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- Controlli di Windows Message EM_STREAMIN
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478275"
---
# <a name="em_streamin-message"></a>\_Messaggio flusso Emin

Sostituisce il contenuto di un controllo Rich Edit con un flusso di dati fornito da una funzione di callback [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definita dall'applicazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il formato dei dati e le opzioni di sostituzione. Questo valore deve essere uno dei valori seguenti.



| Valore                                                                                                                                       | Significato         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**RTF per SF \_**</dt> </dl>    | RTF<br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**\_testo SF**</dt> </dl> | Testo<br/> |



 

Inoltre, è possibile specificare i flag seguenti.



| Valore                                                                                                                                                         | Significato                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**\_PLAINRTF SFF**</dt> </dl>    | Se specificato, solo le parole chiave comuni a tutti i linguaggi vengono trasmesse in. Le parole chiave RTF specifiche del linguaggio nel flusso vengono ignorate. Se non è specificato, tutte le parole chiave vengono trasmesse in. È possibile combinare questo flag con il **flag \_ RTF di SF** .<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**\_selezione SFF**</dt> </dl> | Se specificato, il flusso di dati sostituisce il contenuto della selezione corrente. Se non è specificato, il flusso di dati sostituisce l'intero contenuto del controllo. È possibile combinare questo flag con i flag di **\_ testo SF** o **\_ RTF** .<br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**\_Unicode SF**</dt> </dl>          | **Microsoft Rich Edit 2,0 e versioni successive:** Indica il testo Unicode. È possibile combinare questo flag con il flag di **\_ testo SF** . <br/>                                                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . In fase di input, il membro **pfnCallback** di questa struttura deve puntare a una funzione [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definita dall'applicazione. Nell'output il membro **dwError** può contenere un codice di errore diverso da zero se si è verificato un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il numero di caratteri letti.

## <a name="remarks"></a>Commenti

Quando si invia un **messaggio \_ flusso Emin** , il controllo Rich Edit effettua chiamate ripetute alla funzione [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) specificata dal membro **pfnCallback** della struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . Ogni volta che viene chiamata la funzione di callback, riempie un buffer con i dati da leggere nel controllo. Continua fino a quando la funzione di callback non indica che l'operazione del flusso è stata completata o si è verificato un errore.

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

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**\_flusso em**](em-streamout.md)
</dt> </dl>

 

 





