---
title: Generazione di una DLL proxy e di una libreria dei tipi da un singolo file IDL
description: È possibile usare un singolo file IDL per generare sia gli stub proxy che i file di intestazione per il marshalling del codice e una libreria dei tipi.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Microsoft Interface Definition Language MIDL , attività, generazione di una DLL proxy e di una libreria dei tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e7bf2694b791007b0f1da303525217cf55d75d574e083c6d1756bc2784d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384237"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a>Generazione di una DLL proxy e di una libreria dei tipi da un singolo file IDL

È possibile usare un singolo file IDL per generare sia gli stub proxy che i file di intestazione per il marshalling del codice e una libreria dei tipi. A tale scopo, definire un'interfaccia all'esterno del blocco di libreria e quindi fare riferimento a tale interfaccia dall'interno del blocco di libreria, come illustrato in questo esempio:

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

Per altre informazioni, vedere [Marshalling di tipi](marshaling-ole-data-types.md) di dati OLE e [file aggiuntivi necessari per generare una libreria dei tipi.](additional-files-required-to-generate-a-type-library-2.md)

 

 




