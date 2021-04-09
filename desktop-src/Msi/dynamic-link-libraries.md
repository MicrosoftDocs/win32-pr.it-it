---
description: Un'azione personalizzata può chiamare una funzione definita in una libreria a collegamento dinamico (DLL) scritta in C o C++.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Librerie di Dynamic-Link (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050147"
---
# <a name="dynamic-link-libraries-windows-installer"></a><span data-ttu-id="63cc0-103">Librerie di Dynamic-Link (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="63cc0-103">Dynamic-Link Libraries (Windows Installer)</span></span>

<span data-ttu-id="63cc0-104">Un'azione personalizzata può chiamare una funzione definita in una libreria a collegamento dinamico (DLL) scritta in C o C++.</span><span class="sxs-lookup"><span data-stu-id="63cc0-104">A custom action can call a function defined in a dynamic-link library (DLL) written in C or C++.</span></span> <span data-ttu-id="63cc0-105">La DLL può esistere come file installato durante l'installazione corrente o come flusso binario temporaneo originato dalla [tabella binaria](binary-table.md) del database di installazione.</span><span class="sxs-lookup"><span data-stu-id="63cc0-105">The DLL can exist as a file installed during the current installation or as a temporary binary stream originating from the [Binary table](binary-table.md) of the installation database.</span></span>

<span data-ttu-id="63cc0-106">Si noti che tutte le funzioni chiamate, incluse le azioni personalizzate nelle DLL, devono specificare la \_ \_ convenzione di chiamata stdcall.</span><span class="sxs-lookup"><span data-stu-id="63cc0-106">Note that any called functions, including custom actions in DLLs, must specify the \_\_stdcall calling convention.</span></span> <span data-ttu-id="63cc0-107">Per chiamare CustomAction, ad esempio, usare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="63cc0-107">For example, to call CustomAction use the following.</span></span>


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="63cc0-108">Per altre informazioni, vedere [accesso alla sessione corrente del programma di installazione dall'interno di un'azione personalizzata](accessing-the-current-installer-session-from-inside-a-custom-action.md)</span><span class="sxs-lookup"><span data-stu-id="63cc0-108">For more information see, [Accessing the Current Installer Session from Inside a Custom Action](accessing-the-current-installer-session-from-inside-a-custom-action.md)</span></span>

<span data-ttu-id="63cc0-109">I tipi seguenti di azioni personalizzate chiamano una libreria a collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="63cc0-109">The following types of custom actions call a dynamic-link library.</span></span>



| <span data-ttu-id="63cc0-110">Tipo di azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="63cc0-110">Custom action type</span></span>                                 | <span data-ttu-id="63cc0-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63cc0-111">Description</span></span>                               |
|----------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="63cc0-112">Tipo di azione personalizzata 1</span><span class="sxs-lookup"><span data-stu-id="63cc0-112">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="63cc0-113">File DLL archiviato in un flusso di tabella binario.</span><span class="sxs-lookup"><span data-stu-id="63cc0-113">DLL file stored in a Binary table stream.</span></span> |
| [<span data-ttu-id="63cc0-114">Tipo di azione personalizzata 17</span><span class="sxs-lookup"><span data-stu-id="63cc0-114">Custom Action Type 17</span></span>](custom-action-type-17.md) | <span data-ttu-id="63cc0-115">File DLL installato con un prodotto.</span><span class="sxs-lookup"><span data-stu-id="63cc0-115">DLL file installed with a product.</span></span>        |



 

> [!Note]  
> <span data-ttu-id="63cc0-116">Per usare COM è necessario chiamare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) nell'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="63cc0-116">To use COM you need to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in the custom action.</span></span> <span data-ttu-id="63cc0-117">Non uscire se si rileva che il thread è già stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="63cc0-117">Do not quit if you find that the thread has already been initialized.</span></span> <span data-ttu-id="63cc0-118">Ad esempio, il thread viene inizializzato in un'installazione per computer, ma non in un'installazione per utente.</span><span class="sxs-lookup"><span data-stu-id="63cc0-118">For example, the thread is initialized in a per-machine installation but not in a per-user installation.</span></span>

 

<span data-ttu-id="63cc0-119">Vedere l' [elenco riepilogativo di tutti i tipi di azione personalizzati](summary-list-of-all-custom-action-types.md) per un riepilogo di tutti i tipi di azioni personalizzate e il modo in cui vengono codificati nella [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="63cc0-119">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction table](customaction-table.md).</span></span>

 

 
