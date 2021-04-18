---
description: Quando si crea un processo con la funzione CreateProcess, è possibile specificare che il processo erediti gli handle per gli oggetti mutex, Event, Semaphore o timer usando la \_ struttura degli attributi di sicurezza.
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Ereditarietà degli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6087ae3699e7628ab97871ede41cc2e406e40157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314645"
---
# <a name="object-inheritance"></a><span data-ttu-id="c8f46-103">Ereditarietà degli oggetti</span><span class="sxs-lookup"><span data-stu-id="c8f46-103">Object Inheritance</span></span>

<span data-ttu-id="c8f46-104">Quando si crea un processo con la funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , è possibile specificare che il processo erediti gli handle per gli oggetti mutex, Event, Semaphore o timer usando la struttura degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c8f46-104">When you create a process with the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, you can specify that the process inherit handles to mutex, event, semaphore, or timer objects using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="c8f46-105">L'handle ereditato dal processo ha lo stesso accesso all'oggetto come handle originale.</span><span class="sxs-lookup"><span data-stu-id="c8f46-105">The handle inherited by the process has the same access to the object as the original handle.</span></span> <span data-ttu-id="c8f46-106">L'handle ereditato viene visualizzato nella tabella di handle del processo creato, ma è necessario comunicare il valore dell'handle al processo creato.</span><span class="sxs-lookup"><span data-stu-id="c8f46-106">The inherited handle appears in the handle table of the created process, but you must communicate the handle value to the created process.</span></span> <span data-ttu-id="c8f46-107">È possibile eseguire questa operazione specificando il valore come argomento della riga di comando quando si chiama **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="c8f46-107">You can do this by specifying the value as a command-line argument when you call **CreateProcess**.</span></span> <span data-ttu-id="c8f46-108">Il processo creato usa quindi la funzione [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) per recuperare la stringa della riga di comando e convertire l'argomento handle in un handle utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="c8f46-108">The created process then uses the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function to retrieve the command-line string and convert the handle argument into a usable handle.</span></span> <span data-ttu-id="c8f46-109">Per altre informazioni, vedere [Ereditarietà](../procthread/inheritance.md).</span><span class="sxs-lookup"><span data-stu-id="c8f46-109">For more information, see [Inheritance](../procthread/inheritance.md).</span></span>

 

 
