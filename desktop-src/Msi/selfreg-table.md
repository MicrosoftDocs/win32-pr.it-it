---
description: La tabella SelfReg contiene informazioni sui moduli che devono essere registrati autonomamente.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Tabella SelfReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5895b1d23369a7c121547fed841731b5d3e76ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760145"
---
# <a name="selfreg-table"></a><span data-ttu-id="56f8f-103">Tabella SelfReg</span><span class="sxs-lookup"><span data-stu-id="56f8f-103">SelfReg Table</span></span>

<span data-ttu-id="56f8f-104">La tabella SelfReg contiene informazioni sui moduli che devono essere registrati autonomamente.</span><span class="sxs-lookup"><span data-stu-id="56f8f-104">The SelfReg table contains information about modules that need to be self registered.</span></span> <span data-ttu-id="56f8f-105">Il programma di installazione chiama la funzione [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) durante l'installazione del modulo. chiama [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) durante la disinstallazione del modulo.</span><span class="sxs-lookup"><span data-stu-id="56f8f-105">The installer calls the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function during installation of the module; it calls [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) during uninstallation of the module.</span></span> <span data-ttu-id="56f8f-106">Il programma di installazione non registra autonomamente i file EXE.</span><span class="sxs-lookup"><span data-stu-id="56f8f-106">The installer does not self register EXE files.</span></span>

<span data-ttu-id="56f8f-107">La tabella SelfReg include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="56f8f-107">The SelfReg table has the following columns.</span></span>



| <span data-ttu-id="56f8f-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="56f8f-108">Column</span></span> | <span data-ttu-id="56f8f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="56f8f-109">Type</span></span>                         | <span data-ttu-id="56f8f-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="56f8f-110">Key</span></span> | <span data-ttu-id="56f8f-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="56f8f-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="56f8f-112">file\_</span><span class="sxs-lookup"><span data-stu-id="56f8f-112">File\_</span></span> | [<span data-ttu-id="56f8f-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="56f8f-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="56f8f-114">S</span><span class="sxs-lookup"><span data-stu-id="56f8f-114">Y</span></span>   | <span data-ttu-id="56f8f-115">N</span><span class="sxs-lookup"><span data-stu-id="56f8f-115">N</span></span>        |
| <span data-ttu-id="56f8f-116">Costo</span><span class="sxs-lookup"><span data-stu-id="56f8f-116">Cost</span></span>   | [<span data-ttu-id="56f8f-117">Integer</span><span class="sxs-lookup"><span data-stu-id="56f8f-117">Integer</span></span>](integer.md)       | <span data-ttu-id="56f8f-118">N</span><span class="sxs-lookup"><span data-stu-id="56f8f-118">N</span></span>   | <span data-ttu-id="56f8f-119">S</span><span class="sxs-lookup"><span data-stu-id="56f8f-119">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="56f8f-120">Colonne</span><span class="sxs-lookup"><span data-stu-id="56f8f-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="56f8f-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="56f8f-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="56f8f-122">Chiave esterna nella prima colonna della [tabella file](file-table.md) che indica il modulo che deve essere registrato.</span><span class="sxs-lookup"><span data-stu-id="56f8f-122">External key into the first column of the [File table](file-table.md) indicating the module that needs to be registered.</span></span>

</dd> <dt>

<span data-ttu-id="56f8f-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Costo</span><span class="sxs-lookup"><span data-stu-id="56f8f-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="56f8f-124">Costo della registrazione del modulo in byte.</span><span class="sxs-lookup"><span data-stu-id="56f8f-124">The cost of registering the module in bytes.</span></span> <span data-ttu-id="56f8f-125">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="56f8f-125">This must be a non-negative number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56f8f-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="56f8f-126">Remarks</span></span>

