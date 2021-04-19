---
description: .
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Rimozione della reflection del registro di sistema di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c610cb0b6ce446e3105fd61cb940028f478892ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317613"
---
# <a name="removal-of-windows-registry-reflection"></a><span data-ttu-id="0bc5e-103">Rimozione della reflection del registro di sistema di Windows</span><span class="sxs-lookup"><span data-stu-id="0bc5e-103">Removal of Windows Registry Reflection</span></span>

## <a name="platform"></a><span data-ttu-id="0bc5e-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="0bc5e-104">Platform</span></span>

<span data-ttu-id="0bc5e-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="0bc5e-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="0bc5e-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0bc5e-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="0bc5e-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="0bc5e-107">Feature Impact</span></span>

 <span data-ttu-id="0bc5e-108">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="0bc5e-108">**Severity** - Low</span></span>  
<span data-ttu-id="0bc5e-109">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="0bc5e-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="0bc5e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bc5e-110">Description</span></span>

<span data-ttu-id="0bc5e-111">Il processo di reflection del registro di sistema copia le chiavi e i valori del registro di sistema tra due visualizzazioni del registro di sistema per mantene Nelle installazioni precedenti di Windows a 64 bit, il processo ha riflesso un subset delle chiavi del registro di sistema reindirizzate tra le visualizzazioni a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-111">The registry reflection process copies registry keys and values between two registry views to keep them in synch. In previous 64-bit installations of Windows, the process reflected a subset of the redirected registry keys between the 32-bit and 64-bit views.</span></span> <span data-ttu-id="0bc5e-112">Tuttavia, l'implementazione di questo ha causato alcune incoerenze nello stato del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-112">However, the implementation of this caused some inconsistencies in the state of the registry.</span></span> <span data-ttu-id="0bc5e-113">Per informazioni dettagliate sulla reflection del registro di sistema, vedere l'articolo di MSDN corrispondente nella sezione *collegamenti ad altre risorse* .</span><span class="sxs-lookup"><span data-stu-id="0bc5e-113">(For details on Registry Reflection, please refer to the corresponding MSDN article in the *Links to Other Resources* section below.)</span></span>

<span data-ttu-id="0bc5e-114">A partire da Windows 7, la reflection del registro di sistema è stata rimossa completamente e sono state unite le chiavi che erano state riflesse:</span><span class="sxs-lookup"><span data-stu-id="0bc5e-114">Starting with Windows 7, we have removed registry reflection completely and merged the keys that used to be reflected:</span></span>

-   <span data-ttu-id="0bc5e-115">\_ \_ Classi software del computer locale \\ HKEY \\</span><span class="sxs-lookup"><span data-stu-id="0bc5e-115">HKEY\_LOCAL\_MACHINE\\Software\\Classes</span></span>
-   <span data-ttu-id="0bc5e-116">HKEY \_ \_ computer locale \\ software \\ Microsoft \\ COM3</span><span class="sxs-lookup"><span data-stu-id="0bc5e-116">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\COM3</span></span>
-   <span data-ttu-id="0bc5e-117">HKEY \_ \_ computer locale \\ software \\ Microsoft \\ EventSystem</span><span class="sxs-lookup"><span data-stu-id="0bc5e-117">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\EventSystem</span></span>
-   <span data-ttu-id="0bc5e-118">\_Software per \_ computer locale HKEY \\ \\ Microsoft \\ OLE</span><span class="sxs-lookup"><span data-stu-id="0bc5e-118">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Ole</span></span>
-   <span data-ttu-id="0bc5e-119">HKEY \_ \_ computer locale \\ software \\ Microsoft \\ RPC</span><span class="sxs-lookup"><span data-stu-id="0bc5e-119">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc</span></span>
-   <span data-ttu-id="0bc5e-120">\_ \\ \* \\ Classi software per utenti \\ HKEY</span><span class="sxs-lookup"><span data-stu-id="0bc5e-120">HKEY\_USERS\\\*\\Software\\Classes</span></span>
-   <span data-ttu-id="0bc5e-121">\_Classi di utenti HKEY \\ \* \_</span><span class="sxs-lookup"><span data-stu-id="0bc5e-121">HKEY\_USERS\\\*\_Classes</span></span>

<span data-ttu-id="0bc5e-122">In realtà, questo fornisce lo stesso comportamento di reflection, dal momento che le modifiche apportate a queste chiavi sono immediatamente disponibili per le applicazioni a 32 bit e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-122">Effectively, this provides the same reflection behavior, since changes to these keys immediately are available for both 32-bit and 64-bit applications.</span></span>

<span data-ttu-id="0bc5e-123">Le chiavi riflesse in modo condizionale rimangono separate:</span><span class="sxs-lookup"><span data-stu-id="0bc5e-123">The keys that were reflected conditionally remain split:</span></span>

-   <span data-ttu-id="0bc5e-124">HKEY \_ \_ classi software del computer locale \\ \\ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="0bc5e-124">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="0bc5e-125">\_Interfaccia delle \_ \\ classi software \\ del computer locale HKEY \\</span><span class="sxs-lookup"><span data-stu-id="0bc5e-125">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="0bc5e-126">\_ \\ \* \\ Classi software utenti \\ HKEY \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="0bc5e-126">HKEY\_USERS\\\*\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="0bc5e-127">\_ \\ \* \\ \\ Interfaccia classi software \\ utenti HKEY</span><span class="sxs-lookup"><span data-stu-id="0bc5e-127">HKEY\_USERS\\\*\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="0bc5e-128">\_Classi di utenti HKEY \\ \* \_ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="0bc5e-128">HKEY\_USERS\\\*\_Classes\\CLSID</span></span>
-   <span data-ttu-id="0bc5e-129">\_ \\ \* \_ Interfaccia classi utenti \\ HKEY</span><span class="sxs-lookup"><span data-stu-id="0bc5e-129">HKEY\_USERS\\\*\_Classes\\Interface</span></span>

