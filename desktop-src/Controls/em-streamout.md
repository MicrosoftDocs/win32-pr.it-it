---
title: EM_STREAMOUT messaggio (Richedit.h)
description: Fa in modo che un controllo Rich Edit passi il contenuto a un'applicazione \ 8211;funzione di callback EditStreamCallback definita. La funzione di callback può quindi scrivere il flusso di dati in un file o in qualsiasi altro percorso scelto.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- EM_STREAMOUT dei messaggi Windows controllo
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
ms.openlocfilehash: 63236083c1964d29cb915e4bfc51303b30b730e01f76f2b186cc200d1dcfce6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019469"
---
# <a name="em_streamout-message"></a>Messaggio \_ EM STREAMOUT

Fa in modo che un controllo Rich Edit passi il contenuto a una funzione di callback [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definita dall'applicazione. La funzione di callback può quindi scrivere il flusso di dati in un file o in qualsiasi altro percorso scelto.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il formato dei dati e le opzioni di sostituzione.

Questo valore deve essere uno dei valori seguenti.



| Valore                                                                                                                                                      | Significato                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**SF \_ RTF**</dt> </dl>                   | Rtf.<br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <dt>**SF \_ RTFNOOBJS**</dt> </dl> | RTF con spazi al posto degli oggetti COM.<br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**SF \_ TEXT**</dt> </dl>                | Testo con spazi al posto degli oggetti COM.<br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <dt>**SF \_ TEXTIZED**</dt> </dl>    | Testo con una rappresentazione testuale di oggetti COM.<br/> |



 

**\_ L'opzione SF RTFNOOBJS** è utile se un'applicazione archivia oggetti COM, in quanto la rappresentazione RTF degli oggetti COM non è molto compatta. La parola di \\ controllo, objattph, seguita da uno spazio indica la posizione dell'oggetto.

È anche possibile specificare i flag seguenti.



| Valore                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF \_ PLAINRTF**</dt> </dl>       | Se specificato, il controllo Rich Edit consente di trasmettere solo le parole chiave comuni a tutti i linguaggi, ignorando le parole chiave specifiche del linguaggio. Se non viene specificato, il controllo Rich Edit esere il flusso di tutte le parole chiave. È possibile combinare questo flag con il flag **SF \_ RTF** o **SF \_ RTFNOOBJS.**<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**SELEZIONE \_ SFF**</dt> </dl>    | Se specificato, il controllo Rich Edit esere il flusso solo del contenuto della selezione corrente. Se non viene specificato, il controllo esere il flusso dell'intero contenuto. È possibile combinare questo flag con qualsiasi valore del formato dati.<br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF \_ UNICODE**</dt> </dl>             | **Microsoft Rich Edit 2.0 e versioni successive:** Indica il testo Unicode. È possibile combinare questo flag con il flag **SF \_ TEXT.**<br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <dt>**SF \_ USECODEPAGE**</dt> </dl> | **Rich Edit 3.0 e versioni successive:** Genera testo e RTF UTF-8 usando altre code pages. La tabella codici viene impostata nella parola alta *di wParam*. Ad esempio, per UTF-8 RTF, impostare *wParam* su (CP \_ UTF8 << 16) \| SF \_ USECODEPAGE \| SF \_ RTF.<br/>                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream) Nell'input, il **membro pfnCallback** di questa struttura deve puntare a una funzione [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definita dall'applicazione. Nell'output, **il membro dwError** può contenere un codice di errore diverso da zero se si è verificato un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il numero di caratteri scritti nel flusso di dati.

## <a name="remarks"></a>Commenti

Quando si invia un **messaggio EM \_ STREAMOUT,** il controllo Rich Edit effettua chiamate ripetute alla funzione [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) specificata dal membro **pfnCallback** della [**struttura EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream) Ogni volta che chiama la funzione di callback, il controllo passa un buffer contenente una parte del contenuto del controllo. Questo processo continua fino a quando il controllo non ha passato tutto il contenuto alla funzione di callback o fino a quando non si verifica un errore.

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

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**EM \_ STREAMIN**](em-streamin.md)
</dt> </dl>

 

 





