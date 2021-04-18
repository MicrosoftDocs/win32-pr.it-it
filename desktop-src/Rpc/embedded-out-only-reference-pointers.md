---
title: Puntatori di riferimento Out-Only incorporati
description: Puntatori di riferimento Out-Only incorporati
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072e9aa3cc3f0f673e4bb737016bc035a3ac496
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300300"
---
# <a name="embedded-out-only-reference-pointers"></a>Puntatori di riferimento Out-Only incorporati

Quando si utilizzano \[ [](/windows/desktop/Midl/out-idl) \] i puntatori di riferimento solo in Microsoft RPC, gli stub del server generati allocano solo il primo livello di puntatori accessibili dal puntatore di riferimento. I puntatori a livelli più profondi non vengono allocati dagli Stub, ma devono essere allocati dal livello dell'applicazione server. Si supponga, ad esempio, che un'interfaccia specifichi una \[  \] matrice di puntatori di riferimento:

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

In questo esempio lo stub del server alloca memoria per 10 puntatori e imposta il valore di ogni puntatore su null. L'applicazione server deve allocare la memoria per i 10 numeri interi [**brevi**](/windows/desktop/Midl/short) a cui fanno riferimento i puntatori, quindi impostare i 10 puntatori in modo che puntino ai numeri interi.

Quando la \[ [](/windows/desktop/Midl/out-idl) \] struttura dei dati di sola uscita include puntatori di riferimento annidati, gli stub del server allocano solo il primo puntatore accessibile dal puntatore di riferimento. Ad esempio:

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

Nell'esempio precedente, gli stub del server allocano il puntatore *psTop* e il **\_ \_ tipo di primo livello dello struct** della struttura. Il puntatore di riferimento *ps1* nel **\_ \_ tipo struct Top** è impostato su null. Lo stub del server non alloca ogni livello della struttura di dati né alloca il **\_ tipo STRUCT1** o il puntatore incorporato, *psValue*.

 

 