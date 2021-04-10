---
description: Imposta un callback che crea la sessione multimediale PMP durante la risoluzione dell'origine.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: Proprietà MFPKEY_PMP_Creation_Callback (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226996"
---
# <a name="mfpkey_pmp_creation_callback-property"></a>Proprietà di callback per la \_ creazione di MFPKEY PMP \_ \_

Imposta un callback che crea la [sessione multimediale PMP](pmp-media-session.md) durante la risoluzione dell'origine.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**IUnknown \** _

VT \_ sconosciuto

_ *punkVal**



## <a name="remarks"></a>Commenti

Alcuni contenuti protetti potrebbero richiedere l'uso di questa proprietà. In tal caso, il processo di risoluzione dell'origine ha esito negativo con il codice di errore **MF \_ E la \_ risoluzione \_ richiede il \_ \_ \_ callback di creazione PMP**.

Per usare questa proprietà, eseguire le operazioni seguenti.

1.  Chiamare [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) per creare un archivio delle proprietà.
2.  Implementare l'interfaccia di callback [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
3.  Impostare la \_ \_ \_ proprietà di callback per la creazione di MFPKEY PMP nell'archivio delle proprietà. Il valore è un puntatore all'implementazione di [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
4.  Chiamare [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl). Passare un puntatore all'archivio delle proprietà nel parametro *pProps* .

Nel metodo [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) dell'interfaccia di callback eseguire le operazioni seguenti.

1.  Chiamare [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) per creare la [sessione multimediale PMP](pmp-media-session.md).
2.  Chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sulla sessione multimediale PMP in un puntatore all'interfaccia [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) .
3.  Chiamare [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) sull'oggetto risultato passato nel parametro *pAsyncResult* di [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Eseguire una query sul puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) restituito per l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
4.  Chiamare [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) con i parametri seguenti:
    -   *dwQueue*: **MFASYNC \_ coda di callback \_ \_ standard**
    -   *pCallback*: puntatore [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) ottenuto nel passaggio 3.
    -   *pState*: puntatore [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) ottenuto nel passaggio 2.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sessione multimediale PMP](pmp-media-session.md)
</dt> <dt>

[Percorso supporto protetto](protected-media-path.md)
</dt> <dt>

[Resolver di origine](source-resolver.md)
</dt> </dl>

 

 
