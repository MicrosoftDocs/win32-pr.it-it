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
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a>Generazione di una DLL proxy e di una libreria dei tipi da un singolo file IDL

È possibile utilizzare un singolo file IDL per generare sia gli stub proxy che i file di intestazione per il marshalling del codice e una libreria dei tipi. A tale scopo, è necessario definire un'interfaccia all'esterno del blocco di libreria e quindi fare riferimento a tale interfaccia dall'interno del blocco della libreria, come illustrato nell'esempio seguente:

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

Per ulteriori informazioni, vedere [marshalling di tipi di dati OLE](marshaling-ole-data-types.md) e [file aggiuntivi necessari per generare una libreria dei tipi](additional-files-required-to-generate-a-type-library-2.md).

 

 




