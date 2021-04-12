---
title: Perché gli oggetti proxy sono necessari
description: Con gli oggetti accessibili, quando un client imposta una funzione hook nel contesto, la DLL in cui è implementata la funzione hook del client viene caricata nello spazio degli indirizzi del server.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d672f48e9c41f23599a8a64585062a126dafb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329916"
---
# <a name="why-proxy-objects-are-needed"></a><span data-ttu-id="8037b-103">Perché gli oggetti proxy sono necessari</span><span class="sxs-lookup"><span data-stu-id="8037b-103">Why Proxy Objects Are Needed</span></span>

<span data-ttu-id="8037b-104">Con gli oggetti accessibili, quando un client imposta una [funzione hook nel contesto](in-context-and-out-of-context-hook-functions.md), la dll in cui è implementata la funzione hook del client viene caricata nello spazio degli indirizzi del server.</span><span class="sxs-lookup"><span data-stu-id="8037b-104">With accessible objects, when a client sets an [in-context hook function](in-context-and-out-of-context-hook-functions.md), the DLL in which the client's hook function is implemented is loaded into the server's address space.</span></span> <span data-ttu-id="8037b-105">In questo caso, quando il client chiama [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) dall'interno della funzione hook, il puntatore a interfaccia restituito punta direttamente al codice nello spazio degli indirizzi del server.</span><span class="sxs-lookup"><span data-stu-id="8037b-105">In this case, when the client calls [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) from within the hook function, the interface pointer that is returned points directly to code in the server's address space.</span></span> <span data-ttu-id="8037b-106">Quando il client chiama una proprietà di interfaccia utilizzando questo puntatore, la libreria Component Object Model (COM) non è associata al marshalling o all'unmarshalling e non è in grado di rilevare se un oggetto viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="8037b-106">When the client calls an interface property using this pointer, the Component Object Model (COM) library is not involved with marshaling or unmarshaling and cannot detect if an object is destroyed.</span></span> <span data-ttu-id="8037b-107">Pertanto, il server deve rilevare questa situazione e restituire un codice di errore al client.</span><span class="sxs-lookup"><span data-stu-id="8037b-107">Therefore, the server must detect this situation and return an error code to the client.</span></span>

 

 




