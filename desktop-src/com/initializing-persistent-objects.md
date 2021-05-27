---
title: Inizializzazione di oggetti persistenti
description: Inizializzazione di oggetti persistenti
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549197"
---
# <a name="initializing-persistent-objects"></a><span data-ttu-id="0f20b-103">Inizializzazione di oggetti persistenti</span><span class="sxs-lookup"><span data-stu-id="0f20b-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="0f20b-104">Diverse interfacce di oggetti persistenti, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))e [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), consentono ai client di inizializzare gli oggetti su uno stato "nuovo" o "predefinito".</span><span class="sxs-lookup"><span data-stu-id="0f20b-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="0f20b-105">Questo stato iniziale è diverso da quello di un oggetto appena creato, che non ha stato.</span><span class="sxs-lookup"><span data-stu-id="0f20b-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="0f20b-106">L'inizializzazione dello stato di un oggetto, anche allo stato predefinito, può essere un'operazione a elevato utilizzo di calcolo o a elevato utilizzo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f20b-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="0f20b-107">Separando la creazione dall'inizializzazione, l'inizializzazione può essere eseguita solo quando è effettivamente necessaria e i client possono evitare di inizializzare gli oggetti allo stato predefinito solo per caricare immediatamente i dati archiviati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0f20b-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f20b-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f20b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f20b-109">Interfacce di oggetti persistenti</span><span class="sxs-lookup"><span data-stu-id="0f20b-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 