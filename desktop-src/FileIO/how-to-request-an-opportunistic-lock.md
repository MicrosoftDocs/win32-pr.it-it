---
description: I blocchi opportunistici vengono richiesti aprendo prima un file con le autorizzazioni e i flag appropriati all'applicazione per l'apertura del file. Tutti i file per i quali verranno richiesti blocchi opportunistici devono essere aperti per operazioni sovrapposte (asincrone).
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: Come richiedere un blocco opportunistico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884882"
---
# <a name="how-to-request-an-opportunistic-lock"></a><span data-ttu-id="31f15-104">Come richiedere un blocco opportunistico</span><span class="sxs-lookup"><span data-stu-id="31f15-104">How to Request an Opportunistic Lock</span></span>

<span data-ttu-id="31f15-105">Le applicazioni client richiedono direttamente blocchi opportunistici solo quando il blocco è destinato a un file nel server locale.</span><span class="sxs-lookup"><span data-stu-id="31f15-105">Client applications directly request opportunistic locks only when the lock is intended for a file on the local server.</span></span> <span data-ttu-id="31f15-106">Quando si accede a file su server remoti, è il redirector di rete e non l'applicazione client che richiede il blocco opportunistico dal server remoto.</span><span class="sxs-lookup"><span data-stu-id="31f15-106">When accessing files on remote servers, it is the network redirector, and not the client application, that requests the opportunistic lock from the remote server.</span></span>

<span data-ttu-id="31f15-107">I blocchi opportunistici vengono richiesti aprendo prima un file con le autorizzazioni e i flag appropriati all'applicazione per l'apertura del file.</span><span class="sxs-lookup"><span data-stu-id="31f15-107">Opportunistic locks are requested by first opening a file with permissions and flags appropriate to the application opening the file.</span></span> <span data-ttu-id="31f15-108">Tutti i file per i quali verranno richiesti blocchi opportunistici devono essere aperti per operazioni sovrapposte (asincrone).</span><span class="sxs-lookup"><span data-stu-id="31f15-108">All files for which opportunistic locks will be requested must be opened for overlapped (asynchronous) operation.</span></span> <span data-ttu-id="31f15-109">Dopo l'apertura dei file per un'operazione sovrapposta, utilizzare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con il codice di controllo appropriato per richiedere un blocco opportunistico.</span><span class="sxs-lookup"><span data-stu-id="31f15-109">After the files are opened for overlapped operation, use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the appropriate control code to request an opportunistic lock.</span></span> <span data-ttu-id="31f15-110">Per un elenco delle operazioni di blocco opportunistiche, vedere [operazioni di blocco opportunistiche](opportunistic-lock-operations.md).</span><span class="sxs-lookup"><span data-stu-id="31f15-110">For a list of the opportunistic lock operations, see [Opportunistic Lock Operations](opportunistic-lock-operations.md).</span></span>

<span data-ttu-id="31f15-111">Alle applicazioni viene notificato che un blocco opportunistico viene rotto utilizzando il membro **hEvent** della struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associata al file.</span><span class="sxs-lookup"><span data-stu-id="31f15-111">Applications are notified that an opportunistic lock is broken by using the **hEvent** member of the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the file.</span></span> <span data-ttu-id="31f15-112">Le applicazioni possono anche usare funzioni quali [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) e [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span><span class="sxs-lookup"><span data-stu-id="31f15-112">Applications may also use functions such as [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) and [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span></span> <span data-ttu-id="31f15-113">L'applicazione è responsabile dell'associazione del file corretto al blocco opportunistico rotto.</span><span class="sxs-lookup"><span data-stu-id="31f15-113">The application is responsible for associating the correct file with the broken opportunistic lock.</span></span>

<span data-ttu-id="31f15-114">Per ulteriori informazioni sulla notifica, vedere [sincronizzazione](/windows/desktop/Sync/synchronization).</span><span class="sxs-lookup"><span data-stu-id="31f15-114">For more information on notification, see [Synchronization](/windows/desktop/Sync/synchronization).</span></span>

 

 
