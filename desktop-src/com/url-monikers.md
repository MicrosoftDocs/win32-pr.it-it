---
title: Moniker URL
description: L'architettura del moniker OLE fornisce un modello di programmazione pratico per l'utilizzo degli URL.
ms.assetid: 8e0e2bad-9275-4b96-a96b-35d9c933ae31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2a63f63d14dfe51c0b8c5c3727637e12a51356
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104234403"
---
# <a name="url-monikers"></a>Moniker URL

L'architettura del moniker OLE fornisce un modello di programmazione pratico per l'utilizzo degli URL. L'architettura del moniker supporta l'analisi dei nomi estendibile e completa tramite la funzione [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) e le interfacce [**IParseDisplayName**](/windows/desktop/api/OleIdl/nn-oleidl-iparsedisplayname) e [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , nonché i nomi stampabili tramite il metodo [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) . L'interfaccia **IMoniker** è il modo in cui si usano effettivamente gli URL che si verificano e la compilazione di componenti che rientrano nell'architettura del moniker è il modo per estendere effettivamente gli spazi dei nomi URL in pratica.

Una classe di moniker fornita dal sistema, il moniker URL, fornisce un Framework per la compilazione e l'uso di determinati URL. Poiché gli URL visualizzano spesso le risorse tra le reti a latenza elevata, il moniker URL supporta l'associazione asincrona e sincrona. Il moniker URL attualmente non supporta l' [archiviazione asincrona](/windows/desktop/Stg/asynchronous-storage).

Il diagramma seguente illustra i componenti necessari per l'uso dei moniker URL. Tutti questi componenti dovrebbero avere una certa familiarità. (Vedere [moniker asincroni](asynchronous-monikers.md)).

![Diagramma che mostra i componenti necessari per l'uso dei moniker U R L.](images/bb10975a-9cb5-418e-872e-1e1add0b58ed.png)

Come tutti i client moniker, un utente di moniker URL Crea in genere e include un riferimento al moniker, oltre al contesto di associazione da usare durante l'associazione ([**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) o [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)). Per supportare il binding asincrono, il client può implementare un oggetto Bind-status-callback che implementa l'interfaccia [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) e registrarlo nel contesto di associazione usando la funzione [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) . Questo oggetto riceverà l'interfaccia [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) del trasporto durante le chiamate a [**IBindStatusCallback:: OnStart**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)).

Il moniker URL identifica il protocollo usato analizzando il prefisso URL e quindi recupera l'interfaccia [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) dal livello trasporto. Il client utilizza **IBinding** per supportare la sospensione, l'annullamento e la definizione delle priorità dell'operazione di associazione. L'oggetto callback riceve anche la notifica dello stato di avanzamento tramite [**IBindStatusCallback:: OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), la notifica di disponibilità dei dati tramite [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))e varie altre notifiche a livello di trasporto sullo stato dell'associazione. Il moniker URL o i livelli di trasporto specifici possono anche richiedere informazioni estese dal client tramite **IBindStatusCallback:: QueryInterface**, consentendo al client di fornire informazioni specifiche del protocollo che avranno effetto sull'operazione di associazione.

Per altre informazioni, vedere i seguenti argomenti:

-   [Sincronizzazione callback](callback-synchronization.md)
-   [Negoziazione del tipo di supporto](media-type-negotiation.md)
-   [Funzioni moniker URL](url-moniker-api-functions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker asincroni](asynchronous-monikers.md)
</dt> <dt>

[Informazioni sui moniker URL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775149(v=vs.85))
</dt> </dl>

 

 