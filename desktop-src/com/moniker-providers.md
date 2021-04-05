---
title: Provider moniker
description: Provider moniker
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710351"
---
# <a name="moniker-providers"></a><span data-ttu-id="24af7-103">Provider moniker</span><span class="sxs-lookup"><span data-stu-id="24af7-103">Moniker Providers</span></span>

<span data-ttu-id="24af7-104">In generale, un componente deve essere un provider del moniker quando consente l'accesso a uno dei relativi oggetti, controllando comunque l'archiviazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="24af7-104">In general, a component should be a moniker provider when it allows access to one of its objects, while still controlling the object's storage.</span></span> <span data-ttu-id="24af7-105">Se un componente distribuisce moniker che identificano gli oggetti, deve essere in grado di eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="24af7-105">If a component is going to hand out monikers that identify its objects, it must be capable of performing the following tasks:</span></span>

-   <span data-ttu-id="24af7-106">Su richiesta, creare un moniker che identifichi un oggetto.</span><span class="sxs-lookup"><span data-stu-id="24af7-106">On request, create a moniker that identifies an object.</span></span>
-   <span data-ttu-id="24af7-107">Consente di associare il moniker quando un client chiama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) .</span><span class="sxs-lookup"><span data-stu-id="24af7-107">Enable the moniker to be bound when a client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on it.</span></span>

<span data-ttu-id="24af7-108">Un provider del moniker deve creare un moniker di una *classe di moniker* appropriata per identificare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="24af7-108">A moniker provider must create a moniker of an appropriate *moniker class* to identify an object.</span></span> <span data-ttu-id="24af7-109">La classe moniker si riferisce a un'implementazione specifica dell'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) che definisce il tipo di moniker creato.</span><span class="sxs-lookup"><span data-stu-id="24af7-109">The moniker class refers to a specific implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface that defines the type of moniker created.</span></span> <span data-ttu-id="24af7-110">Sebbene sia possibile implementare **IMoniker** per creare una nuova classe moniker, spesso non è necessario perché OLE fornisce implementazioni di diverse classi moniker, ciascuna con il proprio CLSID.</span><span class="sxs-lookup"><span data-stu-id="24af7-110">While you can implement **IMoniker** to create a new moniker class, it is frequently unnecessary because OLE provides implementations of several different moniker classes, each with its own CLSID.</span></span> <span data-ttu-id="24af7-111">Vedere [implementazioni del moniker OLE](ole-moniker-implementations.md) per le descrizioni delle classi moniker fornite da OLE.</span><span class="sxs-lookup"><span data-stu-id="24af7-111">See [OLE Moniker Implementations](ole-moniker-implementations.md) for descriptions of moniker classes that OLE provides.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24af7-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24af7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24af7-113">Client moniker</span><span class="sxs-lookup"><span data-stu-id="24af7-113">Moniker Clients</span></span>](moniker-clients.md)
</dt> <dt>

[<span data-ttu-id="24af7-114">Implementazioni del moniker OLE</span><span class="sxs-lookup"><span data-stu-id="24af7-114">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




