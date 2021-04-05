---
title: Generazione di una DLL proxy e di una libreria dei tipi da un singolo file IDL
description: È possibile utilizzare un singolo file IDL per generare sia gli stub proxy che i file di intestazione per il marshalling del codice e una libreria dei tipi.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Microsoft Interface Definition Language MIDL, attività, generazione di una DLL proxy e di una libreria di tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81001bba7aeff416e765291d3e6660b705919a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045088"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a><span data-ttu-id="a536a-104">Generazione di una DLL proxy e di una libreria dei tipi da un singolo file IDL</span><span class="sxs-lookup"><span data-stu-id="a536a-104">Generating a Proxy DLL and a Type Library from a Single IDL File</span></span>

<span data-ttu-id="a536a-105">È possibile utilizzare un singolo file IDL per generare sia gli stub proxy che i file di intestazione per il marshalling del codice e una libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="a536a-105">You can use a single IDL file to generate both the proxy stubs and header files for marshaling code, and a type library.</span></span> <span data-ttu-id="a536a-106">A tale scopo, è necessario definire un'interfaccia all'esterno del blocco di libreria e quindi fare riferimento a tale interfaccia dall'interno del blocco della libreria, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="a536a-106">You do this by defining an interface outside the library block and then referencing that interface from inside the library block, as shown in this example:</span></span>

``` syntax
//file: AllKnown.idl

[
    object, uuid(. . .), <other interface attributes>
]
interface IKnown : IUnknown 
{
    import "unknwn.idl";
    <declarations, etc. for IKnown interface go here>
};

[
    <library attributes>
]
library KnownLibrary 
{

    //reference interface IKnown:
    interface IKnown;

    //or create a new class:
    [
        <coclass attributes>
    ] 
    coclass KnowMore 
    {
       interface IKnown;
    };
};
```

<span data-ttu-id="a536a-107">Per ulteriori informazioni, vedere [marshalling di tipi di dati OLE](marshaling-ole-data-types.md) e [file aggiuntivi necessari per generare una libreria dei tipi](additional-files-required-to-generate-a-type-library-2.md).</span><span class="sxs-lookup"><span data-stu-id="a536a-107">For more information, see [Marshaling OLE Data Types](marshaling-ole-data-types.md) and [Additional Files Required To Generate a Type Library](additional-files-required-to-generate-a-type-library-2.md).</span></span>

 

 




