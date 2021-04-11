---
description: .
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Nuovi file binari di Low-Level
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b6e197f22df9fb3d6e12aeeff3c5f4a2a0e41c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232916"
---
# <a name="new-low-level-binaries"></a><span data-ttu-id="85b9b-103">Nuovi file binari di Low-Level</span><span class="sxs-lookup"><span data-stu-id="85b9b-103">New Low-Level Binaries</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="85b9b-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="85b9b-104">Affected Platforms</span></span>

<span data-ttu-id="85b9b-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="85b9b-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="85b9b-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85b9b-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="85b9b-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="85b9b-107">Feature Impact</span></span>

<span data-ttu-id="85b9b-108">**Gravità** -medio</span><span class="sxs-lookup"><span data-stu-id="85b9b-108">**Severity** - Medium</span></span>  
<span data-ttu-id="85b9b-109">**Frequenza** -alta</span><span class="sxs-lookup"><span data-stu-id="85b9b-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="85b9b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85b9b-110">Description</span></span>

<span data-ttu-id="85b9b-111">Per migliorare l'efficienza di progettazione interna e migliorare le fondamenta per il lavoro futuro, abbiamo rilocato alcune funzionalità per i nuovi file binari di basso livello.</span><span class="sxs-lookup"><span data-stu-id="85b9b-111">To improve internal engineering efficiencies and improve foundations for future work, we have relocated some functionality to new low-level binaries.</span></span> <span data-ttu-id="85b9b-112">Questo refactoring renderà possibile l'installazione futura di Windows per fornire subset di funzionalità per ridurre la superficie di attacco (requisiti di disco e memoria, manutenzione e superficie di attacco).</span><span class="sxs-lookup"><span data-stu-id="85b9b-112">This refactoring will make it possible for future installs of Windows to provide subsets of functionality to reduce surface area (disk and memory requirements, servicing, and attack surface).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="85b9b-113">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="85b9b-113">Manifestation of Impact</span></span>

<span data-ttu-id="85b9b-114">Come esempio di funzionalità che siamo passati a file binari di basso livello, kernelbase.dll ottiene la funzionalità da kernel32.dll e advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="85b9b-114">As an example of functionality that we moved to low-level binaries, kernelbase.dll gets functionality from kernel32.dll and advapi32.dll.</span></span> <span data-ttu-id="85b9b-115">Ciò significa che il file binario esistente ora esegue le chiamate al nuovo file binario anziché gestirli direttamente; l'invio può essere statico (la tabella di esportazione Mostra il reindirizzamento) o il runtime (la dll ha una routine stub che chiama il nuovo binario).</span><span class="sxs-lookup"><span data-stu-id="85b9b-115">This means that the existing binary now forwards calls down to the new binary rather than handling them directly; the forwarding can be static (the export table shows the redirection), or runtime (the dll has a stub routine that calls down to the new binary).</span></span> <span data-ttu-id="85b9b-116">Questo influirà sulle applicazioni di basso livello, ad esempio le applicazioni di sicurezza e di backup che dipendono da API e offset interni.</span><span class="sxs-lookup"><span data-stu-id="85b9b-116">This will impact low-level applications such as security and backup applications that are dependent upon internal APIs and offsets.</span></span>

## <a name="solution"></a><span data-ttu-id="85b9b-117">Soluzione</span><span class="sxs-lookup"><span data-stu-id="85b9b-117">Solution</span></span>

<span data-ttu-id="85b9b-118">L'unico effetto è il codice che fa supposizioni quando si tenta di esaminare la kernel32.dll o la tabella di esportazione advapi32.dll in memoria, ad esempio un'applicazione antivirus.</span><span class="sxs-lookup"><span data-stu-id="85b9b-118">The only impact is to code that makes assumptions when attempting to look at the kernel32.dll or the advapi32.dll export table in memory, such as an anti-virus application might do.</span></span> <span data-ttu-id="85b9b-119">Usare le API pubblicate e non i dettagli relativi all'implementazione.</span><span class="sxs-lookup"><span data-stu-id="85b9b-119">Use published APIs and not the details of their implementation.</span></span> <span data-ttu-id="85b9b-120">Questo è solo un esempio di implementazione di in un dettaglio di implementazione per un'API.</span><span class="sxs-lookup"><span data-stu-id="85b9b-120">This is just one example of implementing around a detail of implementation for an API.</span></span>

 

 



