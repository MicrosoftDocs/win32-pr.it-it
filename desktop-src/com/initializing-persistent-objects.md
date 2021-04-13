---
title: Inizializzazione di oggetti permanenti
description: Inizializzazione di oggetti permanenti
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211d9d89b7a8f36ab06d9930e45f365e0fb5d4dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399766"
---
# <a name="initializing-persistent-objects"></a><span data-ttu-id="4b5f5-103">Inizializzazione di oggetti permanenti</span><span class="sxs-lookup"><span data-stu-id="4b5f5-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="4b5f5-104">Molte delle interfacce di oggetti persistenti, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [Metodo IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))e [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), consentono ai client di inizializzare gli oggetti in uno stato "aggiornato" o "predefinito".</span><span class="sxs-lookup"><span data-stu-id="4b5f5-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="4b5f5-105">Questo stato iniziale è diverso da quello di un oggetto appena creato, che non ha stato.</span><span class="sxs-lookup"><span data-stu-id="4b5f5-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="4b5f5-106">L'inizializzazione dello stato di un oggetto, anche allo stato predefinito, può essere un'operazione a elevato utilizzo di calcolo o a elevato utilizzo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b5f5-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="4b5f5-107">Separando la creazione dall'inizializzazione, l'inizializzazione può essere eseguita solo quando è effettivamente necessaria e i client possono evitare di inizializzare gli oggetti allo stato predefinito solo per caricare immediatamente i dati archiviati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="4b5f5-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b5f5-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b5f5-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b5f5-109">Interfacce oggetto permanenti</span><span class="sxs-lookup"><span data-stu-id="4b5f5-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 