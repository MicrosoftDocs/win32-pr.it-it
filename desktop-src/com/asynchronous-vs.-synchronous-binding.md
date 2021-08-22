---
title: Associazione asincrona e sincrona
description: Associazione asincrona e sincrona
ms.assetid: 9852df19-5ae4-4425-9ce0-cac160d68456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb498d083260db087e9f32cd3f24b67f03f9a788c0add2592dde36fe7a7905e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048859"
---
# <a name="asynchronous-and-synchronous-binding"></a>Associazione asincrona e sincrona

Il client può verificare se il moniker è asincrono chiamando la [**funzione IsAsyncMoniker.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) Se il client restituisce il flag BINDF ASYNCHRONOUS, anziché restituire un puntatore a oggetto o un puntatore di archiviazione dalle chiamate successive \_ a [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) o [**IMoniker::BindToObject,**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)il moniker restituisce MK S ASYNCHRONOUS al posto del puntatore a oggetto e NULL al posto del puntatore \_ di \_ archiviazione.  In risposta, il client deve attendere di ricevere l'oggetto o lo spazio di archiviazione richiesto durante l'implementazione di [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) e [**IBindStatusCallBack::OnObjectAvailable.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85))

L'oggetto callback riceve anche la notifica dello stato di avanzamento tramite [**IBindStatusCallback::OnProgress,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85))la notifica di disponibilità dei dati tramite [**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))e varie altre notifiche dal moniker sullo stato dell'operazione di associazione.

Se il client non restituisce il flag BINDF ASYNCHRONOUS dalla chiamata del \_ moniker a [**IBindStatusCallback::GetBindInfo,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))l'operazione di associazione procederà in modo sincrono e l'oggetto o lo spazio di archiviazione desiderato verrà restituito dalle chiamate successive a [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) o [**BindToStorage.**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) Analogamente, se il client desidera un'operazione sincrona e non vuole ricevere notifiche o callback di stato, può richiedere a un moniker asincrono di comportarsi in modo sincrono non implementando [**IBindStatusCallback.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) In questi casi, il moniker asincrono si comporterà come un moniker sincrono standard.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker asincroni](asynchronous-monikers.md)
</dt> </dl>

 

 