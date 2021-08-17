---
title: Regole per più pipe
description: Regole per più pipe in una singola chiamata in RPC (Remote Procedure Call).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fd2de7a44f63d5c943f1d6526ee328bbae3e63c99bac118ec843ad266d1f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925978"
---
# <a name="rules-for-multiple-pipes"></a>Regole per più pipe

È possibile combinare in , out e in, i parametri della pipe out in qualsiasi combinazione in una singola chiamata, ma è necessario elaborare le pipe in un ordine specifico, come illustrato nell'esempio \[ [](/windows/desktop/Midl/in) \] \[ [](/windows/desktop/Midl/out-idl) \] \[  \] di pseudocodice seguente:

> [!Note]  
> Questa funzionalità non è più supportata in Windows Vista e nelle piattaforme successive.

 

-   Ottenere i dati da ogni pipe di input, a partire dal primo parametro (più a sinistra) e continuando nell'ordine, svuotando ogni pipe prima di iniziare a elaborare \[  \] la successiva.
-   Dopo che ogni pipe di input è stata completamente elaborata, inviare i dati per le pipe di output, iniziando di nuovo con il primo parametro out e continuando \[  nell'ordine, riempiendo ogni pipe prima di iniziare a elaborare la \] successiva.

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

 

 