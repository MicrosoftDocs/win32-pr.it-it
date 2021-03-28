---
description: Utilizzare la funzione EventWriteTransfer quando più componenti desiderano correlare gli eventi in uno scenario di traccia end-to-end.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Scrittura di eventi correlati in un provider basato su manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527282"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a><span data-ttu-id="8891f-103">Scrittura di eventi correlati in un provider basato su manifesto</span><span class="sxs-lookup"><span data-stu-id="8891f-103">Writing Related Events in a Manifest-based Provider</span></span>

<span data-ttu-id="8891f-104">Utilizzare la funzione [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) quando più componenti desiderano correlare gli eventi in uno scenario di traccia end-to-end.</span><span class="sxs-lookup"><span data-stu-id="8891f-104">Use the [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) function when several components want to relate their events in an end-to-end tracing scenario.</span></span> <span data-ttu-id="8891f-105">I componenti A, B e C, ad esempio, eseguono operazioni su un'attività correlata e vogliono collegare tutti gli eventi correlati a tale attività.</span><span class="sxs-lookup"><span data-stu-id="8891f-105">For example, components A, B and C perform work on a related activity and want to link all the events related to that activity.</span></span>

<span data-ttu-id="8891f-106">ETW usa l'archiviazione locale di thread per rendere disponibile l'identificatore di attività del componente precedente al componente successivo.</span><span class="sxs-lookup"><span data-stu-id="8891f-106">ETW uses thread local storage to make the previous component's activity identifier available to the next component.</span></span> <span data-ttu-id="8891f-107">Il componente recupera l'identificatore del componente precedente dalla risorsa di archiviazione locale e ne imposta l'identificatore di attività correlato.</span><span class="sxs-lookup"><span data-stu-id="8891f-107">The component retrieves the previous component's identifier from the local storage and sets the related activity identifier to it.</span></span> <span data-ttu-id="8891f-108">Il consumer può quindi utilizzare l'identificatore di attività correlato per scorrere la catena degli eventi da un componente a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="8891f-108">The consumer can then use the related activity identifier to walk the chain of the events from one component to the next.</span></span>

 

 



