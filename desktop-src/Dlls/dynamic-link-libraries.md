---
description: Una libreria di collegamento dinamico (DLL) è un modulo che contiene funzioni e dati che possono essere usati da un altro modulo (applicazione o DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Librerie di Dynamic-Link (librerie a collegamento dinamico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753783"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a><span data-ttu-id="ddbe2-103">Librerie di Dynamic-Link (librerie a collegamento dinamico)</span><span class="sxs-lookup"><span data-stu-id="ddbe2-103">Dynamic-Link Libraries (Dynamic-Link Libraries)</span></span>

<span data-ttu-id="ddbe2-104">Una *libreria di collegamento dinamico* (dll) è un modulo che contiene funzioni e dati che possono essere usati da un altro modulo (applicazione o dll).</span><span class="sxs-lookup"><span data-stu-id="ddbe2-104">A *dynamic-link library* (DLL) is a module that contains functions and data that can be used by another module (application or DLL).</span></span>

<span data-ttu-id="ddbe2-105">Una DLL può definire due tipi di funzioni: esportate e interne.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-105">A DLL can define two kinds of functions: exported and internal.</span></span> <span data-ttu-id="ddbe2-106">Le funzioni esportate sono progettate per essere chiamate da altri moduli, nonché dall'interno della DLL in cui sono definite.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-106">The exported functions are intended to be called by other modules, as well as from within the DLL where they are defined.</span></span> <span data-ttu-id="ddbe2-107">Le funzioni interne sono in genere destinate a essere chiamate solo dall'interno della DLL in cui sono definite.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-107">Internal functions are typically intended to be called only from within the DLL where they are defined.</span></span> <span data-ttu-id="ddbe2-108">Sebbene una DLL possa esportare dati, i relativi dati vengono in genere utilizzati solo dalle relative funzioni.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-108">Although a DLL can export data, its data is generally used only by its functions.</span></span> <span data-ttu-id="ddbe2-109">Tuttavia, non c'è nulla da impedire a un altro modulo di leggere o scrivere tale indirizzo.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-109">However, there is nothing to prevent another module from reading or writing that address.</span></span>

<span data-ttu-id="ddbe2-110">Le DLL consentono di modularizzare le applicazioni in modo che le relative funzionalità possano essere aggiornate e riutilizzate più facilmente.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-110">DLLs provide a way to modularize applications so that their functionality can be updated and reused more easily.</span></span> <span data-ttu-id="ddbe2-111">Le DLL consentono inoltre di ridurre il sovraccarico della memoria quando più applicazioni utilizzano la stessa funzionalità allo stesso tempo, perché anche se ogni applicazione riceve una copia dei dati DLL, le applicazioni condividono il codice DLL.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-111">DLLs also help reduce memory overhead when several applications use the same functionality at the same time, because although each application receives its own copy of the DLL data, the applications share the DLL code.</span></span>

<span data-ttu-id="ddbe2-112">Windows Application Programming Interface (API) viene implementato come un set di dll, pertanto qualsiasi processo che utilizza l'API Windows utilizza il collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-112">The Windows application programming interface (API) is implemented as a set of DLLs, so any process that uses the Windows API uses dynamic linking.</span></span>

-   [<span data-ttu-id="ddbe2-113">Informazioni sulle librerie Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="ddbe2-113">About Dynamic-Link Libraries</span></span>](about-dynamic-link-libraries.md)
-   [<span data-ttu-id="ddbe2-114">Uso di librerie Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="ddbe2-114">Using Dynamic-Link Libraries</span></span>](using-dynamic-link-libraries.md)
-   [<span data-ttu-id="ddbe2-115">Riferimenti alla libreria a collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="ddbe2-115">Dynamic-Link Library Reference</span></span>](dynamic-link-library-reference.md)

> [!Note]  
> <span data-ttu-id="ddbe2-116">Se si riscontrano problemi con una DLL nel computer, è necessario contattare il supporto tecnico per il fornitore del software che pubblica la DLL.</span><span class="sxs-lookup"><span data-stu-id="ddbe2-116">If you are a user experiencing difficulty with a DLL on your computer, you should contact customer support for the software vendor that publishes the DLL.</span></span> <span data-ttu-id="ddbe2-117">Se si ritiene che sia necessario il supporto per un prodotto Microsoft (incluso Windows), visitare il sito del supporto tecnico all'indirizzo [support.Microsoft.com](https://support.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ddbe2-117">If you feel you are in need of support for a Microsoft product (including Windows), please go to our technical support site at [support.microsoft.com](https://support.microsoft.com).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ddbe2-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ddbe2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddbe2-119">Dll (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="ddbe2-119">DLLs (Visual C++)</span></span>](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
