---
description: .
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Stato WoW64 in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a121c6bb9c4fb2cd052825bb4c2d5e3dbd0183c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318563"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a><span data-ttu-id="82bd0-103">WoW64 è ora una funzionalità facoltativa per Server Core</span><span class="sxs-lookup"><span data-stu-id="82bd0-103">WoW64 Is Now an Optional Feature for Server Core</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="82bd0-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="82bd0-104">Affected Platforms</span></span>

<span data-ttu-id="82bd0-105">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="82bd0-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="82bd0-106">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="82bd0-106">Feature Impact</span></span>

 <span data-ttu-id="82bd0-107">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="82bd0-107">**Severity** - Low</span></span>  
<span data-ttu-id="82bd0-108">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="82bd0-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="82bd0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82bd0-109">Description</span></span>

<span data-ttu-id="82bd0-110">L'opzione di installazione dei componenti di base del server per Windows Server 2008 R2 consente di disinstallare WoW64.</span><span class="sxs-lookup"><span data-stu-id="82bd0-110">The Server Core installation option for Windows Server 2008 R2 allows you to uninstall WoW64.</span></span> <span data-ttu-id="82bd0-111">WoW64 è ora una funzionalità facoltativa che è possibile disinstallare se non è necessario eseguire codice a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="82bd0-111">WoW64 is now an optional feature that you can uninstall if it is not necessary to run 32-bit code.</span></span>

<span data-ttu-id="82bd0-112">Inoltre, per l'esecuzione in Windows Server 2008 R2, i ruoli Active Directory e Active Directory Lightweight Directory Services richiedono WoW64.</span><span class="sxs-lookup"><span data-stu-id="82bd0-112">In addition, the Active Directory and Active Directory Lightweight Directory Services roles require WoW64 in order to run in Windows Server 2008 R2.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="82bd0-113">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="82bd0-113">Manifestation of Impact</span></span>

<span data-ttu-id="82bd0-114">Se si disinstalla WoW64, gli amministratori che eseguono codice a 32 bit in Server Core riceveranno un messaggio di errore che segnala che non è possibile eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="82bd0-114">If you uninstall WoW64, Administrators running 32-bit code on Server Core will receive an error message that the application cannot be executed.</span></span> <span data-ttu-id="82bd0-115">Se gli amministratori tentano di eseguire Active Directory e Active Directory Lightweight Directory Services, riceveranno un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="82bd0-115">If Administrators attempt to run Active Directory and Active Directory Lightweight Directory Services, they will receive an error message.</span></span>

## <a name="mitigation"></a><span data-ttu-id="82bd0-116">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="82bd0-116">Mitigation</span></span>

<span data-ttu-id="82bd0-117">Installare WoW64.</span><span class="sxs-lookup"><span data-stu-id="82bd0-117">Install WoW64.</span></span>

## <a name="solution"></a><span data-ttu-id="82bd0-118">Soluzione</span><span class="sxs-lookup"><span data-stu-id="82bd0-118">Solution</span></span>

<span data-ttu-id="82bd0-119">La soluzione preferita consiste nel fornire una versione a 64 bit del codice per consentirne l'esecuzione in Server Core senza la necessità di WoW64.</span><span class="sxs-lookup"><span data-stu-id="82bd0-119">The preferred solution is to provide a 64-bit version of the code to enable it to run on Server Core without needing WoW64.</span></span>

<span data-ttu-id="82bd0-120">Fornire almeno la documentazione utente nota per eseguire codice a 32 bit, è necessario installare WoW64.</span><span class="sxs-lookup"><span data-stu-id="82bd0-120">At a minimum, provide user documentation noting that to run 32-bit code they must install WoW64.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="82bd0-121">Compatibilità, prestazioni, affidabilità e test di usabilità</span><span class="sxs-lookup"><span data-stu-id="82bd0-121">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="82bd0-122">Verificare che tutto il codice utilizzato sia a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="82bd0-122">Verify that all code used is 64-bit.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="82bd0-123">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="82bd0-123">Links to Other Resources</span></span>

-   [<span data-ttu-id="82bd0-124">Dettagli di implementazione di WOW64</span><span class="sxs-lookup"><span data-stu-id="82bd0-124">WOW64 Implementation Details</span></span>](../winprog64/wow64-implementation-details.md)
-   [<span data-ttu-id="82bd0-125">Debug di WOW64</span><span class="sxs-lookup"><span data-stu-id="82bd0-125">Debugging WOW64</span></span>](../winprog64/debugging-wow64.md)
-   <span data-ttu-id="82bd0-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82bd0-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>

 

 
