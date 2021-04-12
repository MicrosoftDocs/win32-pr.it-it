---
title: Moniker della classe
description: Sebbene le classi siano in genere identificate direttamente con CLSID per funzioni quali CoCreateInstance o CoGetClassObject, le classi possono ora essere identificate anche con un moniker denominato moniker della classe.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80886ce49ea25d2fb5acbf4dddf550c9d2c3ae29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332196"
---
# <a name="class-monikers"></a><span data-ttu-id="f998b-103">Moniker della classe</span><span class="sxs-lookup"><span data-stu-id="f998b-103">Class Monikers</span></span>

<span data-ttu-id="f998b-104">Sebbene le classi siano in genere identificate direttamente con CLSID per funzioni quali [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), le classi possono ora essere identificate anche con un moniker denominato *moniker della classe*.</span><span class="sxs-lookup"><span data-stu-id="f998b-104">Although classes are typically identified directly with CLSIDs to functions such as [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), classes may also now be identified with a moniker called a *class moniker*.</span></span> <span data-ttu-id="f998b-105">I moniker della classe sono associati all'oggetto classe della classe per cui sono stati creati.</span><span class="sxs-lookup"><span data-stu-id="f998b-105">Class monikers bind to the class object of the class for which they are created.</span></span>

<span data-ttu-id="f998b-106">La possibilità di identificare le classi con un moniker supporta operazioni utili che non sono altrimenti ingombranti.</span><span class="sxs-lookup"><span data-stu-id="f998b-106">The ability to identify classes with a moniker supports useful operations that are otherwise unwieldy.</span></span> <span data-ttu-id="f998b-107">I moniker di file, ad esempio, supportavano tradizionalmente l'associazione completa solo alla classe associata alla classe del file a cui fa riferimento. un moniker di un file di Excel viene associato a un'istanza di un oggetto di Excel e un moniker a un'immagine GIF viene associato a un'istanza del gestore GIF attualmente registrato.</span><span class="sxs-lookup"><span data-stu-id="f998b-107">For example, file monikers traditionally supported rich binding only to the class associated with the class of file they referred to; a moniker to an Excel file would bind to an instance of an Excel object, and a moniker to a GIF image would bind to an instance of the currently registered GIF handler.</span></span> <span data-ttu-id="f998b-108">Un moniker della classe consente di indicare la classe che si vuole usare per modificare un file tramite la composizione con un moniker del file.</span><span class="sxs-lookup"><span data-stu-id="f998b-108">A class moniker allows you to indicate the class you want to use to manipulate a file through composition with a file moniker.</span></span> <span data-ttu-id="f998b-109">Un moniker della classe per una classe di grafici 3D costituito da un moniker a un file di Excel produce un moniker associato a un'istanza dell'oggetto grafico 3D e Inizializza l'oggetto con il contenuto del file di Excel.</span><span class="sxs-lookup"><span data-stu-id="f998b-109">A class moniker for a 3D charting class composed with a moniker to an Excel file yields a moniker that binds to an instance of the 3D charting object and initializes the object with the contents of the Excel file.</span></span>

<span data-ttu-id="f998b-110">I moniker della classe sono pertanto molto utili in composizione con altri tipi di moniker, ad esempio moniker di file o moniker di elemento.</span><span class="sxs-lookup"><span data-stu-id="f998b-110">Class monikers are therefore most useful in composition with other types of monikers, such as file monikers or item monikers.</span></span>

<span data-ttu-id="f998b-111">I moniker della classe possono anche essere composti a destra dei moniker che supportano l'associazione all'interfaccia [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) .</span><span class="sxs-lookup"><span data-stu-id="f998b-111">Class monikers may also be composed to the right of monikers supporting binding to the [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) interface.</span></span> <span data-ttu-id="f998b-112">Quando è composto in questo modo, **IClassActivator** fornisce semplicemente l'accesso all'oggetto della classe e alle istanze della classe tramite [**IClassActivator:: GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span><span class="sxs-lookup"><span data-stu-id="f998b-112">When composed in this manner, **IClassActivator** simply gives access to the class object and instances of the class through [**IClassActivator::GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span></span> <span data-ttu-id="f998b-113">I moniker della classe possono essere identificati tramite [**IMoniker:: IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), che restituisce MKSYS \_ CLASSMONIKER in *pdwMksys*.</span><span class="sxs-lookup"><span data-stu-id="f998b-113">Class monikers may be identified through [**IMoniker::IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), which returns MKSYS\_CLASSMONIKER in *pdwMksys*.</span></span>

<span data-ttu-id="f998b-114">I programmatori in genere creano moniker di classe usando la funzione [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) o [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span><span class="sxs-lookup"><span data-stu-id="f998b-114">Programmers typically create class monikers using the [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) function or through [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span></span> <span data-ttu-id="f998b-115">Per informazioni dettagliate, vedere [**IMoniker::P arsedisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) .</span><span class="sxs-lookup"><span data-stu-id="f998b-115">(See [**IMoniker::ParseDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) for details.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f998b-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f998b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f998b-117">Anti-moniker</span><span class="sxs-lookup"><span data-stu-id="f998b-117">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="f998b-118">Moniker compositi</span><span class="sxs-lookup"><span data-stu-id="f998b-118">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="f998b-119">Moniker di file</span><span class="sxs-lookup"><span data-stu-id="f998b-119">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="f998b-120">Moniker elemento</span><span class="sxs-lookup"><span data-stu-id="f998b-120">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="f998b-121">Moniker puntatore</span><span class="sxs-lookup"><span data-stu-id="f998b-121">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




