---
description: Quando il sistema avvia un programma che usa il collegamento dinamico in fase di caricamento, USA le informazioni inserite dal linker nel file per individuare i nomi delle DLL utilizzate dal processo.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Collegamento dinamico Load-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530013"
---
# <a name="load-time-dynamic-linking"></a><span data-ttu-id="340b3-103">Collegamento dinamico Load-Time</span><span class="sxs-lookup"><span data-stu-id="340b3-103">Load-Time Dynamic Linking</span></span>

<span data-ttu-id="340b3-104">Quando il sistema avvia un programma che usa il collegamento dinamico in fase di caricamento, USA le informazioni inserite dal linker nel file per individuare i nomi delle DLL utilizzate dal processo.</span><span class="sxs-lookup"><span data-stu-id="340b3-104">When the system starts a program that uses load-time dynamic linking, it uses the information the linker placed in the file to locate the names of the DLLs that are used by the process.</span></span> <span data-ttu-id="340b3-105">Il sistema cerca quindi le dll.</span><span class="sxs-lookup"><span data-stu-id="340b3-105">The system then searches for the DLLs.</span></span> <span data-ttu-id="340b3-106">Per ulteriori informazioni, vedere l' [ordine di ricerca della libreria a collegamento dinamico](dynamic-link-library-search-order.md).</span><span class="sxs-lookup"><span data-stu-id="340b3-106">For more information, see [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).</span></span>

<span data-ttu-id="340b3-107">Se il sistema non è in grado di individuare una DLL obbligatoria, termina il processo e visualizza una finestra di dialogo che segnala l'errore all'utente.</span><span class="sxs-lookup"><span data-stu-id="340b3-107">If the system cannot locate a required DLL, it terminates the process and displays a dialog box that reports the error to the user.</span></span> <span data-ttu-id="340b3-108">In caso contrario, il sistema esegue il mapping della DLL allo spazio degli indirizzi virtuali del processo e incrementa il conteggio dei riferimenti alla DLL.</span><span class="sxs-lookup"><span data-stu-id="340b3-108">Otherwise, the system maps the DLL into the virtual address space of the process and increments the DLL reference count.</span></span>

<span data-ttu-id="340b3-109">Il sistema chiama la funzione del punto di ingresso.</span><span class="sxs-lookup"><span data-stu-id="340b3-109">The system calls the entry-point function.</span></span> <span data-ttu-id="340b3-110">La funzione riceve un codice che indica che il processo sta caricando la DLL.</span><span class="sxs-lookup"><span data-stu-id="340b3-110">The function receives a code indicating that the process is loading the DLL.</span></span> <span data-ttu-id="340b3-111">Se la funzione del punto di ingresso non restituisce TRUE, il sistema termina il processo e segnala l'errore.</span><span class="sxs-lookup"><span data-stu-id="340b3-111">If the entry-point function does not return TRUE, the system terminates the process and reports the error.</span></span> <span data-ttu-id="340b3-112">Per ulteriori informazioni sulla funzione del punto di ingresso, vedere [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="340b3-112">For more information about the entry-point function, see [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).</span></span>

<span data-ttu-id="340b3-113">Infine, il sistema modifica la tabella degli indirizzi di funzione con gli indirizzi iniziali per le funzioni DLL importate.</span><span class="sxs-lookup"><span data-stu-id="340b3-113">Finally, the system modifies the function address table with the starting addresses for the imported DLL functions.</span></span>

<span data-ttu-id="340b3-114">La DLL viene mappata allo spazio degli indirizzi virtuali del processo durante l'inizializzazione e viene caricata nella memoria fisica solo quando necessario.</span><span class="sxs-lookup"><span data-stu-id="340b3-114">The DLL is mapped into the virtual address space of the process during its initialization and is loaded into physical memory only when needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="340b3-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="340b3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="340b3-116">Uso di Load-Time collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="340b3-116">Using Load-Time Dynamic Linking</span></span>](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



