---
title: Moniker puntatore
description: Un moniker del puntatore identifica un oggetto che può esistere solo nello stato attivo o in esecuzione. Questo comportamento è diverso da quello delle altre classi dei moniker, che identificano gli oggetti che possono esistere nello stato passivo o attivo.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "104398449"
---
# <a name="pointer-monikers"></a><span data-ttu-id="4b1dd-104">Moniker puntatore</span><span class="sxs-lookup"><span data-stu-id="4b1dd-104">Pointer Monikers</span></span>

<span data-ttu-id="4b1dd-105">Un *moniker del puntatore* identifica un oggetto che può esistere solo nello stato attivo o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-105">A *pointer moniker* identifies an object that can exist only in the active or running state.</span></span> <span data-ttu-id="4b1dd-106">Questo comportamento è diverso da quello delle altre classi dei moniker, che identificano gli oggetti che possono esistere nello stato passivo o attivo.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-106">This differs from other classes of monikers, which identify objects that can exist in either the passive or the active state.</span></span>

<span data-ttu-id="4b1dd-107">Si supponga, ad esempio, che un'applicazione disponga di un oggetto senza rappresentazione permanente.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-107">Suppose, for example, an application has an object that has no persistent representation.</span></span> <span data-ttu-id="4b1dd-108">In genere, se un client dell'applicazione deve accedere a tale oggetto, è sufficiente passare al client un puntatore all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-108">Normally, if a client of your application needs access to that object, you could simply pass the client a pointer to the object.</span></span> <span data-ttu-id="4b1dd-109">Si supponga, tuttavia, che il client stia aspettando un moniker.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-109">However, suppose your client is expecting a moniker.</span></span> <span data-ttu-id="4b1dd-110">L'oggetto non può essere identificato con un moniker di file perché non è archiviato in un file, né con un moniker di elemento, perché non è contenuto in un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-110">The object cannot be identified with a file moniker, because it isn't stored in a file, nor with an item moniker, because it isn't contained in another object.</span></span>

<span data-ttu-id="4b1dd-111">Al contrario, l'applicazione può creare un moniker puntatore, che è un moniker che contiene semplicemente un puntatore internamente e passarlo al client.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-111">Instead, your application can create a pointer moniker, which is a moniker that simply contains a pointer internally, and pass that to the client.</span></span> <span data-ttu-id="4b1dd-112">Il client può gestire questo moniker come qualsiasi altro.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-112">The client can treat this moniker like any other.</span></span> <span data-ttu-id="4b1dd-113">Tuttavia, quando il client chiama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sul moniker del puntatore, il codice del moniker non controlla la tabella degli oggetti in esecuzione (ROT) o carica qualsiasi elemento dalla risorsa di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-113">However, when the client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on the pointer moniker, the moniker code does not check the running object table (ROT) or load anything from storage.</span></span> <span data-ttu-id="4b1dd-114">Al contrario, il codice del moniker chiama semplicemente [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore archiviato all'interno del moniker.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-114">Instead, the moniker code simply calls [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer stored inside the moniker.</span></span>

<span data-ttu-id="4b1dd-115">I moniker del puntatore consentono agli oggetti esistenti solo nello stato attivo o in esecuzione di partecipare alle operazioni del moniker e di essere utilizzati dai client del moniker.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-115">Pointer monikers allow objects that exist only in the active or running state to participate in moniker operations and be used by moniker clients.</span></span> <span data-ttu-id="4b1dd-116">Una differenza importante tra i moniker del puntatore e altre classi di moniker è che i moniker del puntatore non possono essere salvati nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-116">One important difference between pointer monikers and other classes of monikers is that pointer monikers cannot be saved to persistent storage.</span></span> <span data-ttu-id="4b1dd-117">In tal caso, la chiamata al metodo [**IMoniker:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-117">If you do, calling the [**IMoniker::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) method returns an error.</span></span> <span data-ttu-id="4b1dd-118">Ciò significa che i moniker del puntatore sono utili solo in situazioni specializzate.</span><span class="sxs-lookup"><span data-stu-id="4b1dd-118">This means that pointer monikers are useful only in specialized situations.</span></span> <span data-ttu-id="4b1dd-119">Se è necessario usare un moniker puntatore, è possibile usare la funzione [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) .</span><span class="sxs-lookup"><span data-stu-id="4b1dd-119">You can use the [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) function if you need to use a pointer moniker.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b1dd-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b1dd-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b1dd-121">Anti-moniker</span><span class="sxs-lookup"><span data-stu-id="4b1dd-121">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="4b1dd-122">Moniker della classe</span><span class="sxs-lookup"><span data-stu-id="4b1dd-122">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="4b1dd-123">Moniker compositi</span><span class="sxs-lookup"><span data-stu-id="4b1dd-123">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="4b1dd-124">Moniker di file</span><span class="sxs-lookup"><span data-stu-id="4b1dd-124">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="4b1dd-125">Moniker elemento</span><span class="sxs-lookup"><span data-stu-id="4b1dd-125">Item Monikers</span></span>](item-monikers.md)
</dt> </dl>

 

 




