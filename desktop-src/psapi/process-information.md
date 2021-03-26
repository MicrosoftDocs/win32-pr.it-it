---
title: Informazioni sul processo
description: Il sistema gestisce un elenco di processi in esecuzione. È possibile recuperare gli identificatori per questi processi chiamando la funzione EnumProcesses. Questa funzione riempie una matrice di valori DWORD con gli identificatori di tutti i processi nel sistema.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338031"
---
# <a name="process-information"></a><span data-ttu-id="5aba6-105">Informazioni sul processo</span><span class="sxs-lookup"><span data-stu-id="5aba6-105">Process Information</span></span>

<span data-ttu-id="5aba6-106">Il sistema gestisce un elenco di processi in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5aba6-106">The system maintains a list of running processes.</span></span> <span data-ttu-id="5aba6-107">È possibile recuperare gli identificatori per questi processi chiamando la funzione [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="5aba6-107">You can retrieve the identifiers for these processes by calling the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="5aba6-108">Questa funzione riempie una matrice di valori **DWORD** con gli identificatori di tutti i processi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5aba6-108">This function fills an array of **DWORD** values with the identifiers of all processes in the system.</span></span>

<span data-ttu-id="5aba6-109">Molte funzioni in PSAPI richiedono un handle di processo.</span><span class="sxs-lookup"><span data-stu-id="5aba6-109">Many functions in PSAPI require a process handle.</span></span> <span data-ttu-id="5aba6-110">Per ottenere un handle di processo per un processo in esecuzione, passare il relativo identificatore di processo (ottenuto da [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) alla funzione [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) .</span><span class="sxs-lookup"><span data-stu-id="5aba6-110">To obtain a process handle for a running process, pass its process identifier (obtained from [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) to the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function.</span></span> <span data-ttu-id="5aba6-111">Ricordare di chiamare la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) al termine dell'handle di processo.</span><span class="sxs-lookup"><span data-stu-id="5aba6-111">Remember to call the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function when you are finished with the process handle.</span></span>

 

 