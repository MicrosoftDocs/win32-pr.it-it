---
description: I meccanismi strutturati di gestione delle eccezioni e di gestione delle terminazioni sono parti integrali del sistema; consentono al sistema di essere affidabile. È possibile usare questi meccanismi per creare applicazioni solide e affidabili.
ms.assetid: ab5bc1bd-107f-4ed2-b471-a229a76637fe
title: Informazioni sulla gestione delle eccezioni strutturata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161e60725f137f379b7d734485fae7cad39ae1be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225567"
---
# <a name="about-structured-exception-handling"></a><span data-ttu-id="10be9-104">Informazioni sulla gestione delle eccezioni strutturata</span><span class="sxs-lookup"><span data-stu-id="10be9-104">About Structured Exception Handling</span></span>

<span data-ttu-id="10be9-105">I meccanismi strutturati di gestione delle eccezioni e di gestione delle terminazioni sono parti integrali del sistema; consentono al sistema di essere affidabile.</span><span class="sxs-lookup"><span data-stu-id="10be9-105">The structured exception handling and termination handling mechanisms are integral parts of the system; they enable the system to be robust.</span></span> <span data-ttu-id="10be9-106">È possibile usare questi meccanismi per creare applicazioni solide e affidabili.</span><span class="sxs-lookup"><span data-stu-id="10be9-106">You can use these mechanisms to create consistently robust and reliable applications.</span></span>

<span data-ttu-id="10be9-107">La gestione strutturata delle eccezioni viene resa disponibile principalmente tramite il supporto del compilatore.</span><span class="sxs-lookup"><span data-stu-id="10be9-107">Structured exception handling is made available primarily through compiler support.</span></span> <span data-ttu-id="10be9-108">Ad esempio, il compilatore di ottimizzazione di Microsoft C/C++ supporta la parola chiave **\_ \_ try** che identifica un corpo sorvegliato di codice, la parola chiave **\_ \_ except** che identifica un gestore di eccezioni e la parola chiave **\_ \_ finally** che identifica un gestore di terminazione.</span><span class="sxs-lookup"><span data-stu-id="10be9-108">For example, the Microsoft C/C++ Optimizing Compiler supports the **\_\_try** keyword that identifies a guarded body of code, the **\_\_except** keyword that identifies an exception handler, and the **\_\_finally** keyword that identifies a termination handler.</span></span> <span data-ttu-id="10be9-109">Anche se questa panoramica usa esempi specifici del compilatore Microsoft C/C++, altri compilatori forniscono anche questo supporto.</span><span class="sxs-lookup"><span data-stu-id="10be9-109">Although this overview uses examples specific to the Microsoft C/C++ compiler, other compilers provide this support as well.</span></span>

-   [<span data-ttu-id="10be9-110">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="10be9-110">Exception Handling</span></span>](exception-handling.md)
-   [<span data-ttu-id="10be9-111">Gestione delle eccezioni basata su frame</span><span class="sxs-lookup"><span data-stu-id="10be9-111">Frame-based Exception Handling</span></span>](frame-based-exception-handling.md)
-   [<span data-ttu-id="10be9-112">Gestione delle eccezioni con vettori</span><span class="sxs-lookup"><span data-stu-id="10be9-112">Vectored Exception Handling</span></span>](vectored-exception-handling.md)
-   [<span data-ttu-id="10be9-113">Gestione della terminazione</span><span class="sxs-lookup"><span data-stu-id="10be9-113">Termination Handling</span></span>](termination-handling.md)
-   [<span data-ttu-id="10be9-114">Sintassi del gestore</span><span class="sxs-lookup"><span data-stu-id="10be9-114">Handler Syntax</span></span>](handler-syntax.md)

 

 



