---
title: /cstruct_out opzione
description: L'opzione/cstruct_out modifica la definizione C di un'interfaccia COM che restituisce le strutture che corrispondono all'ABI fornito da un responsabile dell'implementazione C++.
keywords:
- /cstruct_out switch MIDL
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 535e1630046b424493e2211c29248c18bf1ed798
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103874734"
---
# <a name="cstruct_out-switch"></a>/cstruct- \_ opzione

Questa opzione modifica la definizione C di un'interfaccia COM che restituisce le strutture in modo che corrispondano all'ABI fornito da un responsabile dell'implementazione C++.

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Alcune definizioni di interfaccia (in particolare quelle in `d3d12.idl` ) contengono `__stdcall` metodi che restituiscono strutture. Le ABI C e C++ da MSVC differiscono nel modo in cui implementano tali funzioni:

* C li tratta come funzioni semplici che accettano un `this` puntatore nascosto come primo parametro. Il compilatore applica un'ottimizzazione di struct di piccole dimensioni che consente a struct di dimensioni inferiori a 8 byte (o maggiori se tutti i valori sono a virgola mobile) da restituire nei registri. Solo le strutture di dimensioni maggiori vengono promosse per usare un parametro nascosto e un valore restituito allocato dal chiamante.
* C++ li considera come funzioni membro. Il compilatore esegue *sempre* questa operazione inserendo un parametro nascosto (un puntatore a un valore restituito allocato dal chiamante) come secondo parametro, dopo l'indicatore di misura `this` . Restituisce anche lo stesso puntatore del valore restituito.

Questa opzione impone la definizione C delle interfacce nell'intestazione risultante per presumere che l'implementatore stia usando C++ e che il codice C debba invece usare in modo esplicito l'ABI C++. Ciò implica che la funzione include un parametro nascosto per il puntatore al valore restituito e restituisce tale puntatore anziché direttamente la struttura.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>
