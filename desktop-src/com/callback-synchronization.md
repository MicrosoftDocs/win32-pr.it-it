---
title: Sincronizzazione callback
description: Sincronizzazione callback
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c274c35a6df176f65c505f2a3fecc9a53a20e5d9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300521"
---
# <a name="callback-synchronization"></a>Sincronizzazione callback

L' [API WinInet](/windows/desktop/WinInet/portal) asincrona (usata per i protocolli più comuni) lascia la sincronizzazione del meccanismo di callback e dell'applicazione chiamante come esercizio per il client. Questo comportamento è intenzionale perché consente il massimo grado di flessibilità. I protocolli predefiniti e l'implementazione del moniker URL eseguono questa sincronizzazione e garantiscono che le applicazioni a thread singolo e con threading Apartment non debbano mai gestire conflitti di tipo Free-thread. Ovvero le interfacce [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) e [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) del client vengono chiamate solo sui rispettivi thread appropriati. Questa funzionalità è trasparente per l'utente dell'URL mMoniker, a condizione che ogni thread che chiama [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) e [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) disponga di una coda di messaggi.

La specifica del moniker asincrono richiede un controllo più preciso sulla definizione delle priorità e la gestione dei download rispetto a quella consentita da WinSock o WinInet. Di conseguenza, un moniker URL gestisce tutti i download per un thread del chiamante specifico, usando (come parte della sincronizzazione) uno schema di priorità basato sulla specifica [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker URL](url-monikers.md)
</dt> </dl>

 

 