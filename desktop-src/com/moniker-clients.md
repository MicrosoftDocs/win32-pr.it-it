---
title: Client moniker
description: I client moniker devono iniziare ottenendo un moniker e esistono diversi modi per ottenere un moniker da un client moniker.
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297747"
---
# <a name="moniker-clients"></a><span data-ttu-id="90b1f-103">Client moniker</span><span class="sxs-lookup"><span data-stu-id="90b1f-103">Moniker Clients</span></span>

<span data-ttu-id="90b1f-104">I client moniker devono iniziare ottenendo un moniker e esistono diversi modi per ottenere un moniker da un client moniker.</span><span class="sxs-lookup"><span data-stu-id="90b1f-104">Moniker clients must start by getting a moniker, and there are several ways for a moniker client to get a moniker.</span></span> <span data-ttu-id="90b1f-105">Ad esempio, nei documenti compositi OLE, quando l'utente finale crea un elemento collegato (usando la finestra di dialogo **Inserisci oggetto** , gli Appunti o il trascinamento della selezione), un moniker viene incorporato come parte dell'elemento collegato.</span><span class="sxs-lookup"><span data-stu-id="90b1f-105">For example, in OLE compound documents, when the end user creates a linked item (either using **Insert Object** dialog, the clipboard, or drag-and drop), a moniker is embedded as part of the linked item.</span></span> <span data-ttu-id="90b1f-106">In tal caso, il programmatore ha un contatto minimo con i moniker.</span><span class="sxs-lookup"><span data-stu-id="90b1f-106">In that case, the programmer has minimal contact with monikers.</span></span> <span data-ttu-id="90b1f-107">A livello di codice, se si dispone di un puntatore di interfaccia a un oggetto che implementa l'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , è possibile utilizzarlo per ottenere un moniker e sono presenti metodi su altre interfacce definite per restituire moniker.</span><span class="sxs-lookup"><span data-stu-id="90b1f-107">Programmatically, if you have an interface pointer to an object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface, you can use that to get a moniker, and there are methods on other interfaces that are defined to return monikers.</span></span>

<span data-ttu-id="90b1f-108">Sono disponibili tipi diversi di moniker, usati per identificare tipi diversi di oggetti, ma a un client moniker, tutti i moniker hanno lo stesso aspetto.</span><span class="sxs-lookup"><span data-stu-id="90b1f-108">There are different kinds of monikers, which are used to identify different kinds of objects, but to a moniker client, all monikers look the same.</span></span> <span data-ttu-id="90b1f-109">Un client moniker chiama semplicemente [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) su un moniker e ottiene un puntatore di interfaccia all'oggetto identificato dal moniker.</span><span class="sxs-lookup"><span data-stu-id="90b1f-109">A moniker client simply calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on a moniker and gets an interface pointer to the object that the moniker identifies.</span></span> <span data-ttu-id="90b1f-110">La chiamata di **BindToObject** restituirà un puntatore a tale oggetto, indipendentemente dal fatto che il moniker identifichi un oggetto di grandi dimensioni come un intero foglio di calcolo o una singola cella in un foglio di calcolo.</span><span class="sxs-lookup"><span data-stu-id="90b1f-110">Whether the moniker identifies an object as large as an entire spreadsheet or as small as a single cell within a spreadsheet, calling **BindToObject** will return a pointer to that object.</span></span> <span data-ttu-id="90b1f-111">Se l'oggetto è già in esecuzione, **BindToObject** lo troverà in memoria.</span><span class="sxs-lookup"><span data-stu-id="90b1f-111">If the object is already running, **BindToObject** will find it in memory.</span></span> <span data-ttu-id="90b1f-112">Se l'oggetto viene archiviato passivamente sul disco, **BindToObject** individuerà un server per tale oggetto, eseguirà il server e consentirà al server di portare l'oggetto in stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="90b1f-112">If the object is stored passively on disk, **BindToObject** will locate a server for that object, run the server, and have the server bring the object into the running state.</span></span> <span data-ttu-id="90b1f-113">Tutti i dettagli del processo di associazione sono nascosti dal client del moniker.</span><span class="sxs-lookup"><span data-stu-id="90b1f-113">All the details of the binding process are hidden from the moniker client.</span></span> <span data-ttu-id="90b1f-114">Pertanto, per un client moniker, l'utilizzo del moniker è molto semplice.</span><span class="sxs-lookup"><span data-stu-id="90b1f-114">Thus, for a moniker client, using the moniker is very simple.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90b1f-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90b1f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90b1f-116">Provider moniker</span><span class="sxs-lookup"><span data-stu-id="90b1f-116">Moniker Providers</span></span>](moniker-providers.md)
</dt> <dt>

[<span data-ttu-id="90b1f-117">Implementazioni del moniker OLE</span><span class="sxs-lookup"><span data-stu-id="90b1f-117">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




