---
title: Associazione asincrona e sincrona
description: Associazione asincrona e sincrona
ms.assetid: 9852df19-5ae4-4425-9ce0-cac160d68456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b022df239221f0a019b972067248225210e585
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730519"
---
# <a name="asynchronous-and-synchronous-binding"></a>Associazione asincrona e sincrona

Il client può verificare se il moniker è asincrono chiamando la funzione [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) . Se il client restituisce il \_ flag asincrono BINDF, anziché restituire un puntatore a un oggetto o un puntatore di archiviazione da chiamate successive a [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) o [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject), il MONIKER restituisce l' \_ \_ oggetto asincrono MK S al posto del puntatore all'oggetto e **null** al posto del puntatore di archiviazione. In risposta, il client deve attendere di ricevere l'oggetto o l'archiviazione richiesta durante l'implementazione di [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) e [**IBindStatusCallback:: OnObjectAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85)).

L'oggetto callback riceve anche la notifica dello stato di avanzamento tramite [**IBindStatusCallback:: OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), la notifica di disponibilità dei dati tramite [**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))e diverse altre notifiche dal moniker sullo stato dell'operazione di associazione.

Se il client non restituisce il \_ flag asincrono BINDF dalla chiamata del moniker a [**IBindStatusCallback:: GetBindInfo.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)), l'operazione di associazione verrà eseguita in modo sincrono e l'oggetto o l'archiviazione desiderata verrà restituito dalle chiamate successive a [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) o [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage). Analogamente, se il client desidera un'operazione sincrona e non desidera ricevere notifiche di stato o callback, può richiedere un moniker asincrono per comportarsi in modo sincrono senza implementare [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)). In questi casi, il moniker asincrono si comporterà come un moniker sincrono standard.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker asincroni](asynchronous-monikers.md)
</dt> </dl>

 

 