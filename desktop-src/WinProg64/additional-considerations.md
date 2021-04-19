---
title: Ulteriori considerazioni
description: Quando si porta il codice, considerare i punti seguenti.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- Suggerimenti per il porting per la programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323774"
---
# <a name="additional-considerations"></a><span data-ttu-id="f993e-104">Ulteriori considerazioni</span><span class="sxs-lookup"><span data-stu-id="f993e-104">Additional Considerations</span></span>

<span data-ttu-id="f993e-105">Quando si porta il codice, considerare i punti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f993e-105">When porting your code, consider the following points:</span></span>

- <span data-ttu-id="f993e-106">Il presupposto seguente non è più valido:</span><span class="sxs-lookup"><span data-stu-id="f993e-106">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   <span data-ttu-id="f993e-107">Tuttavia, il compilatore a 64 bit definisce \_ Win32 per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="f993e-107">However, the 64-bit compiler defines \_WIN32 for backward compatibility.</span></span>

- <span data-ttu-id="f993e-108">Il presupposto seguente non è più valido:</span><span class="sxs-lookup"><span data-stu-id="f993e-108">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   <span data-ttu-id="f993e-109">In questo caso, la clausola else può rappresentare \_ Win32 o \_ Win64.</span><span class="sxs-lookup"><span data-stu-id="f993e-109">In this case, the else clause can represent \_WIN32 or \_WIN64.</span></span>

- <span data-ttu-id="f993e-110">Prestare attenzione all'allineamento del tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="f993e-110">Be careful with data-type alignment.</span></span> <span data-ttu-id="f993e-111">La macro di **\_ allineamento dei tipi** restituisce i requisiti di allineamento di un tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="f993e-111">The **TYPE\_ALIGNMENT** macro returns the alignment requirements of a data type.</span></span> <span data-ttu-id="f993e-112">Ad esempio: `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 su x86, 8 su processore Intel Itanium `TYPE_ALIGNMENT( UCHAR )` = = 1 ovunque</span><span class="sxs-lookup"><span data-stu-id="f993e-112">For example: `TYPE_ALIGNMENT( KFLOATING_SAVE )` == 4 on x86, 8 on Intel Itanium processor`TYPE_ALIGNMENT( UCHAR )` == 1 everywhere</span></span>

    <span data-ttu-id="f993e-113">Ad esempio, il codice del kernel che attualmente ha un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="f993e-113">As an example, kernel code that currently looks like this:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    <span data-ttu-id="f993e-114">è probabilmente necessario modificare in:</span><span class="sxs-lookup"><span data-stu-id="f993e-114">should probably be changed to:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    <span data-ttu-id="f993e-115">Le correzioni automatiche delle eccezioni di allineamento in modalità kernel sono disabilitate per i sistemi Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="f993e-115">Automatic fixes of kernel-mode alignment exceptions are disabled for Intel Itanium systems.</span></span>

