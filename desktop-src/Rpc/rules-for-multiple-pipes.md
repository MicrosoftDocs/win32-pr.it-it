---
title: Regole per più pipe
description: Regole per più pipe in una singola chiamata in RPC (Remote Procedure Call).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d804c132d7fc859906f065e4c9dc39dd3159519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473886"
---
# <a name="rules-for-multiple-pipes"></a>Regole per più pipe

È possibile combinare \[ [](/windows/desktop/Midl/in) \] i parametri in, \[ [**out**](/windows/desktop/Midl/out-idl) \] e \[ **in out** \] pipe in qualsiasi combinazione in una singola chiamata, ma è necessario elaborare le pipe in un ordine specifico, come illustrato nell'esempio di pseudocodice seguente:

> [!Note]  
> Questa funzionalità non è più supportata in Windows Vista e nelle piattaforme successive.

 

-   Ottenere i dati da ogni pipe di input, iniziando dal primo (a sinistra) \[ **nel** \] parametro e continuando in ordine, svuotando ogni pipe prima di iniziare a elaborare la successiva.
-   Dopo che ogni pipe di input è stata completamente elaborata, inviare i dati per le pipe di output, iniziando nuovamente con il primo \[  \] parametro out e continuando in ordine, riempiendo ogni pipe prima di iniziare a elaborare la successiva.

``` syntax
//in .IDL file:
void InOutUCharPipe( [in,out] UCHAR_PIPE *uchar_pipe_1, 
                     [out] UCHAR_PIPE * uchar_pipe_2, 
                     [in] UCHAR_PIPE uchar_pipe_3);
 
//remote procedure:
void InOutUCharPipe( UCHAR_PIPE *param1,
                     UCHAR_PIPE *param2,
                     UCHAR_PIPE  param3)
{
    while(!END_OF_PIPE1)
    {
        param1->pull (. . .);
        . . .
    };

    while(!END_OF_PIPE3)
    {
        param3.pull (. . .);
        . . .
    };

    while(!END_OF_PIPE1)
    {
        param1->push (. . .);
        . . .
    };

    while(!END_OF_PIPE2)
    {
        param2->push(. . .);
        . . .
    };
} //end InOutUCharPipe
```

 

 