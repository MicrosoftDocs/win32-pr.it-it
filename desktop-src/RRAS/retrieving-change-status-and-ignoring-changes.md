---
title: Recupero dello stato delle modifiche e delle modifiche ignorate
description: Il client può eseguire una query su Gestione tabelle di routing per verificare se una notifica di una modifica a una destinazione è in sospeso chiamando RtmGetChangeStatus. Questa funzione restituisce TRUE finché il chiamante non recupera questa modifica chiamando RtmGetChangedDests.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a339cbf9ba4e97dfef25b2ebc2020ff94f8e20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709103"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a><span data-ttu-id="03845-104">Recupero dello stato delle modifiche e delle modifiche ignorate</span><span class="sxs-lookup"><span data-stu-id="03845-104">Retrieving Change Status and Ignoring Changes</span></span>

<span data-ttu-id="03845-105">Il client può eseguire una query su Gestione tabelle di routing per verificare se una notifica di una modifica a una destinazione è in sospeso chiamando [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span><span class="sxs-lookup"><span data-stu-id="03845-105">The client can query the routing table manager to find out if a notification of a change to a destination is pending by calling [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span></span> <span data-ttu-id="03845-106">Questa funzione restituisce **true** finché il chiamante non recupera questa modifica chiamando [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span><span class="sxs-lookup"><span data-stu-id="03845-106">This function returns **TRUE** until the caller retrieves this change by calling [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span></span>

<span data-ttu-id="03845-107">Un client può utilizzare questa query per evitare di eseguire un'azione che dovrebbe essere annullata dopo la ricezione e l'elaborazione della notifica di modifica.</span><span class="sxs-lookup"><span data-stu-id="03845-107">A client can use this query to avoid performing an action that would have to be undone after the change notification is received and processed.</span></span> <span data-ttu-id="03845-108">L'uso di questa funzionalità consente al client di lavorare in modo efficiente rinviando determinate operazioni a un momento successivo.</span><span class="sxs-lookup"><span data-stu-id="03845-108">Using this feature allows the client to work efficiently by deferring certain operations to a later time.</span></span>

<span data-ttu-id="03845-109">Il client può anche ignorare una notifica di modifica in sospeso per una destinazione chiamando [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span><span class="sxs-lookup"><span data-stu-id="03845-109">The client can also ignore a pending change notification for a destination by calling [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span> <span data-ttu-id="03845-110">Una chiamata successiva a [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) non restituisce questa destinazione a meno che non si verifichi un'altra modifica dopo la chiamata a [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span><span class="sxs-lookup"><span data-stu-id="03845-110">A later call to [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) does not return this destination unless another change occurs after the call to [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span>

 

 




