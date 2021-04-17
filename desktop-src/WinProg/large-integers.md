---
title: Numeri interi grandi
description: Le funzioni e le strutture Integer di grandi dimensioni forniscono originariamente supporto per i valori a 64 bit nelle finestre a 32 bit.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- numeri interi grandi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300262"
---
# <a name="large-integers"></a><span data-ttu-id="1bfed-104">Numeri interi grandi</span><span class="sxs-lookup"><span data-stu-id="1bfed-104">Large Integers</span></span>

<span data-ttu-id="1bfed-105">Le funzioni e le strutture Integer di grandi dimensioni forniscono originariamente supporto per i valori a 64 bit nelle finestre a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="1bfed-105">The large integer functions and structures originally provided support for 64-bit values on 32-bit Windows.</span></span> <span data-ttu-id="1bfed-106">A questo punto, il compilatore C può supportare interi a 64 bit a livello nativo.</span><span class="sxs-lookup"><span data-stu-id="1bfed-106">Now, your C compiler may support 64-bit integers natively.</span></span> <span data-ttu-id="1bfed-107">Ad esempio, Microsoft Visual C++ supporta il tipo Integer di dimensioni [**\_ \_ Int64**](/windows/desktop/Midl/--int64) .</span><span class="sxs-lookup"><span data-stu-id="1bfed-107">For example, Microsoft Visual C++ supports the [**\_\_int64**](/windows/desktop/Midl/--int64) sized integer type.</span></span> <span data-ttu-id="1bfed-108">Per ulteriori informazioni, vedere la documentazione inclusa con il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="1bfed-108">For more information, see the documentation included with your C compiler.</span></span>

<span data-ttu-id="1bfed-109">Per informazioni sugli Integer a 64 bit in Windows a 64 bit, vedere [i nuovi tipi di dati](/windows/desktop/WinProg64/the-new-data-types).</span><span class="sxs-lookup"><span data-stu-id="1bfed-109">For information on 64-bit integers on 64-bit Windows, see [The New Data Types](/windows/desktop/WinProg64/the-new-data-types).</span></span>

## <a name="large-integer-operations"></a><span data-ttu-id="1bfed-110">Operazioni integer di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="1bfed-110">Large Integer Operations</span></span>

<span data-ttu-id="1bfed-111">Le applicazioni possono moltiplicare interi a 32 bit firmati o senza segno, generando risultati a 64 bit, usando le funzioni [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) e [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) .</span><span class="sxs-lookup"><span data-stu-id="1bfed-111">Applications can multiply signed or unsigned 32-bit integers, generating 64-bit results, by using the [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) and [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) functions.</span></span> <span data-ttu-id="1bfed-112">Le applicazioni possono spostare i bit nei valori a 64 bit a sinistra o a destra usando le funzioni [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)e [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) .</span><span class="sxs-lookup"><span data-stu-id="1bfed-112">Applications can shift bits in 64-bit values to the left or right by using the [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32), and [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) functions.</span></span> <span data-ttu-id="1bfed-113">Queste funzioni forniscono lo spostamento logico e aritmetico.</span><span class="sxs-lookup"><span data-stu-id="1bfed-113">These functions provide logical and arithmetic shifting.</span></span>

<span data-ttu-id="1bfed-114">Le applicazioni possono anche moltiplicare e dividere i valori a 32 bit in un'unica operazione usando la funzione [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) .</span><span class="sxs-lookup"><span data-stu-id="1bfed-114">Applications can also multiply and divide 32-bit values in a single operation by using the [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) function.</span></span> <span data-ttu-id="1bfed-115">Sebbene il risultato dell'operazione sia un valore a 32 bit, la funzione archivia il risultato intermedio come valore a 64 bit, in modo che le informazioni non vadano perse quando si moltiplicano e si suddividono valori di grandi dimensioni a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="1bfed-115">Although the result of the operation is a 32-bit value, the function stores the intermediate result as a 64-bit value, so that information is not lost when large 32-bit values are multiplied and divided.</span></span>

## <a name="large-integer-reference"></a><span data-ttu-id="1bfed-116">Riferimento Integer grande</span><span class="sxs-lookup"><span data-stu-id="1bfed-116">Large Integer Reference</span></span>

-   [<span data-ttu-id="1bfed-117">Funzioni Integer di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="1bfed-117">Large Integer Functions</span></span>](large-integer-functions.md)
-   [<span data-ttu-id="1bfed-118">Strutture Integer grandi</span><span class="sxs-lookup"><span data-stu-id="1bfed-118">Large Integer Structures</span></span>](large-integer-structures.md)

 

 