---
title: Immissione dello stato caricato
description: Immissione dello stato caricato
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709442"
---
# <a name="entering-the-loaded-state"></a><span data-ttu-id="0c8bc-103">Immissione dello stato caricato</span><span class="sxs-lookup"><span data-stu-id="0c8bc-103">Entering the Loaded State</span></span>

<span data-ttu-id="0c8bc-104">Quando un oggetto passa allo stato Loaded, vengono create le strutture in memoria che rappresentano l'oggetto, in modo che sia possibile richiamare le operazioni su di esso.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-104">When an object enters the loaded state, the in-memory structures representing the object are created so that operations can be invoked on it.</span></span> <span data-ttu-id="0c8bc-105">Il gestore dell'oggetto o il server in-process viene caricato.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-105">The object's handler or in-process server is loaded.</span></span> <span data-ttu-id="0c8bc-106">Questo processo, denominato creazione di *istanza*, si verifica quando un oggetto viene caricato dall'archivio permanente (una transizione dallo stato passivo a quello caricato) o quando viene creato un oggetto per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-106">This process, referred to as *instantiation*, occurs when an object is loaded from persistent storage (a transition from the passive to the loaded state) or when an object is being created for the first time.</span></span>

<span data-ttu-id="0c8bc-107">Internamente, la creazione di istanze è un processo in due fasi.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-107">Internally, instantiation is a two-phase process.</span></span> <span data-ttu-id="0c8bc-108">Viene creato un oggetto della classe appropriata, dopo il quale viene chiamato un metodo su tale oggetto per eseguire l'inizializzazione e consentire l'accesso ai dati dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-108">An object of the appropriate class is created, after which a method on that object is called to perform initialization and give access to the object's data.</span></span> <span data-ttu-id="0c8bc-109">Il metodo di inizializzazione è definito in una delle interfacce supportate dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-109">The initialization method is defined in one of the object's supported interfaces.</span></span> <span data-ttu-id="0c8bc-110">Il metodo di inizializzazione specifico chiamato dipende dal contesto in cui viene creata un'istanza dell'oggetto e dal percorso dei dati di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="0c8bc-110">The particular initialization method called depends on the context in which the object is being instantiated and the location of the initialization data.</span></span>

 

 