<span data-ttu-id="56f8f-127">Gli autori dei pacchetti di installazione si sconsigliano vivamente di usare la registrazione automatica.</span><span class="sxs-lookup"><span data-stu-id="56f8f-127">Installation package authors are strongly advised against using self registration.</span></span> <span data-ttu-id="56f8f-128">Devono invece registrare i moduli creando una o più tabelle fornite dal programma di installazione per questo scopo.</span><span class="sxs-lookup"><span data-stu-id="56f8f-128">Instead they should register modules by authoring one or more tables provided by the installer for this purpose.</span></span> <span data-ttu-id="56f8f-129">Per ulteriori informazioni, vedere [gruppo di tabelle del registro di sistema](registry-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="56f8f-129">For more information, see [Registry Tables Group](registry-tables-group.md).</span></span> <span data-ttu-id="56f8f-130">Molti dei vantaggi derivanti dalla presenza di un servizio di installazione centrale vengono persi con la registrazione automatica perché le routine di registrazione automatica tendono a nascondere le informazioni di configurazione critiche.</span><span class="sxs-lookup"><span data-stu-id="56f8f-130">Many of the benefits of having a central installer service are lost with self registration because self-registration routines tend to hide critical configuration information.</span></span> <span data-ttu-id="56f8f-131">I motivi per evitare la registrazione automatica includono:</span><span class="sxs-lookup"><span data-stu-id="56f8f-131">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="56f8f-132">Il rollback di un'installazione con moduli autoregistrati non può essere eseguito in modo sicuro con [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) perché non esiste alcun modo per stabilire se le chiavi autoregistrate vengono usate da un'altra funzionalità o applicazione.</span><span class="sxs-lookup"><span data-stu-id="56f8f-132">Rollback of an installation with self-registered modules cannot be safely done using [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) because there is no way of telling if the self-registered keys are used by another feature or application.</span></span>
-   <span data-ttu-id="56f8f-133">La possibilità di usare l'annuncio è ridotta se la registrazione di classi o server di estensione viene eseguita in routine di registrazione automatica.</span><span class="sxs-lookup"><span data-stu-id="56f8f-133">The ability to use advertisement is reduced if Class or extension server registration is performed within self-registration routines.</span></span>
-   <span data-ttu-id="56f8f-134">Il programma di installazione gestisce automaticamente le chiavi di HKCR nelle tabelle del registro di sistema per le installazioni per utente o per computer.</span><span class="sxs-lookup"><span data-stu-id="56f8f-134">The installer automatically handles HKCR keys in the registry tables for both per-user or per-machine installations.</span></span> <span data-ttu-id="56f8f-135">Le routine [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) attualmente non supportano la nozione di chiave HKCR per utente.</span><span class="sxs-lookup"><span data-stu-id="56f8f-135">[**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) routines currently do not support the notion of a per-user HKCR key.</span></span>
-   <span data-ttu-id="56f8f-136">Se più utenti usano un'applicazione autoregistrata nello stesso computer, ogni utente deve installare l'applicazione la prima volta che la esegue.</span><span class="sxs-lookup"><span data-stu-id="56f8f-136">If multiple users are using a self-registered application on the same computer, each user must install the application the first time they run it.</span></span> <span data-ttu-id="56f8f-137">In caso contrario, il programma di installazione non è in grado di determinare facilmente le chiavi di registro HKCU appropriate</span><span class="sxs-lookup"><span data-stu-id="56f8f-137">Otherwise the installer cannot easily determine that the proper HKCU registry keys exist.</span></span>
-   <span data-ttu-id="56f8f-138">A [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) è possibile negare l'accesso alle risorse di rete, ad esempio le librerie dei tipi, se un componente viene specificato come Run-from-source ed è elencato nella tabella SelfReg.</span><span class="sxs-lookup"><span data-stu-id="56f8f-138">The [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) can be denied access to network resources such as type libraries if a component is both specified as run-from-source and is listed in the SelfReg table.</span></span> <span data-ttu-id="56f8f-139">Questa operazione può causare un errore di installazione del componente durante un'installazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="56f8f-139">This can cause the installation of the component to fail to during an administrative installation.</span></span>
-   <span data-ttu-id="56f8f-140">La registrazione automatica delle dll è più soggetta a errori di codifica perché il nuovo codice necessario per [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) è generalmente diverso per ogni dll.</span><span class="sxs-lookup"><span data-stu-id="56f8f-140">Self-registering DLLs are more susceptible to coding errors because the new code required for [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) is commonly different for each DLL.</span></span> <span data-ttu-id="56f8f-141">Usare invece le tabelle del registro di sistema nel database per sfruttare il codice esistente fornito dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="56f8f-141">Instead use the registry tables in the database to take advantage of existing code provided by the installer.</span></span>
-   <span data-ttu-id="56f8f-142">La registrazione automatica delle dll può talvolta essere collegata a DLL ausiliarie che non sono presenti o sono la versione sbagliata.</span><span class="sxs-lookup"><span data-stu-id="56f8f-142">Self-registering DLLs can sometimes link to auxiliary DLLs that are not present or are the wrong version.</span></span> <span data-ttu-id="56f8f-143">Al contrario, il programma di installazione può registrare le dll utilizzando le tabelle del registro di sistema senza dipendenze dallo stato corrente del sistema.</span><span class="sxs-lookup"><span data-stu-id="56f8f-143">In contrast, the installer can register the DLLs using the registry tables with no dependency on the current state of the system.</span></span>

> [!Note]  
> <span data-ttu-id="56f8f-144">Non è possibile specificare l'ordine in cui il programma di installazione registra o Annulla la registrazione delle dll con registrazione automatica usando le azioni [SelfRegModules](selfregmodules-action.md) e [SelfUnRegModules](selfunregmodules-action.md) .</span><span class="sxs-lookup"><span data-stu-id="56f8f-144">You cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="56f8f-145">Vedere [specifica dell'ordine di registrazione automatica](specifying-the-order-of-self-registration.md).</span><span class="sxs-lookup"><span data-stu-id="56f8f-145">See [Specifying the Order of Self Registration](specifying-the-order-of-self-registration.md).</span></span>

 

## <a name="validation"></a><span data-ttu-id="56f8f-146">Convalida</span><span class="sxs-lookup"><span data-stu-id="56f8f-146">Validation</span></span>

<dl>

[<span data-ttu-id="56f8f-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="56f8f-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="56f8f-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="56f8f-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="56f8f-149">ICE32</span><span class="sxs-lookup"><span data-stu-id="56f8f-149">ICE32</span></span>](ice32.md)  
</dl>

 

 
