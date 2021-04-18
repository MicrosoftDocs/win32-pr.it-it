---
description: Le applicazioni possono utilizzare in modo sicuro le funzionalità di gestione della memoria della libreria di runtime C (malloc, free e così via) e C++ (nuovo, DELETE e così via).
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Funzioni della libreria C standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308334"
---
# <a name="standard-c-library-functions"></a><span data-ttu-id="ca3fe-103">Funzioni della libreria C standard</span><span class="sxs-lookup"><span data-stu-id="ca3fe-103">Standard C Library Functions</span></span>

<span data-ttu-id="ca3fe-104">Le applicazioni possono utilizzare in modo sicuro le funzionalità di gestione della memoria della libreria di runtime C (**malloc**, **Free** e così via) e C++ (**nuovo**, **Delete** e così via).</span><span class="sxs-lookup"><span data-stu-id="ca3fe-104">Applications can safely use the memory management features of the C run-time library (**malloc**, **free**, and so on) and C++ (**new**, **delete**, and so on).</span></span> <span data-ttu-id="ca3fe-105">Le funzioni della libreria di runtime C non presentano i potenziali problemi in Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="ca3fe-105">The C run-time library functions do not have the potential problems they have under 16-bit Windows.</span></span> <span data-ttu-id="ca3fe-106">La gestione della memoria non è più un problema perché il sistema è libero di gestire la memoria spostando le pagine della memoria fisica senza influire sugli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="ca3fe-106">Memory management is no longer a problem because the system is free to manage memory by moving pages of physical memory without affecting the virtual addresses.</span></span> <span data-ttu-id="ca3fe-107">Analogamente, la distinzione tra i puntatori near e lontano non è più pertinente.</span><span class="sxs-lookup"><span data-stu-id="ca3fe-107">Similarly, the distinction between near and far pointers is no longer relevant.</span></span> <span data-ttu-id="ca3fe-108">Pertanto, è possibile utilizzare le funzioni della libreria C standard per la gestione della memoria.</span><span class="sxs-lookup"><span data-stu-id="ca3fe-108">Therefore, you can use the standard C library functions for memory management.</span></span> <span data-ttu-id="ca3fe-109">Tuttavia, le funzioni di gestione della memoria forniscono funzionalità non disponibili nella libreria di runtime del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="ca3fe-109">However, the memory management functions do provide functionality that is unavailable in the C run-time library.</span></span>

 

 



