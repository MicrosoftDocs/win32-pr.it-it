---
title: EM_STREAMIN messaggio (Richedit.h)
description: Sostituisce il contenuto di un controllo Rich Edit con un flusso di dati fornito da un'applicazione definita \ 8211; Funzione di callback EditStreamCallback.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- EM_STREAMIN controlli Windows messaggio
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
ms.openlocfilehash: 597d6483ef02f0c9f6f4e4459cd6780b91e04c39160c8057e88fc537fde3b173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576341"
---
# <a name="em_streamin-message"></a>Messaggio \_ STREAMIN EM

Sostituisce il contenuto di un controllo Rich Edit con un flusso di dati fornito da una funzione di callback [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definita dall'applicazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il formato dei dati e le opzioni di sostituzione. Questo valore deve essere uno dei valori seguenti.



| Valore                                                                                                                                       | Significato         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**SF \_ RTF**</dt> </dl>    | RTF<br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**TESTO \_ SF**</dt> </dl> | Testo<br/> |



 

È anche possibile specificare i flag seguenti.



| Valore                                                                                                                                                         | Significato                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF \_ PLAINRTF**</dt> </dl>    | Se specificato, vengono trasmesse solo le parole chiave comuni a tutti i linguaggi. Le parole chiave RTF specifiche della lingua nel flusso vengono ignorate. Se non specificato, tutte le parole chiave vengono trasmesse in streaming. È possibile combinare questo flag con il flag **\_ SF RTF.**<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**SELEZIONE \_ SFF**</dt> </dl> | Se specificato, il flusso di dati sostituisce il contenuto della selezione corrente. Se non specificato, il flusso di dati sostituisce l'intero contenuto del controllo. È possibile combinare questo flag con i **flag SF \_ TEXT** **o SF \_ RTF.**<br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF \_ UNICODE**</dt> </dl>          | **Microsoft Rich Edit 2.0 e versioni successive:** Indica testo Unicode. È possibile combinare questo flag con il flag **SF \_ TEXT.** <br/>                                                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream) Nell'input, il **membro pfnCallback** di questa struttura deve puntare a una funzione [*EditStreamCallback definita dall'applicazione.*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) Nell'output il **membro dwError** può contenere un codice di errore diverso da zero se si è verificato un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il numero di caratteri letti.

## <a name="remarks"></a>Commenti

Quando si invia un **messaggio \_ STREAMIN EM,** il controllo Rich Edit effettua chiamate ripetute alla funzione [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) specificata dal membro **pfnCallback** della [**struttura EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream) Ogni volta che viene chiamata, la funzione di callback riempie un buffer con i dati da leggere nel controllo. Questa operazione continua fino a quando la funzione di callback non indica che l'operazione di flusso è stata completata o si verifica un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**EM \_ STREAMOUT**](em-streamout.md)
</dt> </dl>

 

 





