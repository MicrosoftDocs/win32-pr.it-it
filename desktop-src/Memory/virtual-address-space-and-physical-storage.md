---
description: La quantità massima di memoria fisica supportata da Microsoft Windows varia da 2 GB a 2 TB, a seconda della versione di Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Spazio degli indirizzi virtuali e archiviazione fisica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d36445eb2639cbfc4db2a6e4abaf28b9af87cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528890"
---
# <a name="virtual-address-space-and-physical-storage"></a><span data-ttu-id="88071-103">Spazio degli indirizzi virtuali e archiviazione fisica</span><span class="sxs-lookup"><span data-stu-id="88071-103">Virtual Address Space and Physical Storage</span></span>

<span data-ttu-id="88071-104">La quantità massima di memoria fisica supportata da Microsoft Windows varia da 2 GB a 24 TB, a seconda della versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="88071-104">The maximum amount of physical memory supported by Microsoft Windows ranges from 2 GB to 24 TB, depending on the version of Windows.</span></span> <span data-ttu-id="88071-105">Per ulteriori informazioni, vedere [limiti di memoria per le versioni di Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="88071-105">For more information, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span> <span data-ttu-id="88071-106">Lo spazio degli indirizzi virtuali di ogni processo può essere minore o maggiore della memoria fisica totale disponibile nel computer.</span><span class="sxs-lookup"><span data-stu-id="88071-106">The virtual address space of each process can be smaller or larger than the total physical memory available on the computer.</span></span> <span data-ttu-id="88071-107">Il subset dello spazio degli indirizzi virtuali di un processo che risiede nella memoria fisica è noto come *working set*.</span><span class="sxs-lookup"><span data-stu-id="88071-107">The subset of the virtual address space of a process that resides in physical memory is known as the *working set*.</span></span> <span data-ttu-id="88071-108">Se i thread di un processo tentano di utilizzare una quantità di memoria fisica superiore a quella attualmente disponibile, il sistema pagine parte del contenuto della memoria su disco.</span><span class="sxs-lookup"><span data-stu-id="88071-108">If the threads of a process attempt to use more physical memory than is currently available, the system pages some of the memory contents to disk.</span></span> <span data-ttu-id="88071-109">La quantità totale di spazio degli indirizzi virtuali disponibile per un processo è limitata dalla memoria fisica e dallo spazio libero su disco disponibile per il file di paging.</span><span class="sxs-lookup"><span data-stu-id="88071-109">The total amount of virtual address space available to a process is limited by physical memory and the free space on disk available for the paging file.</span></span>

<span data-ttu-id="88071-110">L'archiviazione fisica e lo spazio degli indirizzi virtuali di ogni processo sono organizzati in *pagine*, unità di memoria le cui dimensioni dipendono dal computer host.</span><span class="sxs-lookup"><span data-stu-id="88071-110">Physical storage and the virtual address space of each process are organized into *pages*, units of memory, whose size depends on the host computer.</span></span> <span data-ttu-id="88071-111">Ad esempio, nei computer x86 la dimensione della pagina host è 4 kilobyte.</span><span class="sxs-lookup"><span data-stu-id="88071-111">For example, on x86 computers the host page size is 4 kilobytes.</span></span>

<span data-ttu-id="88071-112">Per massimizzare la flessibilità nella gestione della memoria, il sistema può spostare le pagine della memoria fisica da e verso un file di paging su disco.</span><span class="sxs-lookup"><span data-stu-id="88071-112">To maximize its flexibility in managing memory, the system can move pages of physical memory to and from a paging file on disk.</span></span> <span data-ttu-id="88071-113">Quando una pagina viene spostata nella memoria fisica, il sistema aggiorna le mappe della pagina dei processi interessati.</span><span class="sxs-lookup"><span data-stu-id="88071-113">When a page is moved in physical memory, the system updates the page maps of the affected processes.</span></span> <span data-ttu-id="88071-114">Quando il sistema richiede spazio nella memoria fisica, sposta le pagine utilizzate meno di recente nella memoria fisica nel file di paging.</span><span class="sxs-lookup"><span data-stu-id="88071-114">When the system needs space in physical memory, it moves the least recently used pages of physical memory to the paging file.</span></span> <span data-ttu-id="88071-115">La manipolazione della memoria fisica da parte del sistema è completamente trasparente per le applicazioni, che funzionano solo negli spazi degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="88071-115">Manipulation of physical memory by the system is completely transparent to applications, which operate only in their virtual address spaces.</span></span>

 

 