- <span data-ttu-id="f993e-116">Prestare attenzione con le operazioni NOT.</span><span class="sxs-lookup"><span data-stu-id="f993e-116">Be careful with NOT operations.</span></span> <span data-ttu-id="f993e-117">Considerare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="f993e-117">Consider the following:</span></span>

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    <span data-ttu-id="f993e-118">Il problema è che ~ (b-1) produce "0x0000 0000 xxxx xxxx" e non "0xFFFF FFFF xxxx xxxx".</span><span class="sxs-lookup"><span data-stu-id="f993e-118">The problem is that ~(b–1) produces "0x0000 0000 xxxx xxxx" and not "0xFFFF FFFF xxxx xxxx".</span></span> <span data-ttu-id="f993e-119">Il compilatore non riuscirà a rilevare questo problema.</span><span class="sxs-lookup"><span data-stu-id="f993e-119">The compiler will not detect this.</span></span> <span data-ttu-id="f993e-120">Per risolvere il problema, modificare il codice nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="f993e-120">To fix this, change the code as follows:</span></span>

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- <span data-ttu-id="f993e-121">Prestare attenzione a eseguire operazioni senza segno e firmate.</span><span class="sxs-lookup"><span data-stu-id="f993e-121">Be careful performing unsigned and signed operations.</span></span> <span data-ttu-id="f993e-122">Considerare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="f993e-122">Consider the following:</span></span>

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    <span data-ttu-id="f993e-123">Il risultato è inaspettatamente grande.</span><span class="sxs-lookup"><span data-stu-id="f993e-123">The result is unexpectedly large.</span></span> <span data-ttu-id="f993e-124">La regola è che se uno degli operandi è senza segno, il risultato è senza segno.</span><span class="sxs-lookup"><span data-stu-id="f993e-124">The rule is that if either operand is unsigned, the result is unsigned.</span></span> <span data-ttu-id="f993e-125">Nell'esempio precedente, un oggetto viene convertito in un valore senza segno, diviso per b, e il risultato archiviato in c.</span><span class="sxs-lookup"><span data-stu-id="f993e-125">In the preceding example, a is converted to an unsigned value, divided by b, and the result stored in c.</span></span> <span data-ttu-id="f993e-126">La conversione non prevede alcuna manipolazione numerica.</span><span class="sxs-lookup"><span data-stu-id="f993e-126">The conversion involves no numeric manipulation.</span></span>

    <span data-ttu-id="f993e-127">Come altro esempio, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="f993e-127">As another example, consider the following:</span></span>

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    <span data-ttu-id="f993e-128">Il problema si verifica perché x è senza segno, il che rende l'intera espressione senza segno.</span><span class="sxs-lookup"><span data-stu-id="f993e-128">The problem arises because x is unsigned, which makes the entire expression unsigned.</span></span> <span data-ttu-id="f993e-129">Questa operazione funziona correttamente, a meno che y non sia negativo.</span><span class="sxs-lookup"><span data-stu-id="f993e-129">This works fine unless y is negative.</span></span> <span data-ttu-id="f993e-130">In questo caso, y viene convertito in un valore senza segno, l'espressione viene valutata con precisione a 32 bit, ridimensionata e aggiunta a pVar1.</span><span class="sxs-lookup"><span data-stu-id="f993e-130">In this case, y is converted to an unsigned value, the expression is evaluated using 32-bit precision, scaled, and added to pVar1.</span></span> <span data-ttu-id="f993e-131">Un numero negativo senza segno a 32 bit diventa un numero positivo a 64 bit di grandi dimensioni, che fornisce il risultato errato.</span><span class="sxs-lookup"><span data-stu-id="f993e-131">A 32-bit unsigned negative number becomes a large 64-bit positive number, which gives the wrong result.</span></span> <span data-ttu-id="f993e-132">Per risolvere il problema, dichiarare x come valore con segno o typecast in modo esplicito a **Long** nell'espressione.</span><span class="sxs-lookup"><span data-stu-id="f993e-132">To fix this problem, declare x as a signed value or explicitly typecast it to **LONG** in the expression.</span></span>

- <span data-ttu-id="f993e-133">Prestare attenzione quando si effettuano allocazioni di dimensioni a fasi.</span><span class="sxs-lookup"><span data-stu-id="f993e-133">Be careful when making piecemeal size allocations.</span></span> <span data-ttu-id="f993e-134">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="f993e-134">For example:</span></span>

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    <span data-ttu-id="f993e-135">Il codice seguente non è corretto perché il compilatore riempie la struttura con altri 4 byte per rendere l'allineamento a 8 byte:</span><span class="sxs-lookup"><span data-stu-id="f993e-135">The following code is wrong because the compiler will pad the structure with an additional 4 bytes to make the 8-byte alignment:</span></span>

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    <span data-ttu-id="f993e-136">Il codice seguente è corretto:</span><span class="sxs-lookup"><span data-stu-id="f993e-136">The following code is correct:</span></span>

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- <span data-ttu-id="f993e-137">Non passare `(HANDLE)0xFFFFFFFF` a funzioni come [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span><span class="sxs-lookup"><span data-stu-id="f993e-137">Do not pass `(HANDLE)0xFFFFFFFF` to functions such as [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span></span> <span data-ttu-id="f993e-138">Usare invece un **\_ \_ valore di handle non valido**.</span><span class="sxs-lookup"><span data-stu-id="f993e-138">Instead, use **INVALID\_HANDLE\_VALUE**.</span></span>
- <span data-ttu-id="f993e-139">Usare gli identificatori di formato corretti durante la stampa di una stringa.</span><span class="sxs-lookup"><span data-stu-id="f993e-139">Use the proper format specifiers when printing a string.</span></span> <span data-ttu-id="f993e-140">Utilizzare% p per stampare i puntatori in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="f993e-140">Use %p to print pointers in hexadecimal.</span></span> <span data-ttu-id="f993e-141">Questa è la scelta migliore per i puntatori alla stampa.</span><span class="sxs-lookup"><span data-stu-id="f993e-141">This is the best choice for printing pointers.</span></span> <span data-ttu-id="f993e-142">Microsoft Visual C++ supporta% I per stampare i dati polimorfici.</span><span class="sxs-lookup"><span data-stu-id="f993e-142">Microsoft Visual C++ supports %I to print polymorphic data.</span></span> <span data-ttu-id="f993e-143">Visual C++ supporta anche% I64 per stampare valori con 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f993e-143">Visual C++ also supports %I64 to print values that are 64 bits.</span></span>

 

 