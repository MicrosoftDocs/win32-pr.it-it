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
# <a name="cstruct_out-switch"></a><span data-ttu-id="d666c-104">/cstruct- \_ opzione</span><span class="sxs-lookup"><span data-stu-id="d666c-104">/cstruct\_out switch</span></span>

<span data-ttu-id="d666c-105">Questa opzione modifica la definizione C di un'interfaccia COM che restituisce le strutture in modo che corrispondano all'ABI fornito da un responsabile dell'implementazione C++.</span><span class="sxs-lookup"><span data-stu-id="d666c-105">This switch modifies the C definition of a COM interface which returns structures to match the ABI a C++ implementer would provide.</span></span>

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a><span data-ttu-id="d666c-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="d666c-106">Switch Options</span></span>

<span data-ttu-id="d666c-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="d666c-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d666c-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d666c-108">Remarks</span></span>

<span data-ttu-id="d666c-109">Alcune definizioni di interfaccia (in particolare quelle in `d3d12.idl` ) contengono `__stdcall` metodi che restituiscono strutture.</span><span class="sxs-lookup"><span data-stu-id="d666c-109">Some interface definitions (notably those in `d3d12.idl`) contain `__stdcall` methods that return structures.</span></span> <span data-ttu-id="d666c-110">Le ABI C e C++ da MSVC differiscono nel modo in cui implementano tali funzioni:</span><span class="sxs-lookup"><span data-stu-id="d666c-110">The C and C++ ABIs from MSVC differ in how they implement such functions:</span></span>

* <span data-ttu-id="d666c-111">C li tratta come funzioni semplici che accettano un `this` puntatore nascosto come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="d666c-111">C treats them as plain functions that take a hidden `this` pointer as the first parameter.</span></span> <span data-ttu-id="d666c-112">Il compilatore applica un'ottimizzazione di struct di piccole dimensioni che consente a struct di dimensioni inferiori a 8 byte (o maggiori se tutti i valori sono a virgola mobile) da restituire nei registri.</span><span class="sxs-lookup"><span data-stu-id="d666c-112">The complier applies a small struct optimization that allows structs smaller than 8 bytes (or larger if all values are floating point) to be returned in registers.</span></span> <span data-ttu-id="d666c-113">Solo le strutture di dimensioni maggiori vengono promosse per usare un parametro nascosto e un valore restituito allocato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="d666c-113">Only larger structures are promoted to use a hidden parameter and caller-allocated return value.</span></span>
* <span data-ttu-id="d666c-114">C++ li considera come funzioni membro.</span><span class="sxs-lookup"><span data-stu-id="d666c-114">C++ treats them as member functions.</span></span> <span data-ttu-id="d666c-115">Il compilatore esegue *sempre* questa operazione inserendo un parametro nascosto (un puntatore a un valore restituito allocato dal chiamante) come secondo parametro, dopo l'indicatore di misura `this` .</span><span class="sxs-lookup"><span data-stu-id="d666c-115">The compiler *always* does so by inserting a hidden parameter (a pointer to a caller-allocated return value) as the second parameter, after the `this` pointer.</span></span> <span data-ttu-id="d666c-116">Restituisce anche lo stesso puntatore del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="d666c-116">It also returns that same pointer as its return value.</span></span>

<span data-ttu-id="d666c-117">Questa opzione impone la definizione C delle interfacce nell'intestazione risultante per presumere che l'implementatore stia usando C++ e che il codice C debba invece usare in modo esplicito l'ABI C++.</span><span class="sxs-lookup"><span data-stu-id="d666c-117">This switch forces the C definition of interfaces in the resulting header to assume that the implementer was using C++, and that the C code should instead explicitly use the C++ ABI.</span></span> <span data-ttu-id="d666c-118">Ciò implica che la funzione include un parametro nascosto per il puntatore al valore restituito e restituisce tale puntatore anziché direttamente la struttura.</span><span class="sxs-lookup"><span data-stu-id="d666c-118">This implies that the function includes a hidden parameter for the return value pointer and returns that pointer instead of the structure directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="d666c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d666c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d666c-120">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="d666c-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>
