---
title: Esplorazione del modulo
description: Uno snapshot che include l'elenco dei moduli per un processo specificato contiene informazioni su ogni modulo, file eseguibile o libreria a collegamento dinamico (DLL), utilizzato dal processo specificato.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- librerie a collegamento dinamico
- librerie a collegamento dinamico, enumerazione di dll
- enumerazione
- Enumerazione, dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117863"
---
# <a name="module-walking"></a><span data-ttu-id="8a03b-107">Esplorazione del modulo</span><span class="sxs-lookup"><span data-stu-id="8a03b-107">Module Walking</span></span>

<span data-ttu-id="8a03b-108">Uno snapshot che include l'elenco dei moduli per un processo specificato contiene informazioni su ogni modulo, file eseguibile o libreria a collegamento dinamico (DLL), utilizzato dal processo specificato.</span><span class="sxs-lookup"><span data-stu-id="8a03b-108">A snapshot that includes the module list for a specified process contains information about each module, executable file, or dynamic-link library (DLL), used by the specified process.</span></span> <span data-ttu-id="8a03b-109">È possibile recuperare le informazioni per il primo modulo nell'elenco usando la funzione [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) .</span><span class="sxs-lookup"><span data-stu-id="8a03b-109">You can retrieve information for the first module in the list by using the [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) function.</span></span> <span data-ttu-id="8a03b-110">Dopo aver recuperato il primo modulo nell'elenco, è possibile recuperare le informazioni per i moduli successivi nell'elenco usando la funzione [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) .</span><span class="sxs-lookup"><span data-stu-id="8a03b-110">After retrieving the first module in the list, you can retrieve information for subsequent modules in the list by using the [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) function.</span></span> <span data-ttu-id="8a03b-111">**Module32First** e **Module32Next** riempiono una struttura [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) con informazioni sul modulo.</span><span class="sxs-lookup"><span data-stu-id="8a03b-111">**Module32First** and **Module32Next** fill a [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) structure with information about the module.</span></span>

<span data-ttu-id="8a03b-112">È possibile recuperare un codice di stato di errore esteso per [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) e [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) utilizzando la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="8a03b-112">You can retrieve an extended error status code for [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) and [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="8a03b-113">L'identificatore del modulo, specificato nel membro **th32ModuleID** di [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), ha significato solo in Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="8a03b-113">The module identifier, which is specified in the **th32ModuleID** member of [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), only has meaning in 16-bit Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8a03b-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a03b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a03b-115">Attraversamento dell'elenco dei moduli</span><span class="sxs-lookup"><span data-stu-id="8a03b-115">Traversing the Module List</span></span>](traversing-the-module-list.md)
</dt> </dl>

 

 