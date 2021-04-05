---
title: Suggerimenti sulla migrazione
description: È importante prendere in considerazione i calcoli degli indirizzi e l'aritmetica dei puntatori quando si porta il codice in Windows a 64 bit.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- Guida per programmatori Windows a 64 bit Guida alla programmazione Windows a 64 bit, suggerimenti per la migrazione
- Suggerimenti per la migrazione programmazione Windows a 64 bit
- compatibilità con la programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711710"
---
# <a name="migration-tips"></a><span data-ttu-id="89850-106">Suggerimenti sulla migrazione</span><span class="sxs-lookup"><span data-stu-id="89850-106">Migration Tips</span></span>

<span data-ttu-id="89850-107">Le due principali aree di interesse quando si esamina il codice per la compatibilità a 64 bit sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="89850-107">The two primary areas of concern when examining your code for 64-bit compatibility are as follows:</span></span>

-   <span data-ttu-id="89850-108">Calcoli degli indirizzi</span><span class="sxs-lookup"><span data-stu-id="89850-108">Address calculations</span></span>
-   <span data-ttu-id="89850-109">Puntatore aritmetico</span><span class="sxs-lookup"><span data-stu-id="89850-109">Pointer arithmetic</span></span>

<span data-ttu-id="89850-110">Per molti motivi, gli sviluppatori hanno archiviato gli indirizzi come valore **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="89850-110">For many reasons, developers have stored addresses as a **ULONG** value.</span></span> <span data-ttu-id="89850-111">Dopo tutto, in Windows a 32 bit, un indirizzo, un puntatore e un valore **ULONG** sono tutti di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="89850-111">After all, on 32-bit Windows, an address, a pointer, and a **ULONG** value are all 32 bits long.</span></span> <span data-ttu-id="89850-112">Tuttavia, in Windows a 64 bit, un indirizzo e un **ULONG** non hanno la stessa lunghezza.</span><span class="sxs-lookup"><span data-stu-id="89850-112">However, on 64-bit Windows, an address and a **ULONG** are not the same length.</span></span> <span data-ttu-id="89850-113">Mentre un **ULONG** rimane un valore a 32 bit, tutti i puntatori sono ora valori a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="89850-113">While a **ULONG** remains a 32-bit value, all pointers are now 64-bit values.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="89850-114">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="89850-114">In this Section</span></span>

-   [<span data-ttu-id="89850-115">Linee guida generali per il porting</span><span class="sxs-lookup"><span data-stu-id="89850-115">General Porting Guidelines</span></span>](general-porting-guidelines.md)
-   [<span data-ttu-id="89850-116">Archiviazione di un valore a 64 bit</span><span class="sxs-lookup"><span data-stu-id="89850-116">Storing a 64-bit Value</span></span>](storing-a-64-bit-value.md)
-   [<span data-ttu-id="89850-117">Errori comuni del compilatore</span><span class="sxs-lookup"><span data-stu-id="89850-117">Common Compiler Errors</span></span>](common-compiler-errors.md)
-   [<span data-ttu-id="89850-118">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="89850-118">Additional Considerations</span></span>](additional-considerations.md)

 

 




