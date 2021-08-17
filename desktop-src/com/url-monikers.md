---
title: Moniker URL
description: L'architettura del moniker OLE offre un pratico modello di programmazione per l'uso degli URL.
ms.assetid: 8e0e2bad-9275-4b96-a96b-35d9c933ae31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92e952e2d9bdd8ae70108e34845a3e920228b1b68f1db061977dff36e942254
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129488"
---
# <a name="url-monikers"></a>Moniker URL

L'architettura del moniker OLE offre un pratico modello di programmazione per l'uso degli URL. L'architettura del moniker supporta l'analisi dei nomi estendibile e completa tramite la funzione [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) e [**le interfacce IParseDisplayName**](/windows/desktop/api/OleIdl/nn-oleidl-iparsedisplayname) e [**IMoniker,**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) nonché i nomi stampabili tramite il metodo [**IMoniker::GetDisplayName.**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) **L'interfaccia IMoniker** è il modo in cui si usano effettivamente gli URL rilevati e la creazione di componenti che rientrano nell'architettura del moniker è il modo per estendere effettivamente gli spazi dei nomi URL nella pratica.

Una classe moniker fornita dal sistema, il moniker URL, fornisce un framework per la compilazione e l'uso di determinati URL. Poiché gli URL visualizzano spesso le risorse tra reti a latenza elevata, il moniker URL supporta l'associazione asincrona e sincrona. Il moniker URL attualmente non supporta [l'archiviazione asincrona](/windows/desktop/Stg/asynchronous-storage).

Il diagramma seguente illustra i componenti coinvolti nell'uso dei moniker URL. Tutti questi componenti dovrebbero essere familiari. Vedere [Moniker asincroni.](asynchronous-monikers.md)

![Diagramma che mostra i componenti coinvolti nell'uso dei moniker U R L.](images/bb10975a-9cb5-418e-872e-1e1add0b58ed.png)

Come tutti i client moniker, un utente di moniker URL in genere crea e contiene un riferimento al moniker e al contesto di associazione da usare durante l'associazione ([**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) o [**IMoniker::BindToObject).**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) Per supportare l'associazione asincrona, il client può implementare un oggetto bind-status-callback, che implementa [**l'interfaccia IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) e registrarlo con il contesto di associazione usando la funzione [**RegisterBindStatusCallback.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) Questo oggetto riceverà l'interfaccia [**IBinding del**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) trasporto durante le chiamate a [**IBindStatusCallback::OnStartBinding.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85))

Il moniker URL identifica il protocollo usato analizzando il prefisso DELL'URL e quindi recupera [**l'interfaccia IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) dal livello di trasporto. Il client usa **IBinding per** supportare la sospensione, l'annullamento e la definizione delle priorità dell'operazione di associazione. L'oggetto callback riceve anche la notifica dello stato di avanzamento tramite [**IBindStatusCallback::OnProgress,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85))la notifica della disponibilità dei dati tramite [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))e varie altre notifiche a livello di trasporto sullo stato dell'associazione. Il moniker URL o livelli di trasporto specifici possono anche richiedere informazioni estese al client tramite **IBindStatusCallback::QueryInterface,** consentendo al client di fornire informazioni specifiche del protocollo che influiranno sull'operazione di associazione.

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

 

 