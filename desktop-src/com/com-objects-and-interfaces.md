---
title: Oggetti e interfacce COM
description: Oggetti e interfacce COM
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707786"
---
# <a name="com-objects-and-interfaces"></a><span data-ttu-id="ce778-103">Oggetti e interfacce COM</span><span class="sxs-lookup"><span data-stu-id="ce778-103">COM Objects and Interfaces</span></span>

<span data-ttu-id="ce778-104">COM è una tecnologia che consente agli oggetti di interagire tra i confini dei processi e dei computer con la stessa facilità con cui avviene all'interno di un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="ce778-104">COM is a technology that allows objects to interact across process and computer boundaries as easily as within a single process.</span></span> <span data-ttu-id="ce778-105">COM consente di specificare che l'unico modo per modificare i dati associati a un oggetto consiste nell'usare un' *interfaccia* sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ce778-105">COM enables this by specifying that the only way to manipulate the data associated with an object is through an *interface* on the object.</span></span> <span data-ttu-id="ce778-106">Quando questo termine viene usato in questa documentazione, si riferisce a un'implementazione nel codice di un'interfaccia conforme a binari COM associata a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="ce778-106">When this term is used in this documentation, it refers to an implementation in code of a COM binary-compliant interface that is associated with an object.</span></span>

<span data-ttu-id="ce778-107">COM usa l' *interfaccia* di Word in un senso diverso da quello usato in genere nella programmazione Visual C++.</span><span class="sxs-lookup"><span data-stu-id="ce778-107">COM uses the word *interface* in a sense different from that typically used in Visual C++ programming.</span></span> <span data-ttu-id="ce778-108">Un'interfaccia C++ fa riferimento a tutte le funzioni supportate da una classe e che i client di un oggetto possono chiamare per interagire con esso.</span><span class="sxs-lookup"><span data-stu-id="ce778-108">A C++ interface refers to all of the functions that a class supports and that clients of an object can call to interact with it.</span></span> <span data-ttu-id="ce778-109">Un'interfaccia COM fa riferimento a un gruppo predefinito di funzioni correlate implementate da una classe COM, ma un'interfaccia specifica non rappresenta necessariamente tutte le funzioni supportate dalla classe.</span><span class="sxs-lookup"><span data-stu-id="ce778-109">A COM interface refers to a predefined group of related functions that a COM class implements, but a specific interface does not necessarily represent all the functions that the class supports.</span></span>

<span data-ttu-id="ce778-110">Il riferimento a un oggetto che *implementa* un'interfaccia significa che l'oggetto utilizza codice che implementa ogni metodo dell'interfaccia e fornisce puntatori conformi a binari com a tali funzioni alla libreria com.</span><span class="sxs-lookup"><span data-stu-id="ce778-110">Referring to an object *implementing* an interface means that the object uses code that implements each method of the interface and provides COM binary-compliant pointers to those functions to the COM library.</span></span> <span data-ttu-id="ce778-111">COM rende quindi tali funzioni disponibili a qualsiasi client che chiede un puntatore all'interfaccia, indipendentemente dal fatto che il client si trovi all'interno o all'esterno del processo che implementa tali funzioni.</span><span class="sxs-lookup"><span data-stu-id="ce778-111">COM then makes those functions available to any client who asks for a pointer to the interface, whether the client is inside or outside of the process that implements those functions.</span></span>

<span data-ttu-id="ce778-112">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="ce778-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="ce778-113">Interfacce e implementazioni di interfaccia</span><span class="sxs-lookup"><span data-stu-id="ce778-113">Interfaces and Interface Implementations</span></span>](interfaces-and-interface-implementations.md)
-   [<span data-ttu-id="ce778-114">Puntatori a interfaccia e interfacce</span><span class="sxs-lookup"><span data-stu-id="ce778-114">Interface Pointers and Interfaces</span></span>](interface-pointers-and-interfaces.md)
-   [<span data-ttu-id="ce778-115">IUnknown ed ereditarietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="ce778-115">IUnknown and Interface Inheritance</span></span>](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a><span data-ttu-id="ce778-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce778-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce778-117">Interfacce</span><span class="sxs-lookup"><span data-stu-id="ce778-117">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 




