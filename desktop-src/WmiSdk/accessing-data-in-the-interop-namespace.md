---
description: I provider di associazioni consentono ai client di Strumentazione gestione Windows (WMI) di attraversare e recuperare i profili e le istanze di classe associate da spazi dei nomi diversi.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Accesso ai dati nello spazio dei nomi Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968370"
---
# <a name="accessing-data-in-the-interop-namespace"></a><span data-ttu-id="40a99-103">Accesso ai dati nello spazio dei nomi Interop</span><span class="sxs-lookup"><span data-stu-id="40a99-103">Accessing Data in the Interop Namespace</span></span>

<span data-ttu-id="40a99-104">I provider di associazioni consentono ai client di Strumentazione gestione Windows (WMI) di attraversare e recuperare i profili e le istanze di classe associate da spazi dei nomi diversi.</span><span class="sxs-lookup"><span data-stu-id="40a99-104">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>

<span data-ttu-id="40a99-105">I provider di associazioni e le classi si trovano nello \\ \\ \\ spazio dei nomi di interoperabilità radice.</span><span class="sxs-lookup"><span data-stu-id="40a99-105">Association providers and classes reside in the \\\\root\\interop namespace.</span></span> <span data-ttu-id="40a99-106">Per ulteriori informazioni, vedere attraversamento dell' [associazione tra spazi dei nomi](cross-namespace-association-traversal.md) e [scrittura di un provider di associazioni](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="40a99-106">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md) and [Writing an Association Provider](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="40a99-107">I provider di associazioni espongono i profili standard, ad esempio un profilo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="40a99-107">Association providers expose standard profiles, like a power profile.</span></span> <span data-ttu-id="40a99-108">Gli esempi seguenti usano il profilo Power per illustrare come individuare e accedere ai dati tramite lo spazio dei nomi Interop.</span><span class="sxs-lookup"><span data-stu-id="40a99-108">The following examples use the power profile to illustrate how to discover and access data through the interop namespace.</span></span>

<span data-ttu-id="40a99-109">Windows PowerShell fornisce un meccanismo semplice per attraversare l'associazione appropriata, recuperare un profilo di dispositivo e chiamare un metodo.</span><span class="sxs-lookup"><span data-stu-id="40a99-109">Windows PowerShell provides a simple mechanism to traverse through the appropriate association, retrieve a device profile, and call a method.</span></span>

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a><span data-ttu-id="40a99-110">Enumerazione di profili nello spazio dei nomi radice/interoperabilità</span><span class="sxs-lookup"><span data-stu-id="40a99-110">Enumerating profiles in the root/interop namespace</span></span>

<span data-ttu-id="40a99-111">Il comando di Windows PowerShell seguente enumera i profili supportati da Distributed Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) in un computer Windows 7:</span><span class="sxs-lookup"><span data-stu-id="40a99-111">The following Windows PowerShell command enumerates the Distributed Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman))-supported profiles on a Windows 7 computer:</span></span>


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a><span data-ttu-id="40a99-112">Recupero di istanze di un profilo di dispositivo specifico</span><span class="sxs-lookup"><span data-stu-id="40a99-112">Retrieving instances of a specific device profile</span></span>

<span data-ttu-id="40a99-113">Il comando di Windows PowerShell seguente restituisce tutte le istanze di un profilo specificato tramite [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="40a99-113">The following Windows PowerShell command returns all instances of a specified profile through [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):</span></span>


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a><span data-ttu-id="40a99-114">Assegnazione del profilo di alimentazione a una variabile</span><span class="sxs-lookup"><span data-stu-id="40a99-114">Assigning the power profile to a variable</span></span>

<span data-ttu-id="40a99-115">Con il comando di Windows PowerShell seguente viene assegnata l'istanza del profilo Power a una variabile:</span><span class="sxs-lookup"><span data-stu-id="40a99-115">The following Windows PowerShell command assigns the power profile instance to a variable:</span></span>


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a><span data-ttu-id="40a99-116">Enumerazione delle combinazioni per il risparmio di energia in un computer</span><span class="sxs-lookup"><span data-stu-id="40a99-116">Enumerating the power plans on a computer</span></span>

<span data-ttu-id="40a99-117">Il comando di Windows PowerShell seguente enumera i piani di Power profile disponibili:</span><span class="sxs-lookup"><span data-stu-id="40a99-117">The following Windows PowerShell command enumerates the available power profile plans:</span></span>


```PowerShell
$pplan
```



## <a name="calling-a-method"></a><span data-ttu-id="40a99-118">Chiamata di un metodo</span><span class="sxs-lookup"><span data-stu-id="40a99-118">Calling a method</span></span>

<span data-ttu-id="40a99-119">Il seguente comando di Windows PowerShell chiama il metodo [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) per la combinazione per il risparmio di energia:</span><span class="sxs-lookup"><span data-stu-id="40a99-119">The following Windows PowerShell command calls the [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) method for the power plan:</span></span>


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a><span data-ttu-id="40a99-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40a99-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40a99-121">Attraversamento dell'associazione tra spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="40a99-121">Cross Namespace Association Traversal</span></span>](cross-namespace-association-traversal.md)
</dt> <dt>

[<span data-ttu-id="40a99-122">Scrittura di un provider di associazioni</span><span class="sxs-lookup"><span data-stu-id="40a99-122">Writing an Association Provider</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

<span data-ttu-id="40a99-123">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="40a99-123">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="40a99-124">[**\_PowerPlan Win32**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="40a99-124">[**Win32\_PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span></span>
</dt> </dl>

 

 
