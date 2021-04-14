---
title: Moniker di file
description: Moniker di file
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329188"
---
# <a name="file-monikers"></a><span data-ttu-id="94708-103">Moniker di file</span><span class="sxs-lookup"><span data-stu-id="94708-103">File Monikers</span></span>

<span data-ttu-id="94708-104">I *moniker del file* sono la classe del moniker più semplice.</span><span class="sxs-lookup"><span data-stu-id="94708-104">*File monikers* are the simplest moniker class.</span></span> <span data-ttu-id="94708-105">I moniker dei file possono essere utilizzati per identificare qualsiasi oggetto archiviato nel proprio file.</span><span class="sxs-lookup"><span data-stu-id="94708-105">File monikers can be used to identify any object that is stored in its own file.</span></span> <span data-ttu-id="94708-106">Un moniker di file funge da wrapper per il nome del percorso che il file system nativo assegna al file.</span><span class="sxs-lookup"><span data-stu-id="94708-106">A file moniker acts as a wrapper for the path name the native file system assigns to the file.</span></span> <span data-ttu-id="94708-107">Se si chiama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) per questo moniker, questo oggetto verrà attivato e quindi restituirà un puntatore di interfaccia all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94708-107">Calling [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) for this moniker would cause this object to be activated and then would return an interface pointer to the object.</span></span> <span data-ttu-id="94708-108">L'origine dell'oggetto denominato dal moniker deve fornire un'implementazione dell'interfaccia [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) per supportare l'associazione di un moniker di file.</span><span class="sxs-lookup"><span data-stu-id="94708-108">The source of the object named by the moniker must provide an implementation of the [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) interface to support binding a file moniker.</span></span> <span data-ttu-id="94708-109">I moniker del file possono rappresentare un percorso completo o relativo.</span><span class="sxs-lookup"><span data-stu-id="94708-109">File monikers can represent either a complete or a relative path.</span></span>

<span data-ttu-id="94708-110">Ad esempio, il moniker del file per un oggetto foglio di calcolo archiviato come file C: \\ Work \\MySheet.xls conterrebbe informazioni equivalenti al nome di tale percorso.</span><span class="sxs-lookup"><span data-stu-id="94708-110">For example, the file moniker for a spreadsheet object stored as the file C:\\Work\\MySheet.xls would contain information equivalent to that path name.</span></span> <span data-ttu-id="94708-111">Il moniker, tuttavia, non è necessariamente costituito dalla stessa stringa.</span><span class="sxs-lookup"><span data-stu-id="94708-111">The moniker would not necessarily consist of the same string, however.</span></span> <span data-ttu-id="94708-112">La stringa è semplicemente il *nome displayâ*, una rappresentazione del contenuto del moniker significativo per un utente finale.</span><span class="sxs-lookup"><span data-stu-id="94708-112">The string is just its *displayÂ name*, a representation of the moniker's contents that is meaningful to an end user.</span></span> <span data-ttu-id="94708-113">Il nome visualizzato, disponibile tramite il metodo [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) , viene usato solo quando si visualizza un moniker per un utente finale.</span><span class="sxs-lookup"><span data-stu-id="94708-113">The display name, which is available through the [**IMoniker::GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) method, is used only when displaying a moniker to an end user.</span></span> <span data-ttu-id="94708-114">Questo metodo ottiene il nome visualizzato per qualsiasi classe moniker.</span><span class="sxs-lookup"><span data-stu-id="94708-114">This method gets the display name for any of the moniker classes.</span></span> <span data-ttu-id="94708-115">Internamente, il moniker può archiviare le stesse informazioni in un formato più efficiente per l'esecuzione di operazioni sui moniker ma non significative per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="94708-115">Internally, the moniker may store the same information in a format that is more efficient for performing moniker operations but isn't meaningful to users.</span></span> <span data-ttu-id="94708-116">Quindi, quando lo stesso oggetto viene associato tramite una chiamata al metodo [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) , l'oggetto verrebbe attivato, probabilmente caricando il file nel foglio di calcolo.</span><span class="sxs-lookup"><span data-stu-id="94708-116">Then, when this same object is bound through a call to the [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) method, the object would be activated, probably by loading the file into the spreadsheet.</span></span>

<span data-ttu-id="94708-117">OLE offre ai provider del moniker la funzione di supporto [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) che crea un oggetto moniker del file e restituisce il relativo puntatore al provider.</span><span class="sxs-lookup"><span data-stu-id="94708-117">OLE offers moniker providers the helper function [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) that creates a file moniker object and returns its pointer to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94708-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94708-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94708-119">Anti-moniker</span><span class="sxs-lookup"><span data-stu-id="94708-119">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="94708-120">Moniker della classe</span><span class="sxs-lookup"><span data-stu-id="94708-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="94708-121">Moniker compositi</span><span class="sxs-lookup"><span data-stu-id="94708-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="94708-122">Moniker elemento</span><span class="sxs-lookup"><span data-stu-id="94708-122">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="94708-123">Moniker puntatore</span><span class="sxs-lookup"><span data-stu-id="94708-123">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




