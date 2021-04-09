---
title: Più controlli in una DLL
description: Più controlli in una DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044146"
---
# <a name="multiple-controls-in-one-dll"></a><span data-ttu-id="af775-103">Più controlli in una DLL</span><span class="sxs-lookup"><span data-stu-id="af775-103">Multiple Controls in One DLL</span></span>

<span data-ttu-id="af775-104">Una singola DLL OCX può comportare un numero qualsiasi di controlli ActiveX, semplificando in tal modo la distribuzione e l'utilizzo di un set di controlli correlati.</span><span class="sxs-lookup"><span data-stu-id="af775-104">A single .ocx DLL can container any number of ActiveX controls, thus simplifying the distribution and use of a set of related controls.</span></span>

<span data-ttu-id="af775-105">Se si distribuiscono più controlli in una singola DLL, assicurarsi di includere il nome del fornitore in ogni nome di controllo nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="af775-105">If you ship multiple controls in a single DLL, be sure to include the vendor name in each control name in the package.</span></span> <span data-ttu-id="af775-106">L'inclusione dei nomi dei fornitori in ogni nome di controllo consentirà agli utenti di identificare facilmente i controlli all'interno di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="af775-106">Including the vendors' names in each control name will enable users to easily identify controls within a package.</span></span> <span data-ttu-id="af775-107">Se, ad esempio, si invia una DLL che implementa tre controlli, con1, CON2 e con3, i nomi dei controlli devono essere:</span><span class="sxs-lookup"><span data-stu-id="af775-107">For example, if you ship a DLL that implements three controls, Con1, Con2, and Con3, then the control names should be:</span></span>

-   <span data-ttu-id="af775-108">*Nome della società* Controllo con1</span><span class="sxs-lookup"><span data-stu-id="af775-108">*Your company name* Con1 Control</span></span>

-   <span data-ttu-id="af775-109">*Nome della società* Controllo con2</span><span class="sxs-lookup"><span data-stu-id="af775-109">*Your company name* Con2 Control</span></span>

-   <span data-ttu-id="af775-110">*Nome della società* Controllo con3</span><span class="sxs-lookup"><span data-stu-id="af775-110">*Your company name* Con3 Control</span></span>

 

 




