---
description: Imposta un callback che crea la sessione multimediale PMP durante la risoluzione dell'origine.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: MFPKEY_PMP_Creation_Callback proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655d61865eaecd89fa84664fc5c25f89762180ac9007e21cc7cbc98f7a68b056
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953861"
---
# <a name="mfpkey_pmp_creation_callback-property"></a>Proprietà di callback di \_ creazione PMP MFPKEY \_ \_

Imposta un callback che crea la sessione [multimediale PMP durante](pmp-media-session.md) la risoluzione dell'origine.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**IUnknown\***

VT \_ UNKNOWN

**valvalore**



## <a name="remarks"></a>Commenti

Alcuni contenuti protetti potrebbero richiedere l'uso di questa proprietà. In tal caso, il processo di risoluzione del codice sorgente ha esito negativo con codice di **errore MF \_ E RESOLUTION \_ REQUIRES \_ \_ PMP CREATION \_ \_ CALLBACK**.

Per utilizzare questa proprietà, eseguire le operazioni seguenti.

1.  Chiamare [**PSCreateMemoryPropertyStore per**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) creare un archivio delle proprietà.
2.  Implementare l'interfaccia di callback [**IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
3.  Impostare la proprietà MFPKEY \_ PMP \_ Creation Callback \_ nell'archivio delle proprietà. Il valore è un puntatore [**all'implementazione di IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
4.  Chiamare [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl). Passare un puntatore all'archivio delle proprietà nel *parametro pProps.*

Nel metodo [**IMFAsyncCallback::Invoke dell'interfaccia**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) di callback eseguire le operazioni seguenti.

1.  Chiamare [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) per creare la [sessione multimediale PMP.](pmp-media-session.md)
2.  Chiamare [**IMFGetService::GetService nella**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sessione del supporto PMP a un puntatore [**all'interfaccia IMFPMPHost.**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
3.  Chiamare [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) sull'oggetto risultato passato nel *parametro pAsyncResult* [**di IMFAsyncCallback::Invoke.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Eseguire una query sul [**puntatore IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) restituito per [**l'interfaccia IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
4.  Chiamare [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) con i parametri seguenti:
    -   *dwQueue:* **MFASYNC \_ CALLBACK QUEUE \_ \_ STANDARD**
    -   *pCallback:* [**puntatore IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) ottenuto nel passaggio 3.
    -   *pState:* [**puntatore IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) ottenuto nel passaggio 2.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Sessione multimediale PMP](pmp-media-session.md)
</dt> <dt>

[Percorso del supporto protetto](protected-media-path.md)
</dt> <dt>

[Resolver di origine](source-resolver.md)
</dt> </dl>

 

 
