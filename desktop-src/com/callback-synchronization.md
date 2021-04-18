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
# <a name="callback-synchronization"></a><span data-ttu-id="f7946-103">Sincronizzazione callback</span><span class="sxs-lookup"><span data-stu-id="f7946-103">Callback Synchronization</span></span>

<span data-ttu-id="f7946-104">L' [API WinInet](/windows/desktop/WinInet/portal) asincrona (usata per i protocolli più comuni) lascia la sincronizzazione del meccanismo di callback e dell'applicazione chiamante come esercizio per il client.</span><span class="sxs-lookup"><span data-stu-id="f7946-104">The asynchronous [WinInet API](/windows/desktop/WinInet/portal) (used for the most common protocols) leaves the synchronization of the callback mechanism and the calling application as an exercise for the client.</span></span> <span data-ttu-id="f7946-105">Questo comportamento è intenzionale perché consente il massimo grado di flessibilità.</span><span class="sxs-lookup"><span data-stu-id="f7946-105">This is intentional because it allows the greatest degree of flexibility.</span></span> <span data-ttu-id="f7946-106">I protocolli predefiniti e l'implementazione del moniker URL eseguono questa sincronizzazione e garantiscono che le applicazioni a thread singolo e con threading Apartment non debbano mai gestire conflitti di tipo Free-thread.</span><span class="sxs-lookup"><span data-stu-id="f7946-106">The default protocols and the URL moniker implementation perform this synchronization and guarantee that single-threaded and apartment-threaded applications never have to deal with free-thread-style contention.</span></span> <span data-ttu-id="f7946-107">Ovvero le interfacce [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) e [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) del client vengono chiamate solo sui rispettivi thread appropriati.</span><span class="sxs-lookup"><span data-stu-id="f7946-107">That is, the client's [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) and [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) interfaces are called only on their proper threads.</span></span> <span data-ttu-id="f7946-108">Questa funzionalità è trasparente per l'utente dell'URL mMoniker, a condizione che ogni thread che chiama [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) e [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) disponga di una coda di messaggi.</span><span class="sxs-lookup"><span data-stu-id="f7946-108">This feature is transparent to the user of the URL mMoniker as long each thread that calls [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) and [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) has a message queue.</span></span>

<span data-ttu-id="f7946-109">La specifica del moniker asincrono richiede un controllo più preciso sulla definizione delle priorità e la gestione dei download rispetto a quella consentita da WinSock o WinInet.</span><span class="sxs-lookup"><span data-stu-id="f7946-109">The asynchronous moniker specification requires more precise control over the prioritization and management of downloads than is allowed for by either WinSock or WinInet.</span></span> <span data-ttu-id="f7946-110">Di conseguenza, un moniker URL gestisce tutti i download per un thread del chiamante specifico, usando (come parte della sincronizzazione) uno schema di priorità basato sulla specifica [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f7946-110">Accordingly, a URL moniker manages all the downloads for any given caller's thread, using (as part of its synchronization) a priority scheme based on the [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) specification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7946-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7946-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7946-112">Moniker URL</span><span class="sxs-lookup"><span data-stu-id="f7946-112">URL Monikers</span></span>](url-monikers.md)
</dt> </dl>

 

 