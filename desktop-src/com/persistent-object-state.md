---
title: Stato oggetto permanente
description: Stato oggetto permanente
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328980"
---
# <a name="persistent-object-state"></a><span data-ttu-id="106df-103">Stato oggetto permanente</span><span class="sxs-lookup"><span data-stu-id="106df-103">Persistent Object State</span></span>

<span data-ttu-id="106df-104">Alcuni oggetti COM possono salvare lo stato interno quando viene richiesto da un client.</span><span class="sxs-lookup"><span data-stu-id="106df-104">Some COM objects can save their internal state when asked to do so by a client.</span></span>

<span data-ttu-id="106df-105">COM definisce gli standard mediante i quali i client possono richiedere l'inizializzazione, il caricamento e il salvataggio di oggetti da e verso un archivio dati (ad esempio file flat, archiviazione strutturata o memoria).</span><span class="sxs-lookup"><span data-stu-id="106df-105">COM defines standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="106df-106">È responsabilità del cliente gestire la posizione in cui vengono archiviati i dati persistenti dell'oggetto, ma non il formato dei dati.</span><span class="sxs-lookup"><span data-stu-id="106df-106">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span> <span data-ttu-id="106df-107">Gli oggetti COM che rispettano questi standard sono detti *oggetti permanenti*.</span><span class="sxs-lookup"><span data-stu-id="106df-107">COM objects that adhere to these standards are called *persistent objects*.</span></span>

<span data-ttu-id="106df-108">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="106df-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="106df-109">Interfacce oggetto permanenti</span><span class="sxs-lookup"><span data-stu-id="106df-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
-   [<span data-ttu-id="106df-110">Inizializzazione di oggetti permanenti</span><span class="sxs-lookup"><span data-stu-id="106df-110">Initializing Persistent Objects</span></span>](initializing-persistent-objects.md)

## <a name="related-topics"></a><span data-ttu-id="106df-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="106df-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="106df-112">Client e server COM</span><span class="sxs-lookup"><span data-stu-id="106df-112">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




