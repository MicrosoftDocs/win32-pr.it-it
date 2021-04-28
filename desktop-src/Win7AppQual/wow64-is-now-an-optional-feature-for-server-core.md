---
description: WoW64 è ora una funzionalità facoltativa per Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Stato di WoW64 in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad947dac85707d3c9c89a2cffea38c4a4850a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084049"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a><span data-ttu-id="e1f71-103">WoW64 è ora una funzionalità facoltativa per Server Core</span><span class="sxs-lookup"><span data-stu-id="e1f71-103">WoW64 Is Now an Optional Feature for Server Core</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e1f71-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="e1f71-104">Affected Platforms</span></span>

<span data-ttu-id="e1f71-105">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e1f71-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="e1f71-106">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="e1f71-106">Feature Impact</span></span>

 <span data-ttu-id="e1f71-107">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="e1f71-107">**Severity** - Low</span></span>  
<span data-ttu-id="e1f71-108">**Frequenza** - Bassa</span><span class="sxs-lookup"><span data-stu-id="e1f71-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="e1f71-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1f71-109">Description</span></span>

<span data-ttu-id="e1f71-110">L'opzione di installazione Server Core per Windows Server 2008 R2 consente di disinstallare WoW64.</span><span class="sxs-lookup"><span data-stu-id="e1f71-110">The Server Core installation option for Windows Server 2008 R2 allows you to uninstall WoW64.</span></span> <span data-ttu-id="e1f71-111">WoW64 è ora una funzionalità facoltativa che è possibile disinstallare se non è necessario eseguire codice a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="e1f71-111">WoW64 is now an optional feature that you can uninstall if it is not necessary to run 32-bit code.</span></span>

<span data-ttu-id="e1f71-112">Inoltre, i ruoli Active Directory e Active Directory Lightweight Directory Services richiedono WoW64 per l'esecuzione in Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="e1f71-112">In addition, the Active Directory and Active Directory Lightweight Directory Services roles require WoW64 in order to run in Windows Server 2008 R2.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="e1f71-113">Manifestazione di impatto</span><span class="sxs-lookup"><span data-stu-id="e1f71-113">Manifestation of Impact</span></span>

<span data-ttu-id="e1f71-114">Se si disinstalla WoW64, gli amministratori che eseguono codice a 32 bit in Server Core riceveranno un messaggio di errore che indica che l'applicazione non può essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="e1f71-114">If you uninstall WoW64, Administrators running 32-bit code on Server Core will receive an error message that the application cannot be executed.</span></span> <span data-ttu-id="e1f71-115">Se gli amministratori tentano di eseguire Active Directory Active Directory Lightweight Directory Services, riceveranno un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="e1f71-115">If Administrators attempt to run Active Directory and Active Directory Lightweight Directory Services, they will receive an error message.</span></span>

## <a name="mitigation"></a><span data-ttu-id="e1f71-116">Mitigazione</span><span class="sxs-lookup"><span data-stu-id="e1f71-116">Mitigation</span></span>

<span data-ttu-id="e1f71-117">Installare WoW64.</span><span class="sxs-lookup"><span data-stu-id="e1f71-117">Install WoW64.</span></span>

## <a name="solution"></a><span data-ttu-id="e1f71-118">Soluzione</span><span class="sxs-lookup"><span data-stu-id="e1f71-118">Solution</span></span>

<span data-ttu-id="e1f71-119">La soluzione preferita consiste nel fornire una versione a 64 bit del codice per consentire l'esecuzione in Server Core senza la necessità di WoW64.</span><span class="sxs-lookup"><span data-stu-id="e1f71-119">The preferred solution is to provide a 64-bit version of the code to enable it to run on Server Core without needing WoW64.</span></span>

<span data-ttu-id="e1f71-120">Fornire almeno la documentazione dell'utente che indica che per eseguire codice a 32 bit è necessario installare WoW64.</span><span class="sxs-lookup"><span data-stu-id="e1f71-120">At a minimum, provide user documentation noting that to run 32-bit code they must install WoW64.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="e1f71-121">Test di compatibilità, prestazioni, affidabilità e usabilità</span><span class="sxs-lookup"><span data-stu-id="e1f71-121">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="e1f71-122">Verificare che tutto il codice usato sia a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="e1f71-122">Verify that all code used is 64-bit.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="e1f71-123">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="e1f71-123">Links to Other Resources</span></span>

-   [<span data-ttu-id="e1f71-124">Dettagli sull'implementazione di WOW64</span><span class="sxs-lookup"><span data-stu-id="e1f71-124">WOW64 Implementation Details</span></span>](../winprog64/wow64-implementation-details.md)
-   [<span data-ttu-id="e1f71-125">Debug di WOW64</span><span class="sxs-lookup"><span data-stu-id="e1f71-125">Debugging WOW64</span></span>](../winprog64/debugging-wow64.md)
-   <span data-ttu-id="e1f71-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e1f71-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>

 

 
