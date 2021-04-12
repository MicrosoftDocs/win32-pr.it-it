---
description: Un nome di simbolo decorato include caratteri che distinguono il modo in cui un simbolo pubblico è stato dichiarato.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Nomi di simboli decorati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791fe2220b24dfb73b314a91d1797edd739cb74f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482732"
---
# <a name="decorated-symbol-names"></a><span data-ttu-id="3a1dd-103">Nomi di simboli decorati</span><span class="sxs-lookup"><span data-stu-id="3a1dd-103">Decorated Symbol Names</span></span>

<span data-ttu-id="3a1dd-104">Un nome di simbolo decorato include caratteri che distinguono il modo in cui un simbolo pubblico è stato dichiarato.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-104">A decorated symbol name includes characters that distinguish how a public symbol has been declared.</span></span> <span data-ttu-id="3a1dd-105">Per le \_ \_ funzioni stdcall, i nomi includono il carattere "@" e un numero decimale che specifica il numero di byte nei parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-105">For \_\_stdcall functions, names include the "@" character and a decimal number that specifies the number of bytes in its function parameters.</span></span> <span data-ttu-id="3a1dd-106">Ad esempio, il nome decorato della funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) è LoadLibrary@4 .</span><span class="sxs-lookup"><span data-stu-id="3a1dd-106">For example, the decorated name of the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is LoadLibrary@4.</span></span> <span data-ttu-id="3a1dd-107">Per le funzioni C++ la decorazione del nome è più complessa e varia da compilatore a compilatore.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-107">For C++ functions the name decoration is more complex and varies from compiler to compiler.</span></span>

<span data-ttu-id="3a1dd-108">Per recuperare il nome del simbolo non decorato, usare la funzione [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) .</span><span class="sxs-lookup"><span data-stu-id="3a1dd-108">To retrieve the undecorated symbol name, use the [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) function.</span></span> <span data-ttu-id="3a1dd-109">In alternativa, è possibile chiamare la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) per richiedere che il gestore di simboli presenti sempre simboli con nomi non decorati.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-109">Alternatively, you can call the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to request that the symbol handler always present symbols with undecorated names.</span></span> <span data-ttu-id="3a1dd-110">È necessario impostare questa opzione prima di caricare i simboli perché il gestore di simboli crea le tabelle dei nomi di simboli in fase di caricamento.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-110">You must set this option before loading the symbols because the symbol handler creates the symbol name tables at load time.</span></span>

 

 
