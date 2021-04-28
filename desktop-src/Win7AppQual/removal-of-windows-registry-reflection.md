---
description: Rimozione della reflection del Registro di sistema di Windows
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Rimozione della reflection del Registro di sistema di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeab0109cbbac988c89d6add91fa899cea9169ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116259"
---
# <a name="removal-of-windows-registry-reflection"></a><span data-ttu-id="48c25-103">Rimozione della reflection del Registro di sistema di Windows</span><span class="sxs-lookup"><span data-stu-id="48c25-103">Removal of Windows Registry Reflection</span></span>

## <a name="platform"></a><span data-ttu-id="48c25-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="48c25-104">Platform</span></span>

<span data-ttu-id="48c25-105">**Client** - Windows 7</span><span class="sxs-lookup"><span data-stu-id="48c25-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="48c25-106">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48c25-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="48c25-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="48c25-107">Feature Impact</span></span>

 <span data-ttu-id="48c25-108">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="48c25-108">**Severity** - Low</span></span>  
<span data-ttu-id="48c25-109">**Frequenza** - Bassa</span><span class="sxs-lookup"><span data-stu-id="48c25-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="48c25-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48c25-110">Description</span></span>

<span data-ttu-id="48c25-111">Il processo di reflection del Registro di sistema copia le chiavi e i valori del Registro di sistema tra due viste del Registro di sistema per mantenerle sincronizzate. Nelle installazioni precedenti a 64 bit di Windows, il processo rifletteva un subset delle chiavi del Registro di sistema reindirizzate tra le visualizzazioni a 32 bit e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="48c25-111">The registry reflection process copies registry keys and values between two registry views to keep them in synch. In previous 64-bit installations of Windows, the process reflected a subset of the redirected registry keys between the 32-bit and 64-bit views.</span></span> <span data-ttu-id="48c25-112">Tuttavia, l'implementazione di questo ha causato alcune incoerenze nello stato del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="48c25-112">However, the implementation of this caused some inconsistencies in the state of the registry.</span></span> <span data-ttu-id="48c25-113">Per informazioni dettagliate sulla reflection del Registro di sistema, vedere l'articolo MSDN corrispondente *nella sezione Collegamenti* ad altre risorse riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="48c25-113">(For details on Registry Reflection, please refer to the corresponding MSDN article in the *Links to Other Resources* section below.)</span></span>

<span data-ttu-id="48c25-114">A partire da Windows 7, è stata rimossa completamente la reflection del Registro di sistema ed è stato unito il merge delle chiavi che si riflettevano:</span><span class="sxs-lookup"><span data-stu-id="48c25-114">Starting with Windows 7, we have removed registry reflection completely and merged the keys that used to be reflected:</span></span>

-   <span data-ttu-id="48c25-115">Classi software \_ HKEY LOCAL \_ MACHINE \\ \\</span><span class="sxs-lookup"><span data-stu-id="48c25-115">HKEY\_LOCAL\_MACHINE\\Software\\Classes</span></span>
-   <span data-ttu-id="48c25-116">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ COM3</span><span class="sxs-lookup"><span data-stu-id="48c25-116">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\COM3</span></span>
-   <span data-ttu-id="48c25-117">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ EventSystem</span><span class="sxs-lookup"><span data-stu-id="48c25-117">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\EventSystem</span></span>
-   <span data-ttu-id="48c25-118">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Ole</span><span class="sxs-lookup"><span data-stu-id="48c25-118">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Ole</span></span>
-   <span data-ttu-id="48c25-119">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Rpc</span><span class="sxs-lookup"><span data-stu-id="48c25-119">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc</span></span>
-   <span data-ttu-id="48c25-120">Classi software HKEY \_ USERS \\ \* \\ \\</span><span class="sxs-lookup"><span data-stu-id="48c25-120">HKEY\_USERS\\\*\\Software\\Classes</span></span>
-   <span data-ttu-id="48c25-121">Classi HKEY \_ USERS \\ \* \_</span><span class="sxs-lookup"><span data-stu-id="48c25-121">HKEY\_USERS\\\*\_Classes</span></span>

<span data-ttu-id="48c25-122">In effetti, ciò offre lo stesso comportamento di reflection, poiché le modifiche a queste chiavi sono immediatamente disponibili per le applicazioni a 32 bit e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="48c25-122">Effectively, this provides the same reflection behavior, since changes to these keys immediately are available for both 32-bit and 64-bit applications.</span></span>

<span data-ttu-id="48c25-123">Le chiavi riflesse in modo condizionale rimangono suddivise:</span><span class="sxs-lookup"><span data-stu-id="48c25-123">The keys that were reflected conditionally remain split:</span></span>

-   <span data-ttu-id="48c25-124">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Classes \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="48c25-124">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="48c25-125">Interfaccia delle classi software HKEY \_ LOCAL \_ MACHINE \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="48c25-125">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="48c25-126">HKEY \_ USERS - Classi software \\ \* \\ \\ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="48c25-126">HKEY\_USERS\\\*\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="48c25-127">Interfaccia delle \_ classi \\ \* \\ software \\ \\ HKEY USERS</span><span class="sxs-lookup"><span data-stu-id="48c25-127">HKEY\_USERS\\\*\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="48c25-128">HKEY \_ USERS \\ \* \_ Classes \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="48c25-128">HKEY\_USERS\\\*\_Classes\\CLSID</span></span>
-   <span data-ttu-id="48c25-129">Interfaccia delle classi HKEY \_ USERS \\ \* \_ \\</span><span class="sxs-lookup"><span data-stu-id="48c25-129">HKEY\_USERS\\\*\_Classes\\Interface</span></span>

