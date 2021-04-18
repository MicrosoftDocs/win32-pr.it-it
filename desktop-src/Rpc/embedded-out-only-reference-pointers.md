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
# <a name="embedded-out-only-reference-pointers"></a><span data-ttu-id="48fba-103">Puntatori di riferimento Out-Only incorporati</span><span class="sxs-lookup"><span data-stu-id="48fba-103">Embedded Out-Only Reference Pointers</span></span>

<span data-ttu-id="48fba-104">Quando si utilizzano \[ [](/windows/desktop/Midl/out-idl) \] i puntatori di riferimento solo in Microsoft RPC, gli stub del server generati allocano solo il primo livello di puntatori accessibili dal puntatore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="48fba-104">When you use \[[**out**](/windows/desktop/Midl/out-idl)\]-only reference pointers in Microsoft RPC, the generated server stubs allocate only the first level of pointers accessible from the reference pointer.</span></span> <span data-ttu-id="48fba-105">I puntatori a livelli più profondi non vengono allocati dagli Stub, ma devono essere allocati dal livello dell'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="48fba-105">Pointers at deeper levels are not allocated by the stubs, but must be allocated by the server application layer.</span></span> <span data-ttu-id="48fba-106">Si supponga, ad esempio, che un'interfaccia specifichi una \[  \] matrice di puntatori di riferimento:</span><span class="sxs-lookup"><span data-stu-id="48fba-106">For example, suppose an interface specifies an \[**out**\]-only array of reference pointers:</span></span>

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

<span data-ttu-id="48fba-107">In questo esempio lo stub del server alloca memoria per 10 puntatori e imposta il valore di ogni puntatore su null.</span><span class="sxs-lookup"><span data-stu-id="48fba-107">In this example, the server stub allocates memory for 10 pointers and sets the value of each pointer to null.</span></span> <span data-ttu-id="48fba-108">L'applicazione server deve allocare la memoria per i 10 numeri interi [**brevi**](/windows/desktop/Midl/short) a cui fanno riferimento i puntatori, quindi impostare i 10 puntatori in modo che puntino ai numeri interi.</span><span class="sxs-lookup"><span data-stu-id="48fba-108">The server application must allocate the memory for the 10 [**short**](/windows/desktop/Midl/short) integers referenced by the pointers and then set the 10 pointers to point to the integers.</span></span>

<span data-ttu-id="48fba-109">Quando la \[ [](/windows/desktop/Midl/out-idl) \] struttura dei dati di sola uscita include puntatori di riferimento annidati, gli stub del server allocano solo il primo puntatore accessibile dal puntatore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="48fba-109">When the \[[**out**](/windows/desktop/Midl/out-idl)\]-only data structure includes nested reference pointers, the server stubs allocate only the first pointer accessible from the reference pointer.</span></span> <span data-ttu-id="48fba-110">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="48fba-110">For example:</span></span>

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

<span data-ttu-id="48fba-111">Nell'esempio precedente, gli stub del server allocano il puntatore *psTop* e il **\_ \_ tipo di primo livello dello struct** della struttura.</span><span class="sxs-lookup"><span data-stu-id="48fba-111">In the preceding example, the server stubs allocate the pointer *psTop* and the structure **STRUCT\_TOP\_TYPE**.</span></span> <span data-ttu-id="48fba-112">Il puntatore di riferimento *ps1* nel **\_ \_ tipo struct Top** è impostato su null.</span><span class="sxs-lookup"><span data-stu-id="48fba-112">The reference pointer *ps1* in **STRUCT\_TOP\_TYPE** is set to null.</span></span> <span data-ttu-id="48fba-113">Lo stub del server non alloca ogni livello della struttura di dati né alloca il **\_ tipo STRUCT1** o il puntatore incorporato, *psValue*.</span><span class="sxs-lookup"><span data-stu-id="48fba-113">The server stub does not allocate every level of the data structure, nor does it allocate the **STRUCT1\_TYPE** or its embedded pointer, *psValue*.</span></span>

 

 