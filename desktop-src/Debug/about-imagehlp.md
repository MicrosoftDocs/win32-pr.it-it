---
description: Le funzioni ImageHlp sono utilizzate principalmente da strumenti di programmazione, utilità di installazione dell'applicazione e altri programmi che richiedono l'accesso ai dati contenuti in un'immagine PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Informazioni su ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304570"
---
# <a name="about-imagehlp"></a><span data-ttu-id="be854-103">Informazioni su ImageHlp</span><span class="sxs-lookup"><span data-stu-id="be854-103">About ImageHlp</span></span>

<span data-ttu-id="be854-104">Le funzioni ImageHlp sono utilizzate principalmente da strumenti di programmazione, utilità di installazione dell'applicazione e altri programmi che richiedono l'accesso ai dati contenuti in un'immagine PE.</span><span class="sxs-lookup"><span data-stu-id="be854-104">The ImageHlp functions are used mostly by programming tools, application setup utilities, and other programs that need access to the data contained in a PE image.</span></span> <span data-ttu-id="be854-105">Tutte le funzioni ImageHlp sono a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="be854-105">All ImageHlp functions are single threaded.</span></span> <span data-ttu-id="be854-106">Pertanto, le chiamate da più thread a questa funzione potrebbero causare un comportamento imprevisto o un danneggiamento della memoria.</span><span class="sxs-lookup"><span data-stu-id="be854-106">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="be854-107">Per evitare questo problema, è necessario sincronizzare tutte le chiamate simultanee da più di un thread a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="be854-107">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

<span data-ttu-id="be854-108">Negli argomenti seguenti vengono descritte le immagini PE e la funzionalità fornita dalle funzioni ImageHlp.</span><span class="sxs-lookup"><span data-stu-id="be854-108">The following topics describe PE images and the functionality provided by the ImageHlp functions.</span></span>

-   [<span data-ttu-id="be854-109">Formato PE</span><span class="sxs-lookup"><span data-stu-id="be854-109">PE Format</span></span>](pe-format.md)
-   [<span data-ttu-id="be854-110">Funzioni di accesso alle immagini</span><span class="sxs-lookup"><span data-stu-id="be854-110">Image Access Functions</span></span>](image-access-functions.md)
-   [<span data-ttu-id="be854-111">Funzioni di integrità immagini</span><span class="sxs-lookup"><span data-stu-id="be854-111">Image Integrity Functions</span></span>](image-integrity-functions.md)
-   [<span data-ttu-id="be854-112">Funzioni di modifica delle immagini</span><span class="sxs-lookup"><span data-stu-id="be854-112">Image Modification Functions</span></span>](image-modification-functions.md)

 

 



