---
title: Messaggio di EM_STREAMOUT (RichEdit. h)
description: Fa in modo che un controllo Rich Edit passi il contenuto a un'applicazione \ 8211; definita funzione di callback EditStreamCallback. La funzione di callback può quindi scrivere il flusso di dati in un file o in qualsiasi altra posizione scelta.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- Controlli di Windows Message EM_STREAMOUT
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964261"
---
# <a name="em_streamout-message"></a>\_Messaggio di streaming em

Causa il passaggio del contenuto di un controllo Rich Edit a una funzione di callback [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definita dall'applicazione. La funzione di callback può quindi scrivere il flusso di dati in un file o in qualsiasi altra posizione scelta.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il formato dei dati e le opzioni di sostituzione.

Questo valore deve essere uno dei valori seguenti.



| Valore                                                                                                                                                      | Significato                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**RTF per SF \_**</dt> </dl>                   | RTF.<br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <dt>**\_RTFNOOBJS SF**</dt> </dl> | RTF con spazi al posto degli oggetti COM.<br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**\_testo SF**</dt> </dl>                | Testo con spazi al posto degli oggetti COM.<br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <dt>**SF con \_ testo**</dt> </dl>    | Testo con rappresentazione testuale di oggetti COM.<br/> |



 

L'opzione **SF \_ RTFNOOBJS** è utile se un'applicazione archivia oggetti com, perché la rappresentazione RTF degli oggetti com non è molto compatta. Il controllo Word, \\ objattph, seguito da uno spazio indica la posizione dell'oggetto.

Inoltre, è possibile specificare i flag seguenti.



| Valore                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**\_PLAINRTF SFF**</dt> </dl>       | Se specificato, il controllo Rich Edit trasmette solo le parole chiave comuni a tutti i linguaggi, ignorando le parole chiave specifiche della lingua. Se non è specificato, il controllo Rich Edit trasmette tutte le parole chiave. È possibile combinare questo flag con il contrassegno **SF \_ RTF** o **SF \_ RTFNOOBJS** .<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**\_selezione SFF**</dt> </dl>    | Se specificato, il controllo Rich Edit trasmette solo il contenuto della selezione corrente. Se non specificato, il controllo trasmette l'intero contenuto. È possibile combinare questo flag con qualsiasi valore di formato dati.<br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**\_Unicode SF**</dt> </dl>             | **Microsoft Rich Edit 2,0 e versioni successive:** Indica il testo Unicode. È possibile combinare questo flag con il flag di **\_ testo SF** .<br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <dt>**\_USECODEPAGE SF**</dt> </dl> | **Rich Edit 3,0 e versioni successive:** Genera il formato UTF-8 RTF e il testo utilizzando altre tabelle codici. La tabella codici è impostata nella parola alta di *wParam*. Ad esempio, per UTF-8 RTF, impostare *wParam* su (CP \_ UTF8 << 16) \| SF \_ USECODEPAGE \| SF \_ RTF.<br/>                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . In fase di input, il membro **pfnCallback** di questa struttura deve puntare a una funzione [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definita dall'applicazione. Nell'output il membro **dwError** può contenere un codice di errore diverso da zero se si è verificato un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il numero di caratteri scritti nel flusso di dati.

## <a name="remarks"></a>Commenti

Quando si invia un messaggio di **\_ flusso em** , il controllo Rich Edit effettua chiamate ripetute alla funzione [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) specificata dal membro **pfnCallback** della struttura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . Ogni volta che chiama la funzione di callback, il controllo passa un buffer contenente una parte del contenuto del controllo. Questo processo continua fino a quando il controllo non ha passato tutto il contenuto alla funzione di callback o fino a quando non si verifica un errore.

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

[**flusso EMin \_**](em-streamin.md)
</dt> </dl>

 

 





