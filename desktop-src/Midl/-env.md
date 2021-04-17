---
title: opzione/env
description: L'opzione/env consente di selezionare l'ambiente in cui viene eseguita l'applicazione.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- /ENV switch MIDL
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398893"
---
# <a name="env-switch"></a><span data-ttu-id="fde1f-104">opzione/env</span><span class="sxs-lookup"><span data-stu-id="fde1f-104">/env switch</span></span>

<span data-ttu-id="fde1f-105">L'opzione **/ENV** consente di selezionare l'ambiente in cui viene eseguita l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fde1f-105">The **/env** switch selects the environment in which the application runs.</span></span>

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a><span data-ttu-id="fde1f-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="fde1f-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="fde1f-107"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="fde1f-107"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="fde1f-108">Indica al compilatore MIDL di generare file stub o un file di libreria dei tipi per un ambiente a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fde1f-108">Directs the MIDL compiler to generate stub files, or a type library file, for a 32-bit environment.</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="fde1f-109"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="fde1f-109"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="fde1f-110">Indica al compilatore MIDL di generare file stub o un file di libreria dei tipi per un ambiente Intel Architecture 64-bit (IA64).</span><span class="sxs-lookup"><span data-stu-id="fde1f-110">Directs the MIDL compiler to generate stub files, or a type library file, for a Intel Architecture 64-bit (IA64) environment.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="fde1f-111"><span id="amd64"></span><span id="AMD64"></span>amd64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="fde1f-111"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="fde1f-112">Indica al compilatore MIDL di generare file stub o un file di libreria dei tipi per un ambiente di Micro Devices a 64 bit (AMD64) avanzato.</span><span class="sxs-lookup"><span data-stu-id="fde1f-112">Directs the MIDL compiler to generate stub files, or a type library file, for an Advanced Micro Devices 64-bit (AMD64) environment.</span></span>

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span data-ttu-id="fde1f-113"><span id="win64"></span><span id="WIN64"></span>Win64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="fde1f-113"><span id="win64"></span><span id="WIN64"></span>\*\*\*\*win64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="fde1f-114">Stesso comportamento di *ia64*.</span><span class="sxs-lookup"><span data-stu-id="fde1f-114">Same behavior as *ia64*.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fde1f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fde1f-115">Remarks</span></span>

<span data-ttu-id="fde1f-116">L'opzione **/ENV** influiscono principalmente sul livello di compressione usato per le strutture in tale ambiente.</span><span class="sxs-lookup"><span data-stu-id="fde1f-116">The **/env** switch primarily affects the packing level used for structures in that environment.</span></span> <span data-ttu-id="fde1f-117">Assicurarsi di specificare la stessa impostazione a livello di compressione sia per il compilatore MIDL sia per il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="fde1f-117">Be sure you specify the same packing-level setting for both the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="fde1f-118">L'opzione **/ENV** determina il livello di compressione e altre impostazioni come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="fde1f-118">The **/env** switch determines the packing level and other settings as follows:</span></span>

-   <span data-ttu-id="fde1f-119">Quando si specifica **Win32**, gli stub generati usano il livello di compressione del compilatore C 8 per tutti i tipi utilizzati nelle operazioni remote.</span><span class="sxs-lookup"><span data-stu-id="fde1f-119">When you specify **win32**, generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="fde1f-120">I tipi di dati [**int**](int.md) sono entrambi 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fde1f-120">The [**int**](int.md) data types are both 32 bits.</span></span> <span data-ttu-id="fde1f-121">I puntatori sono di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fde1f-121">Pointers are 32 bits.</span></span>
-   <span data-ttu-id="fde1f-122">Quando si specifica **ia64** o **amd64**, il compilatore MIDL viene eseguito in modalità compilatore incrociato per la piattaforma 64 bit indicata (Intel o AMD).</span><span class="sxs-lookup"><span data-stu-id="fde1f-122">When you specify **ia64** or **amd64**, the MIDL compiler runs in a cross-compiler mode for the indicated (Intel or AMD) 64-bit platform.</span></span> <span data-ttu-id="fde1f-123">Gli stub generati usano il livello di compressione del compilatore C 8 per tutti i tipi utilizzati nelle operazioni remote.</span><span class="sxs-lookup"><span data-stu-id="fde1f-123">The generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="fde1f-124">I tipi di dati [**Long**](long.md) e [**int**](int.md) sono di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fde1f-124">The [**long**](long.md) and [**int**](int.md) data types are 32 bits.</span></span> <span data-ttu-id="fde1f-125">I puntatori sono di 64 bit.</span><span class="sxs-lookup"><span data-stu-id="fde1f-125">Pointers are 64 bits.</span></span>

<span data-ttu-id="fde1f-126">Le opzioni [**/align**](-align.md), [**/Pack**](-pack.md)e [**/ZP**](-zp.md) hanno la precedenza sulle impostazioni di **/ENV** .</span><span class="sxs-lookup"><span data-stu-id="fde1f-126">The [**/align**](-align.md), [**/pack**](-pack.md), and [**/Zp**](-zp.md) switches take precedence over the **/env** settings.</span></span>

<span data-ttu-id="fde1f-127">Per ulteriori informazioni sul supporto di 64 bit per MIDL e RPC, vedere [progettazione di interfacce compatibili con 64 bit](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span><span class="sxs-lookup"><span data-stu-id="fde1f-127">For more information on 64 bit support for MIDL and RPC see [Designing 64-bit-Compatible Interfaces](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span></span>

## <a name="examples"></a><span data-ttu-id="fde1f-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="fde1f-128">Examples</span></span>

<span data-ttu-id="fde1f-129">**nome file Win32 MIDL/ENV. idl**</span><span class="sxs-lookup"><span data-stu-id="fde1f-129">**midl /env win32 filename.idl**</span></span>

<span data-ttu-id="fde1f-130">**MIDL/env ia64 nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="fde1f-130">**midl /env ia64 filename.idl**</span></span>

<span data-ttu-id="fde1f-131">**MIDL/ENV amd64 nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="fde1f-131">**midl /env amd64 filename.idl**</span></span>

<span data-ttu-id="fde1f-132">**MIDL/ENV Win64 nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="fde1f-132">**midl /env win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="fde1f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fde1f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde1f-134">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="fde1f-134">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="fde1f-135">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="fde1f-135">**/pack**</span></span>](-pack.md)
</dt> <dt>

[<span data-ttu-id="fde1f-136">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="fde1f-136">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 