<span data-ttu-id="48c25-130">Vengono usati per mantenere i dati che non devono essere condivisi tra le applicazioni a 32 bit e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="48c25-130">They are used to keep the data that should not be shared between 32-bit and 64-bit applications.</span></span>

## <a name="manifestation"></a><span data-ttu-id="48c25-131">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="48c25-131">Manifestation</span></span>

<span data-ttu-id="48c25-132">Le chiavi CLSID e Interface dell'elenco precedente non vengono più riflesse mentre sono ancora reindirizzate.</span><span class="sxs-lookup"><span data-stu-id="48c25-132">CLSID and Interface keys from the list above are not reflected anymore while they are still redirected.</span></span> <span data-ttu-id="48c25-133">Anche se si tratta del comportamento desiderato nella maggior parte dei casi, è possibile che le applicazioni prendano una dipendenza dal comportamento riflessa in Vista.</span><span class="sxs-lookup"><span data-stu-id="48c25-133">While this is the desired behavior in most of cases, it is possible that applications could take a dependency on their reflected behavior in Vista.</span></span>

<span data-ttu-id="48c25-134">Le funzioni che consentono alle applicazioni di controllare la reflection (RegDisableReflectionKey e RegEnableReflectionKey) non sono operazioni in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="48c25-134">The functions allowing applications to control reflection (RegDisableReflectionKey and RegEnableReflectionKey) are no-ops in Windows 7.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="48c25-135">Mitigazione dell'impatto</span><span class="sxs-lookup"><span data-stu-id="48c25-135">Mitigation of Impact</span></span>

<span data-ttu-id="48c25-136">COM è il principale consumer della reflection del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="48c25-136">COM is the major consumer of registry reflection.</span></span> <span data-ttu-id="48c25-137">COM e altri consumer sono stati aggiornati per supportare questa modifica.</span><span class="sxs-lookup"><span data-stu-id="48c25-137">COM and other consumers were updated to accommodate this change.</span></span> <span data-ttu-id="48c25-138">Questa modifica non influisce sulle applicazioni che usano API COM standard.</span><span class="sxs-lookup"><span data-stu-id="48c25-138">This change does not affect applications that use standard COM APIs..</span></span>

## <a name="solution"></a><span data-ttu-id="48c25-139">Soluzione</span><span class="sxs-lookup"><span data-stu-id="48c25-139">Solution</span></span>

<span data-ttu-id="48c25-140">Applicare una delle opzioni seguenti se si fa affidamento sulla reflection del Registro di sistema per sincronizzare le visualizzazioni a 32 bit e a 64 bit:</span><span class="sxs-lookup"><span data-stu-id="48c25-140">Apply one of the following options if you are relying on registry reflection to synchronize 32bit and 64bit views:</span></span>

-   <span data-ttu-id="48c25-141">Creare chiavi in entrambe le visualizzazioni in modo esplicito durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="48c25-141">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="48c25-142">Spostare le chiavi all'esterno dell'ambito delle chiavi riflesse</span><span class="sxs-lookup"><span data-stu-id="48c25-142">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="48c25-143">Controllare entrambe le viste del Registro di sistema durante l'esecuzione di query per una chiave riflessa</span><span class="sxs-lookup"><span data-stu-id="48c25-143">Check both views of the registry when querying for a reflected key</span></span>

    <span data-ttu-id="48c25-144">**Nota:** I \_ flag KEY WOW64 \_ 32KEY e KEY \_ WOW64 \_ 64KEY non possono essere combinati</span><span class="sxs-lookup"><span data-stu-id="48c25-144">**Note:** KEY\_WOW64\_32KEY and KEY\_WOW64\_64KEY flags cannot be combined</span></span>

<span data-ttu-id="48c25-145">Applicare una delle opzioni seguenti se si fa affidamento sulle funzioni RegDisableReflectionKey per disabilitare la reflection del Registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="48c25-145">Apply one of the following options if you are relying on RegDisableReflectionKey functions to disable registry reflection:</span></span>

-   <span data-ttu-id="48c25-146">Creare le chiavi in entrambe le viste in modo esplicito durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="48c25-146">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="48c25-147">Spostare le chiavi all'esterno dell'ambito delle chiavi riflesse</span><span class="sxs-lookup"><span data-stu-id="48c25-147">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="48c25-148">Usare sottochiavi specifiche della piattaforma (ad esempio x86, amd64 e ia64) per separare i dati specifici del bitness</span><span class="sxs-lookup"><span data-stu-id="48c25-148">Use platform-specific subkeys (like x86, amd64 and ia64) to separate bitness-specific data</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="48c25-149">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="48c25-149">Links to Other Resources</span></span>

-   [<span data-ttu-id="48c25-150">Articolo sulla reflection del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="48c25-150">Registry Reflection article</span></span>](../winprog64/registry-reflection.md)
-   [<span data-ttu-id="48c25-151">Elenco di chiavi reindirizzate all'interno dell'articolo Redirector del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="48c25-151">Redirected keys list within Registry Redirector article</span></span>](../winprog64/registry-redirector.md)
-   [<span data-ttu-id="48c25-152">Procedure consigliate per Wow64</span><span class="sxs-lookup"><span data-stu-id="48c25-152">Best Practices for Wow64</span></span>](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> <span data-ttu-id="48c25-153">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="48c25-153">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
