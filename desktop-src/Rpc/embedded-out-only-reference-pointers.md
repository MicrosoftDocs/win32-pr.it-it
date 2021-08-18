---
title: Puntatori Out-Only incorporati
description: Puntatori Out-Only incorporati
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d36fc6229c0b155e3fa9a7f66e6cd1fbd742d7ec876264a8706ce81c4150d6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930525"
---
# <a name="embedded-out-only-reference-pointers"></a>Puntatori Out-Only incorporati

Quando si usano puntatori di riferimento di tipo out -only in Microsoft RPC, gli stub del server generati allocano solo il primo livello di puntatori accessibili dal \[ [](/windows/desktop/Midl/out-idl) \] puntatore di riferimento. I puntatori a livelli più bassi non vengono allocati dagli stub, ma devono essere allocati dal livello dell'applicazione server. Si supponga, ad esempio, che un'interfaccia specifichi \[ **una** \] matrice out-only di puntatori di riferimento:

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

In questo esempio lo stub del server alloca memoria per 10 puntatori e imposta il valore di ogni puntatore su Null. L'applicazione server deve allocare la memoria per i 10 [**valori short**](/windows/desktop/Midl/short) integer a cui fanno riferimento i puntatori e quindi impostare i 10 puntatori in modo che puntino ai numeri interi.

Quando la \[ [**struttura dei dati out-only**](/windows/desktop/Midl/out-idl)include puntatori di riferimento annidati, gli stub del server allocano solo il primo puntatore accessibile \] dal puntatore di riferimento. Esempio:

``` syntax
/* IDL file (fragment) */
typedef struct 
{
    [ref] small * psValue;
} STRUCT1_TYPE;

typedef struct 
{
    [ref] STRUCT1_TYPE * ps1;
} STRUCT_TOP_TYPE;

Proc2([out, ref] STRUCT_TOP_TYPE * psTop);
```

Nell'esempio precedente gli stub del server allocano il puntatore *psTop* e la struttura **STRUCT \_ TOP \_ TYPE**. Il puntatore di *riferimento ps1* in **STRUCT \_ TOP \_ TYPE** è impostato su Null. Lo stub del server non alloca tutti i livelli della struttura dei dati, né alloca **STRUCT1 \_ TYPE** o il relativo puntatore incorporato *psValue.*

 

 