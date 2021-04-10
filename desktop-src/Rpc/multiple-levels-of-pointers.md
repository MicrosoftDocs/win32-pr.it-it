---
title: Più livelli di puntatori
description: Utilizzo di più livelli di puntatori in RPC (Remote Procedure Call).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963300"
---
# <a name="multiple-levels-of-pointers"></a>Più livelli di puntatori

Quando sono presenti più livelli di puntatori, gli attributi sono associati al puntatore più vicino al nome della variabile. Il client è ancora responsabile dell'allocazione di memoria associata alla risposta.

L'esempio seguente consente allo stub di chiamare il server senza conoscere in anticipo la quantità di dati che verrà restituita:

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

In questo esempio lo stub passa il server a un puntatore univoco, che il server Inizializza a **null**. Il server alloca quindi un blocco di barre, imposta il puntatore, imposta l'argomento size e restituisce. Si noti che per fare in modo che il server abbia effetto sul chiamante, è necessario passare \[ un \] puntatore Ref a un \[ [](/windows/desktop/Midl/unique) \] puntatore univoco ai dati. Si noti anche che la virgola \[ [**\_ è**](/windows/desktop/Midl/size-is)(, \* psize) \] , che indica che il puntatore di primo livello non è un puntatore di dimensione, ma che il puntatore di livello inferiore è.

Sul lato client lo stub imposta ppBar su \* **null** prima di chiamare la procedura remota. Lo stub alloca quindi ed esegue l'unmarshalling del Arry degli oggetti barra. L'argomento size indica le dimensioni del blocco e il numero di barre di cui è stato effettuato l'unmarshalling. Il client deve liberare la matrice di oggetti barra restituita quando non è più necessaria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**dimensioni \_**](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 