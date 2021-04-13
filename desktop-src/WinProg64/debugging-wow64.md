---
title: Debug di WOW64
description: È possibile eseguire il debug di applicazioni in esecuzione in WOW64 con un debugger ospitato da x86 o un debugger nativo.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- Programmazione Windows WOW64 a 64 bit, debug
- debug della programmazione Windows WOW64 a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399585"
---
# <a name="debugging-wow64"></a><span data-ttu-id="02e5a-105">Debug di WOW64</span><span class="sxs-lookup"><span data-stu-id="02e5a-105">Debugging WOW64</span></span>

<span data-ttu-id="02e5a-106">È possibile eseguire il debug di applicazioni in esecuzione in WOW64 in due modi:</span><span class="sxs-lookup"><span data-stu-id="02e5a-106">Applications running under WOW64 can be debugged two ways:</span></span>

-   <span data-ttu-id="02e5a-107">Usare un debugger ospitato da x86, ad esempio NTSD, WinDbg o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="02e5a-107">Use an x86-hosted debugger such as NTSD, WinDbg, or Visual Studio.</span></span> <span data-ttu-id="02e5a-108">Il NTSD a 32 bit è installato in% SystemRoot% \\ SysWow64 nelle installazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="02e5a-108">The 32-bit NTSD is installed to %systemroot%\\syswow64 on retail installations.</span></span> <span data-ttu-id="02e5a-109">Si noti che i debugger x86 possono essere usati per eseguire il debug del codice x86, ma non possono essere usati per disassemblare o impostare punti di interruzione all'interno del livello di thunk WOW64 perché si tratta di codice nativo a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="02e5a-109">Note that x86 debuggers can be used to debug x86 code, but cannot be used to disassemble or set breakpoints within the WOW64 thunk layer because it is 64-bit native code.</span></span>
-   <span data-ttu-id="02e5a-110">Usare un debugger nativo, ad esempio CDB, NTSD o WinDbg e l'estensione del debugger WOW64, Wow64exts.dll.</span><span class="sxs-lookup"><span data-stu-id="02e5a-110">Use a native debugger such as CDB, NTSD, or WinDbg and the WOW64 debugger extension, Wow64exts.dll.</span></span> <span data-ttu-id="02e5a-111">Se il debugger nativo si interrompe mentre il processore è in modalità x86, il processo viene presentato come processo x86.</span><span class="sxs-lookup"><span data-stu-id="02e5a-111">If the native debugger breaks while the processor is in x86 mode, the debugger presents the process as an x86 process.</span></span> <span data-ttu-id="02e5a-112">Se il processore è in modalità nativa, il debugger Visualizza il processo come nativo.</span><span class="sxs-lookup"><span data-stu-id="02e5a-112">If the processor is in native mode, the debugger presents the process as native.</span></span>

<span data-ttu-id="02e5a-113">CDB, NTSD e WinDbg sono inclusi negli strumenti di debug per Windows.</span><span class="sxs-lookup"><span data-stu-id="02e5a-113">CDB, NTSD, and WinDbg are included in Debugging Tools for Windows.</span></span> <span data-ttu-id="02e5a-114">Per ulteriori informazioni, vedere la documentazione relativa agli [strumenti di debug per Windows](/windows-hardware/drivers/debugger/) .</span><span class="sxs-lookup"><span data-stu-id="02e5a-114">For more information, see the [Debugging Tools for Windows](/windows-hardware/drivers/debugger/) documentation.</span></span>

<span data-ttu-id="02e5a-115">L'estensione del debugger Wow64exts viene installata con WinDbg.</span><span class="sxs-lookup"><span data-stu-id="02e5a-115">The Wow64exts debugger extension is installed with WinDbg.</span></span> <span data-ttu-id="02e5a-116">Usare il comando! Load wow64exts per caricare l'estensione del debugger.</span><span class="sxs-lookup"><span data-stu-id="02e5a-116">Use the !load wow64exts command to load the debugger extension.</span></span> <span data-ttu-id="02e5a-117">La tabella seguente elenca i comandi dell'estensione del debugger wow64exts.</span><span class="sxs-lookup"><span data-stu-id="02e5a-117">The following table lists the !wow64exts debugger extension commands.</span></span>



| <span data-ttu-id="02e5a-118">Comando</span><span class="sxs-lookup"><span data-stu-id="02e5a-118">Command</span></span>                | <span data-ttu-id="02e5a-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02e5a-119">Description</span></span>                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e5a-120">! wow64exts. SW</span><span class="sxs-lookup"><span data-stu-id="02e5a-120">!wow64exts.sw</span></span>          | <span data-ttu-id="02e5a-121">Passa dalla modalità x86 alla modalità nativa.</span><span class="sxs-lookup"><span data-stu-id="02e5a-121">Switches between x86 and native mode.</span></span>                                                                                                    |
| <span data-ttu-id="02e5a-122">! wow64exts. k *conteggio*</span><span class="sxs-lookup"><span data-stu-id="02e5a-122">!wow64exts.k *count*</span></span>   | <span data-ttu-id="02e5a-123">Dump di un'analisi dello stack a 32 bit/64 bit combinata.</span><span class="sxs-lookup"><span data-stu-id="02e5a-123">Dumps a combined 32-bit/64-bit stack trace.</span></span> <span data-ttu-id="02e5a-124">Se *count* viene specificato, il comando eseguirà il dump dei primi indirizzi di *conteggio* in ogni traccia dello stack.</span><span class="sxs-lookup"><span data-stu-id="02e5a-124">If *count* is specified, the command dumps the first *count* addresses in each stack trace.</span></span>  |
| <span data-ttu-id="02e5a-125">! wow64exts.info</span><span class="sxs-lookup"><span data-stu-id="02e5a-125">!wow64exts.info</span></span>        | <span data-ttu-id="02e5a-126">Effettua il dump delle informazioni di base sul PEB del processo, sulla TEB del thread corrente e sugli slot di archiviazione locale di thread (TLS) usati da WOW64.</span><span class="sxs-lookup"><span data-stu-id="02e5a-126">Dumps basic information about the PEB of the process, the TEB of the current thread, and thread local storage (TLS) slots used by WOW64.</span></span> |
| <span data-ttu-id="02e5a-127">! wow64exts. r *Indirizzo*</span><span class="sxs-lookup"><span data-stu-id="02e5a-127">!wow64exts.r *address*</span></span> | <span data-ttu-id="02e5a-128">Dump del contesto per l'indirizzo specificato.</span><span class="sxs-lookup"><span data-stu-id="02e5a-128">Dumps context for the specified address.</span></span> <span data-ttu-id="02e5a-129">Se *Address* non è specificato, il comando dump il contesto per il processore.</span><span class="sxs-lookup"><span data-stu-id="02e5a-129">If *address* is not specified, the command dumps context for the processor.</span></span>                     |



 

 

 