<span data-ttu-id="0bc5e-130">Vengono utilizzati per tenere i dati che non devono essere condivisi tra applicazioni a 32 bit e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-130">They are used to keep the data that should not be shared between 32-bit and 64-bit applications.</span></span>

## <a name="manifestation"></a><span data-ttu-id="0bc5e-131">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="0bc5e-131">Manifestation</span></span>

<span data-ttu-id="0bc5e-132">Il CLSID e le chiavi di interfaccia dall'elenco precedente non vengono più riflesse mentre vengono ancora reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-132">CLSID and Interface keys from the list above are not reflected anymore while they are still redirected.</span></span> <span data-ttu-id="0bc5e-133">Sebbene questo sia il comportamento desiderato nella maggior parte dei casi, è possibile che le applicazioni possano assumere una dipendenza dal comportamento riflesso in vista.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-133">While this is the desired behavior in most of cases, it is possible that applications could take a dependency on their reflected behavior in Vista.</span></span>

<span data-ttu-id="0bc5e-134">Le funzioni che consentono alle applicazioni di controllare la reflection (RegDisableReflectionKey e RegEnableReflectionKey) non sono Ops in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-134">The functions allowing applications to control reflection (RegDisableReflectionKey and RegEnableReflectionKey) are no-ops in Windows 7.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="0bc5e-135">Attenuazione dell'effetto</span><span class="sxs-lookup"><span data-stu-id="0bc5e-135">Mitigation of Impact</span></span>

<span data-ttu-id="0bc5e-136">COM è il principale consumatore della reflection del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-136">COM is the major consumer of registry reflection.</span></span> <span data-ttu-id="0bc5e-137">COM e altri consumer sono stati aggiornati per adattarsi a questa modifica.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-137">COM and other consumers were updated to accommodate this change.</span></span> <span data-ttu-id="0bc5e-138">Questa modifica non influisce sulle applicazioni che utilizzano API COM standard.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-138">This change does not affect applications that use standard COM APIs..</span></span>

## <a name="solution"></a><span data-ttu-id="0bc5e-139">Soluzione</span><span class="sxs-lookup"><span data-stu-id="0bc5e-139">Solution</span></span>

<span data-ttu-id="0bc5e-140">Applicare una delle opzioni seguenti se si basa la reflection del registro di sistema per sincronizzare le visualizzazioni a 32 bit e a 64 bit:</span><span class="sxs-lookup"><span data-stu-id="0bc5e-140">Apply one of the following options if you are relying on registry reflection to synchronize 32bit and 64bit views:</span></span>

-   <span data-ttu-id="0bc5e-141">Crea chiavi in entrambe le visualizzazioni in modo esplicito durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="0bc5e-141">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="0bc5e-142">Spostare le chiavi dall'ambito delle chiavi riflesse</span><span class="sxs-lookup"><span data-stu-id="0bc5e-142">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="0bc5e-143">Controllare entrambe le visualizzazioni del registro di sistema quando si esegue una query per una chiave riflessa</span><span class="sxs-lookup"><span data-stu-id="0bc5e-143">Check both views of the registry when querying for a reflected key</span></span>

    <span data-ttu-id="0bc5e-144">**Nota:** \_ \_ \_ \_ Impossibile combinare i flag 64KEY di WOW64 32KEY e Key WOW64</span><span class="sxs-lookup"><span data-stu-id="0bc5e-144">**Note:** KEY\_WOW64\_32KEY and KEY\_WOW64\_64KEY flags cannot be combined</span></span>

<span data-ttu-id="0bc5e-145">Applicare una delle opzioni seguenti se si basano sulle funzioni RegDisableReflectionKey per disabilitare la reflection del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="0bc5e-145">Apply one of the following options if you are relying on RegDisableReflectionKey functions to disable registry reflection:</span></span>

-   <span data-ttu-id="0bc5e-146">Crea chiavi in entrambe le visualizzazioni in modo esplicito durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="0bc5e-146">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="0bc5e-147">Spostare le chiavi dall'ambito delle chiavi riflesse</span><span class="sxs-lookup"><span data-stu-id="0bc5e-147">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="0bc5e-148">Usare sottochiavi specifiche della piattaforma (ad esempio x86, amd64 e ia64) per separare i dati specifici di bit</span><span class="sxs-lookup"><span data-stu-id="0bc5e-148">Use platform-specific subkeys (like x86, amd64 and ia64) to separate bitness-specific data</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="0bc5e-149">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="0bc5e-149">Links to Other Resources</span></span>

-   [<span data-ttu-id="0bc5e-150">Articolo di reflection del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0bc5e-150">Registry Reflection article</span></span>](../winprog64/registry-reflection.md)
-   [<span data-ttu-id="0bc5e-151">Elenco delle chiavi reindirizzate nell'articolo redirector del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0bc5e-151">Redirected keys list within Registry Redirector article</span></span>](../winprog64/registry-redirector.md)
-   [<span data-ttu-id="0bc5e-152">Procedure consigliate per WOW64</span><span class="sxs-lookup"><span data-stu-id="0bc5e-152">Best Practices for Wow64</span></span>](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> <span data-ttu-id="0bc5e-153">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-153">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
