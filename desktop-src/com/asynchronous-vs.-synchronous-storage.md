---
title: Archiviazione asincrona e sincrona
description: Archiviazione asincrona e sincrona
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517158"
---
# <a name="asynchronous-and-synchronous-storage"></a><span data-ttu-id="fbd6d-103">Archiviazione asincrona e sincrona</span><span class="sxs-lookup"><span data-stu-id="fbd6d-103">Asynchronous and Synchronous Storage</span></span>

<span data-ttu-id="fbd6d-104">I moniker asincroni possono anche restituire un oggetto di [archiviazione asincrono](/windows/desktop/Stg/asynchronous-storage) nella notifica [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fbd6d-104">Asynchronous monikers may also return an [Asynchronous Storage](/windows/desktop/Stg/asynchronous-storage) object in the [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) notification.</span></span> <span data-ttu-id="fbd6d-105">Questo oggetto di archiviazione può consentire l'accesso ad alcuni dati persistenti dell'oggetto mentre l'associazione è ancora in corso.</span><span class="sxs-lookup"><span data-stu-id="fbd6d-105">This storage object may allow access to some of the object's persistent data while the binding is still in progress.</span></span> <span data-ttu-id="fbd6d-106">Un client può scegliere tra due modalità per l'archiviazione: blocco e non blocco.</span><span class="sxs-lookup"><span data-stu-id="fbd6d-106">A client can choose between two modes for the storage: blocking and nonblocking.</span></span>

<span data-ttu-id="fbd6d-107">In modalità di blocco, che è compatibile con le implementazioni correnti degli oggetti di archiviazione, se i dati non sono disponibili, la chiamata viene bloccata fino a quando non arrivano i dati.</span><span class="sxs-lookup"><span data-stu-id="fbd6d-107">In blocking mode, which is compatible with current implementations of storage objects, if data is unavailable, the call blocks until data arrives.</span></span> <span data-ttu-id="fbd6d-108">In modalità non di blocco, anziché bloccare la chiamata, l'oggetto di archiviazione restituisce un nuovo errore E \_ in sospeso quando i dati non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="fbd6d-108">In nonblocking mode, rather than blocking the call, the storage object returns a new error E\_PENDING when data is unavailable.</span></span> <span data-ttu-id="fbd6d-109">Un client a conoscenza dell'archiviazione e dell'associazione asincrona rileva questo errore e attende altre notifiche ([**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) per ripetere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="fbd6d-109">A client aware of asynchronous binding and storage notes this error and waits for further notifications ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) to retry the operation.</span></span> <span data-ttu-id="fbd6d-110">Un client può scegliere tra un archivio sincrono (bloccante) e asincrono (non bloccante) scegliendo se impostare il \_ flag BINDF ASYNCSTORAGE nel valore *grfBINDF* restituito a [**IBindStatusCallback:: GetBindInfo.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbd6d-110">A client can choose between a synchronous (blocking) and asynchronous (nonblocking) storage by choosing whether to set the BINDF\_ASYNCSTORAGE flag in the *grfBINDF* value returned to [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbd6d-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fbd6d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbd6d-112">Moniker asincroni</span><span class="sxs-lookup"><span data-stu-id="fbd6d-112">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 