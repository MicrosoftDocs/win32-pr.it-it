---
title: Più livelli di puntatori
description: Uso di più livelli di puntatori in RPC (Remote Procedure Call).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c4424679f69daf3a5d88f137d55bd485824ef08498266882d84931a6d03f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019641"
---
# <a name="multiple-levels-of-pointers"></a>Più livelli di puntatori

Quando sono presenti più livelli di puntatori, gli attributi sono associati al puntatore più vicino al nome della variabile. Il client è ancora responsabile dell'allocazione della memoria associata alla risposta.

L'esempio seguente consente lo stub di chiamare il server senza sapere in anticipo la quantità di dati che verranno restituiti:

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

In questo esempio, lo stub passa al server un puntatore univoco, che il server inizializza su **NULL.** Il server alloca quindi un blocco di bar, imposta il puntatore, imposta l'argomento size e restituisce . Si noti che per consentire al server di avere un effetto sul chiamante, è necessario passare un puntatore di riferimento a un \[ \] \[ [**puntatore**](/windows/desktop/Midl/unique) \] univoco ai dati. Si noti anche che la virgola in size è ( , pSize ) , che indica che il puntatore di primo livello non è un puntatore di dimensioni, ma che il puntatore di livello \[ [**\_**](/windows/desktop/Midl/size-is)inferiore \* è \] .

Sul lato client, lo stub imposta \* ppBar su **NULL** prima di chiamare la procedura remota. Lo stub alloca e annulla ilmarsaling dell'arry di oggetti BAR. L'argomento size indica le dimensioni del blocco (e il numero di BAR di cui non è stato esere stato dimarrito). Il client deve liberare la matrice restituita di oggetti BAR quando non è più necessaria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**size \_ è**](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 