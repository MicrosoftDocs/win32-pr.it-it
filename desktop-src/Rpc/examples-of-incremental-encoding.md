---
title: Esempi di codifica incrementale
description: Nella sezione seguente viene fornito un esempio di come usare l'handle di serializzazione dello stile incrementale per la codifica dei tipi.
ms.assetid: c50c0de3-aabb-4166-93dc-67b0fee66635
keywords:
- Chiamata di procedura remota RPC , attività, con codifica incrementale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d80b7f9b8ddb2acf31626da581996a667a7d2f7a395d419ea8da4c36c60d40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021412"
---
# <a name="examples-of-incremental-encoding"></a>Esempi di codifica incrementale

Nella sezione seguente viene fornito un esempio di come usare l'handle di serializzazione dello stile incrementale per la codifica dei tipi.

``` syntax
/* This is an acf file. MooType is defined in the idl file */

[    explicit_handle
]
interface regress
{
typedef [ encode,decode ] MooType;
}
```

L'estratto seguente rappresenta i frammenti dell'applicazione pertinenti.


```C++
if (MesEncodeIncrementalHandleCreate (State, AllocFn, WriteFn, 
    &Handle) == RPC_S_OK)
{
//...
/* The serialize works from the beginning of the buffer because
    the handle is in the initial state. The Moo_Encode does the
    following:
    - sizes *pMooObject for marshalling,
    - calls AllocFn with the size obtained,
    - marshalls into the buffer returned by Alloc, and
    - calls WriteFn with the filled buffer 
*/

Moo_Encode ( Handle, pMooObject );
...
}
if (MesIncrementalHandleReset (Handle, NULL, NULL, NULL, ReadFn,
    MES_DECODE ) == RPC_OK)
{
/*The ReadFn is needed to reset the handle. The arguments
    that are NULL do not change. You can also call 
    MesDecodeIncrementalHandleCreate (State, ReadFn, &Handle);
    The Moo_Decode does the following:
    - calls Read with the appropriate size of data to read and
        receives a buffer with the data
    - unmarshalls the object from the buffer into *pMooObject 
*/

Moo_Decode ( Handle, pMooObject );
//...
MesHandleFree ( Handle );
}
```



 

 




