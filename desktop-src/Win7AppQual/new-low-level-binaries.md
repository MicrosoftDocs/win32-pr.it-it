---
description: Nuovi Low-Level binari
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Nuovi Low-Level binari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4640d31b115dc85ecde9f9423997468ddc8456
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088069"
---
# <a name="new-low-level-binaries"></a><span data-ttu-id="ef4e7-103">Nuovi Low-Level binari</span><span class="sxs-lookup"><span data-stu-id="ef4e7-103">New Low-Level Binaries</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="ef4e7-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="ef4e7-104">Affected Platforms</span></span>

<span data-ttu-id="ef4e7-105">**Client** - Windows 7</span><span class="sxs-lookup"><span data-stu-id="ef4e7-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="ef4e7-106">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef4e7-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="ef4e7-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="ef4e7-107">Feature Impact</span></span>

<span data-ttu-id="ef4e7-108">**Gravità** - Media</span><span class="sxs-lookup"><span data-stu-id="ef4e7-108">**Severity** - Medium</span></span>  
<span data-ttu-id="ef4e7-109">**Frequenza** - Alta</span><span class="sxs-lookup"><span data-stu-id="ef4e7-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="ef4e7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef4e7-110">Description</span></span>

<span data-ttu-id="ef4e7-111">Per migliorare l'efficienza di progettazione interna e migliorare le basi per il lavoro futuro, alcune funzionalità sono state rilocate in nuovi file binari di basso livello.</span><span class="sxs-lookup"><span data-stu-id="ef4e7-111">To improve internal engineering efficiencies and improve foundations for future work, we have relocated some functionality to new low-level binaries.</span></span> <span data-ttu-id="ef4e7-112">Questo refactoring consente alle installazioni future di Windows di fornire subset di funzionalità per ridurre la superficie di attacco (requisiti di memoria e disco, manutenzione e superficie di attacco).</span><span class="sxs-lookup"><span data-stu-id="ef4e7-112">This refactoring will make it possible for future installs of Windows to provide subsets of functionality to reduce surface area (disk and memory requirements, servicing, and attack surface).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="ef4e7-113">Impatto significativo</span><span class="sxs-lookup"><span data-stu-id="ef4e7-113">Manifestation of Impact</span></span>

<span data-ttu-id="ef4e7-114">Come esempio di funzionalità che è stata spostata nei file binari di basso livello, kernelbase.dll le funzionalità da kernel32.dll e advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="ef4e7-114">As an example of functionality that we moved to low-level binaries, kernelbase.dll gets functionality from kernel32.dll and advapi32.dll.</span></span> <span data-ttu-id="ef4e7-115">Ciò significa che il file binario esistente ora inoltra le chiamate al nuovo file binario anziché gestirle direttamente. L'inoltro può essere statico (la tabella di esportazione mostra il reindirizzamento) o runtime (la DLL ha una routine stub che chiama il nuovo file binario).</span><span class="sxs-lookup"><span data-stu-id="ef4e7-115">This means that the existing binary now forwards calls down to the new binary rather than handling them directly; the forwarding can be static (the export table shows the redirection), or runtime (the dll has a stub routine that calls down to the new binary).</span></span> <span data-ttu-id="ef4e7-116">Ciò inciderà sulle applicazioni di basso livello, ad esempio le applicazioni di sicurezza e di backup che dipendono da API interne e offset.</span><span class="sxs-lookup"><span data-stu-id="ef4e7-116">This will impact low-level applications such as security and backup applications that are dependent upon internal APIs and offsets.</span></span>

## <a name="solution"></a><span data-ttu-id="ef4e7-117">Soluzione</span><span class="sxs-lookup"><span data-stu-id="ef4e7-117">Solution</span></span>

<span data-ttu-id="ef4e7-118">L'unico impatto è sul codice che fa ipotesi quando si tenta di esaminare il kernel32.dll o la tabella di esportazione advapi32.dll in memoria, ad esempio un'applicazione antivirus.</span><span class="sxs-lookup"><span data-stu-id="ef4e7-118">The only impact is to code that makes assumptions when attempting to look at the kernel32.dll or the advapi32.dll export table in memory, such as an anti-virus application might do.</span></span> <span data-ttu-id="ef4e7-119">Usare le API pubblicate e non i dettagli dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="ef4e7-119">Use published APIs and not the details of their implementation.</span></span> <span data-ttu-id="ef4e7-120">Questo è solo un esempio di implementazione di in base a un dettaglio di implementazione per un'API.</span><span class="sxs-lookup"><span data-stu-id="ef4e7-120">This is just one example of implementing around a detail of implementation for an API.</span></span>

 

 



