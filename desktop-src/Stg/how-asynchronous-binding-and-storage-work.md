---
title: Funzionamento dell'associazione asincrona e dell'archiviazione
description: L'archiviazione asincrona migliora la specifica di archiviazione strutturata COM per supportare il download di oggetti di archiviazione su reti a latenza elevata e a collegamento lento, ad esempio Internet.
ms.assetid: 891152c3-5abd-45e4-a7bb-0aac23262b03
keywords:
- Funzionamento dell'associazione asincrona e dell'archiviazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626e8c7a55b667e158de42b3c88a17315b5e41ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399195"
---
# <a name="how-asynchronous-binding-and-storage-work"></a>Funzionamento dell'associazione asincrona e dell'archiviazione

L'archiviazione asincrona migliora la specifica di archiviazione strutturata COM per supportare il download di oggetti di archiviazione su reti a latenza elevata e a collegamento lento, ad esempio Internet. L'archiviazione asincrona funziona insieme ai moniker asincroni per fornire un comportamento di associazione asincrono completo.

## <a name="document-object-embedded-in-a-web-page"></a>Oggetto Document incorporato in una pagina Web

Quando un utente fa clic su un collegamento che rappresenta un documento incorporato in una pagina Web, si verificano gli eventi seguenti:

1.  Il browser chiama la funzione [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) , passando l'URL del collegamento.
2.  [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) analizza l'URL, crea un moniker asincrono corrispondente e restituisce un puntatore all'interfaccia [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) del moniker.
3.  Il browser chiama [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) per determinare se il moniker è asincrono, crea un contesto di associazione, registra l'interfaccia [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) con il contesto di associazione, solo se il moniker è asincrono e chiama [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject), passando il contesto di associazione.
4.  Il moniker viene associato all'oggetto ed esegue una query per l'interfaccia [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , che indica se l'oggetto supporta l'associazione asincrona e l'archiviazione. Se l'oggetto restituisce un puntatore a **IPersistMoniker**:

    1.  Il moniker URL chiama [**IPersistMoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)), passando il proprio puntatore [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) all'oggetto.
    2.  L'oggetto modifica il contesto di associazione, sceglie se desidera un'archiviazione bloccante o non bloccata, registra il proprio [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) e chiama [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) sul puntatore ricevuto tramite [**IPersistMoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)).
    3.  Il moniker crea un'archiviazione asincrona, mantiene un riferimento all'interfaccia [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) dell'oggetto wrapper, registra l'interfaccia [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) nell'archivio radice e chiama [**IPersistStorage:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), passando il puntatore [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) dell'archivio asincrono. Quando i dati arrivano (in un thread in background), il moniker chiama **IFillLockBytes** per riempire il [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) nel file temporaneo.
    4.  L'oggetto legge i dati dalla risorsa di archiviazione e restituisce da [**IPersistMoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)) quando riceve dati sufficienti per considerarsi inizializzato. Se l'oggetto tenta di leggere i dati che non sono ancora stati scaricati, il Downloader riceve una notifica su [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). All'interno del metodo [**IProgressNotify:: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) , il thread di download si blocca in un ciclo di messaggi modale o fa in modo che l'archivio asincrono restituisca E \_ in sospeso, a seconda che l'oggetto abbia richiesto un'archiviazione bloccante o non bloccata.

5.  Se l'oggetto non implementa [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)), il moniker esegue una query per [**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), che indica che lo stato persistente dell'oggetto viene archiviato in un oggetto di archiviazione. Se l'oggetto restituisce un puntatore a **IPersistStorage**:

    1.  Il moniker chiama [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) su se stesso, richiedendo un [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) di blocco (poiché l'oggetto non è in grado di riconoscere asincrono), crea un'archiviazione asincrona, mantiene un riferimento all'interfaccia [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) dell'oggetto wrapper, registra l'interfaccia [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) nell'archivio radice e chiama [**IPersistStorage:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), passando il puntatore **IStorage** dell'archivio asincrono. Quando i dati arrivano (in un thread in background), il moniker chiama [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) per riempire il [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) del file temporaneo.
    2.  L'oggetto legge i dati dall'archivio e restituisce da [**IPersistStorage:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) quando riceve dati sufficienti per considerarsi inizializzato. Se l'oggetto tenta di leggere i dati che non sono ancora stati scaricati, riceve una notifica in [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). All'interno del metodo [**IProgressNotify:: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) il thread di download viene sempre bloccato in un ciclo di messaggi modale.

6.  Indipendentemente dal fatto che il download sia sincrono o asincrono, il moniker restituisce da [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject)e il browser riceve l'oggetto inizializzato richiesto.
7.  Il browser esegue una query per [**IOleObject**](/windows/win32/api/oleidl/nn-oleidl-ioleobject) e ospita l'oggetto come oggetto documento. A questo punto l'oggetto potrebbe non essere inizializzato completamente, ma sufficiente per visualizzare un elemento utile, nel qual caso il download continua in background.

 

 