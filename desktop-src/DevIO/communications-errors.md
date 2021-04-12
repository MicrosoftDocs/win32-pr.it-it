---
description: In altre circostanze è possibile completare un'operazione di lettura o scrittura con un numero di caratteri inferiore a quello richiesto, anche se non si è verificato un timeout.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Errori di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483285"
---
# <a name="communications-errors"></a><span data-ttu-id="526fa-103">Errori di comunicazione</span><span class="sxs-lookup"><span data-stu-id="526fa-103">Communications Errors</span></span>

<span data-ttu-id="526fa-104">In altre circostanze è possibile completare un'operazione di lettura o scrittura con un numero di caratteri inferiore a quello richiesto, anche se non si è verificato un timeout.</span><span class="sxs-lookup"><span data-stu-id="526fa-104">There are other circumstances where a read or write operation can be completed with fewer than the requested number of characters, even though a time-out has not occurred.</span></span> <span data-ttu-id="526fa-105">Ecco alcuni esempi:</span><span class="sxs-lookup"><span data-stu-id="526fa-105">Following are some examples:</span></span>

-   <span data-ttu-id="526fa-106">Alcuni driver supportano l'uso di caratteri speciali, che completano immediatamente un'operazione di lettura con solo i caratteri che sono stati letti fino al momento in cui vengono ricevuti.</span><span class="sxs-lookup"><span data-stu-id="526fa-106">Some drivers support the use of special characters, which complete a read operation immediately with only the characters that have been read up to the point when they are received.</span></span>
-   <span data-ttu-id="526fa-107">La funzione [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) può essere chiamata per terminare in modo anomalo le operazioni di lettura o scrittura in sospeso.</span><span class="sxs-lookup"><span data-stu-id="526fa-107">The [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) function can be called to prematurely terminate pending read or write operations.</span></span> <span data-ttu-id="526fa-108">Questa funzione può anche eliminare il contenuto dei buffer di output o di input o entrambi.</span><span class="sxs-lookup"><span data-stu-id="526fa-108">This function can also delete the contents of the output or input buffers, or both.</span></span>
-   <span data-ttu-id="526fa-109">Se si verifica un errore di comunicazione durante un'operazione di lettura o scrittura, tutte le operazioni di I/O sulla risorsa di comunicazione vengono terminate.</span><span class="sxs-lookup"><span data-stu-id="526fa-109">If a communications error occurs during a read or write operation, all I/O operations on the communications resource are terminated.</span></span> <span data-ttu-id="526fa-110">Condizioni di interruzioni, errori di parità o errori di framing sono esempi di tali errori.</span><span class="sxs-lookup"><span data-stu-id="526fa-110">Break conditions, parity errors, or framing errors are examples of such errors.</span></span> <span data-ttu-id="526fa-111">Quando si verifica un errore, è necessario che il processo chiami la funzione [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) per cancellare il flag di errore prima di poter avviare ulteriori operazioni di I/O.</span><span class="sxs-lookup"><span data-stu-id="526fa-111">When an error occurs, the process must call the [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) function to clear the error flag before it can begin additional I/O operations.</span></span> <span data-ttu-id="526fa-112">**ClearCommError** segnala l'errore specifico che si è verificato e lo stato corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="526fa-112">**ClearCommError** reports the specific error that occurred and the current status of the device.</span></span>

 

 



