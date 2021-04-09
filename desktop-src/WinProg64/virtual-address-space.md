---
title: Spazio degli indirizzi virtuali (Guida per programmatori per Windows a 64 bit)
description: Per impostazione predefinita, le applicazioni basate su Microsoft Windows a 64 bit hanno uno spazio degli indirizzi in modalità utente di diversi terabyte.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- Guida per programmatori Windows a 64 bit-programmazione Windows a 64 bit, spazio degli indirizzi virtuali
- spazio degli indirizzi virtuali programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047666"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a><span data-ttu-id="8f00a-105">Spazio degli indirizzi virtuali (Guida per programmatori per Windows a 64 bit)</span><span class="sxs-lookup"><span data-stu-id="8f00a-105">Virtual Address Space (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="8f00a-106">Per impostazione predefinita, le applicazioni basate su Microsoft Windows a 64 bit hanno uno spazio degli indirizzi in modalità utente di diversi terabyte.</span><span class="sxs-lookup"><span data-stu-id="8f00a-106">By default, 64-bit Microsoft Windows-based applications have a user-mode address space of several terabytes.</span></span> <span data-ttu-id="8f00a-107">Per i valori esatti, vedere [limiti di memoria per le versioni di Windows e Windows Server](/windows/desktop/Memory/memory-limits-for-windows-releases).</span><span class="sxs-lookup"><span data-stu-id="8f00a-107">For precise values, see [Memory Limits for Windows and Windows Server Releases](/windows/desktop/Memory/memory-limits-for-windows-releases).</span></span> <span data-ttu-id="8f00a-108">Tuttavia, le applicazioni possono specificare che il sistema deve allocare tutta la memoria per l'applicazione inferiore a 2 gigabyte.</span><span class="sxs-lookup"><span data-stu-id="8f00a-108">However, applications can specify that the system should allocate all memory for the application below 2 gigabytes.</span></span> <span data-ttu-id="8f00a-109">Questa funzionalità è utile per le applicazioni a 64 bit se vengono soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8f00a-109">This feature is beneficial for 64-bit applications if the following conditions are true:</span></span>

-   <span data-ttu-id="8f00a-110">È sufficiente uno spazio degli indirizzi di 2 GB.</span><span class="sxs-lookup"><span data-stu-id="8f00a-110">A 2 GB address space is sufficient.</span></span>
-   <span data-ttu-id="8f00a-111">Il codice presenta molti avvisi di troncamento del puntatore.</span><span class="sxs-lookup"><span data-stu-id="8f00a-111">The code has many pointer truncation warnings.</span></span>
-   <span data-ttu-id="8f00a-112">I puntatori e i numeri interi sono liberamente combinati.</span><span class="sxs-lookup"><span data-stu-id="8f00a-112">Pointers and integers are freely mixed.</span></span>
-   <span data-ttu-id="8f00a-113">Il codice ha un polimorfismo che usa tipi di dati a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8f00a-113">The code has polymorphism using 32-bit data types.</span></span>

<span data-ttu-id="8f00a-114">Tutti i puntatori sono ancora puntatori a 64 bit, ma il sistema garantisce che ogni allocazione di memoria si verifichi al di sotto del limite di 2 GB, in modo che se l'applicazione tronca un puntatore, non viene perso alcun dato significativo.</span><span class="sxs-lookup"><span data-stu-id="8f00a-114">All pointers are still 64-bit pointers, but the system ensures that every memory allocation occurs below the 2 GB limit, so that if the application truncates a pointer, no significant data is lost.</span></span> <span data-ttu-id="8f00a-115">È possibile troncare i puntatori a valori a 32 bit, quindi estenderli a valori a 64 bit in base all'estensione del segno o all'estensione zero.</span><span class="sxs-lookup"><span data-stu-id="8f00a-115">Pointers can be truncated to 32-bit values, then extended to 64-bit values by either sign extension or zero extension.</span></span>

<span data-ttu-id="8f00a-116">Per specificare questa limitazione della memoria, usare l'opzione **/LARGEADDRESSAWARE: No** linker.</span><span class="sxs-lookup"><span data-stu-id="8f00a-116">To specify this memory limitation, use the **/LARGEADDRESSAWARE:NO** linker option.</span></span> <span data-ttu-id="8f00a-117">Si noti che **/LARGEADDRESSAWARE: No** viene ignorato per un file binario arm64.</span><span class="sxs-lookup"><span data-stu-id="8f00a-117">Note that **/LARGEADDRESSAWARE:NO** is ignored for an ARM64 binary.</span></span> <span data-ttu-id="8f00a-118">Tuttavia, tenere presente che possono verificarsi problemi quando si utilizza questa opzione.</span><span class="sxs-lookup"><span data-stu-id="8f00a-118">However, be aware that problems can occur when using this option.</span></span> <span data-ttu-id="8f00a-119">Se si compila una DLL che usa questa opzione e la DLL viene chiamata da un'applicazione che non usa questa opzione, la DLL potrebbe troncare un puntatore a 64 bit i cui 32 bit superiori sono significativi.</span><span class="sxs-lookup"><span data-stu-id="8f00a-119">If you build a DLL that uses this option and the DLL is called by an application that does not use this option, the DLL could truncate a 64-bit pointer whose upper 32 bits are significant.</span></span> <span data-ttu-id="8f00a-120">Questo può causare un errore dell'applicazione senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="8f00a-120">This can cause application failure without any warning.</span></span>

 

 
