---
title: Interfaccia ITsSbResourcePluginStoreEx
description: Espone metodi che consentono ai plug-in di risorse di archiviare oggetti, ad esempio sessioni e destinazioni.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- Interfaccia ITsSbResourcePluginStoreEx Servizi Desktop remoto
- Interfaccia ITsSbResourcePluginStoreEx Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a192b90f38d9b306c59f275d1fed3933d5cbd56a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120182"
---
# <a name="itssbresourcepluginstoreex-interface"></a><span data-ttu-id="391a4-105">Interfaccia ITsSbResourcePluginStoreEx</span><span class="sxs-lookup"><span data-stu-id="391a4-105">ITsSbResourcePluginStoreEx interface</span></span>

<span data-ttu-id="391a4-106">Espone metodi che consentono ai plug-in di risorse di archiviare oggetti, ad esempio sessioni e destinazioni.</span><span class="sxs-lookup"><span data-stu-id="391a4-106">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span> <span data-ttu-id="391a4-107">Questi metodi aggiungono, eliminano ed eseguono query su questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="391a4-107">These methods add, delete, and query these objects.</span></span>

<span data-ttu-id="391a4-108">Questa interfaccia è disponibile solo in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato.</span><span class="sxs-lookup"><span data-stu-id="391a4-108">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="391a4-109">I metodi [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) e [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) dell'interfaccia [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) sono disponibili a partire da Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="391a4-109">The [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) and [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) methods of the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface are available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="391a4-110">Membri</span><span class="sxs-lookup"><span data-stu-id="391a4-110">Members</span></span>

<span data-ttu-id="391a4-111">L'interfaccia **ITsSbResourcePluginStoreEx** eredita da [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span><span class="sxs-lookup"><span data-stu-id="391a4-111">The **ITsSbResourcePluginStoreEx** interface inherits from [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span></span> <span data-ttu-id="391a4-112">**ITsSbResourcePluginStoreEx** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="391a4-112">**ITsSbResourcePluginStoreEx** also has these types of members:</span></span>

-   [<span data-ttu-id="391a4-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="391a4-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="391a4-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="391a4-114">Methods</span></span>

<span data-ttu-id="391a4-115">L'interfaccia **ITsSbResourcePluginStoreEx** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="391a4-115">The **ITsSbResourcePluginStoreEx** interface has these methods.</span></span>



| <span data-ttu-id="391a4-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="391a4-116">Method</span></span>                                                                                                            | <span data-ttu-id="391a4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="391a4-117">Description</span></span>                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="391a4-118">**AcquireTargetLock**</span><span class="sxs-lookup"><span data-stu-id="391a4-118">**AcquireTargetLock**</span></span>](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | <span data-ttu-id="391a4-119">Blocca una destinazione.</span><span class="sxs-lookup"><span data-stu-id="391a4-119">Locks a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="391a4-120">**AddEnvironmentToStore**</span><span class="sxs-lookup"><span data-stu-id="391a4-120">**AddEnvironmentToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | <span data-ttu-id="391a4-121">Aggiunge un ambiente all'archivio plug-in delle risorse.</span><span class="sxs-lookup"><span data-stu-id="391a4-121">Adds an environment to the resource plug-in store.</span></span><br/>                                                   |
| [<span data-ttu-id="391a4-122">**AddSessionToStore**</span><span class="sxs-lookup"><span data-stu-id="391a4-122">**AddSessionToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | <span data-ttu-id="391a4-123">Aggiunge una nuova sessione all'archivio plug-in della risorsa.</span><span class="sxs-lookup"><span data-stu-id="391a4-123">Adds a new session to the resource plug-in store.</span></span><br/>                                                    |
| [<span data-ttu-id="391a4-124">**AddTargetToStore**</span><span class="sxs-lookup"><span data-stu-id="391a4-124">**AddTargetToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | <span data-ttu-id="391a4-125">Aggiunge una destinazione all'archivio plug-in della risorsa.</span><span class="sxs-lookup"><span data-stu-id="391a4-125">Adds a target to the resource plug-in store.</span></span><br/>                                                         |
| [<span data-ttu-id="391a4-126">**DeleteTarget**</span><span class="sxs-lookup"><span data-stu-id="391a4-126">**DeleteTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | <span data-ttu-id="391a4-127">Elimina una destinazione.</span><span class="sxs-lookup"><span data-stu-id="391a4-127">Deletes a target.</span></span><br/>                                                                                    |
| [<span data-ttu-id="391a4-128">**EnumerateEnvironments**</span><span class="sxs-lookup"><span data-stu-id="391a4-128">**EnumerateEnvironments**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | <span data-ttu-id="391a4-129">Restituisce una matrice che contiene gli ambienti presenti nell'archivio di plug-in di risorse.</span><span class="sxs-lookup"><span data-stu-id="391a4-129">Returns an array that contains the environments present in the resource plug-in store.</span></span><br/>               |
| [<span data-ttu-id="391a4-130">**EnumerateFarms**</span><span class="sxs-lookup"><span data-stu-id="391a4-130">**EnumerateFarms**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | <span data-ttu-id="391a4-131">Enumera tutte le farm che sono state aggiunte all'archivio plug-in di risorse.</span><span class="sxs-lookup"><span data-stu-id="391a4-131">Enumerates all the farms that have been added to the resource plug-in store.</span></span><br/>                         |
| [<span data-ttu-id="391a4-132">**EnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="391a4-132">**EnumerateSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | <span data-ttu-id="391a4-133">Enumera un set specificato di sessioni.</span><span class="sxs-lookup"><span data-stu-id="391a4-133">Enumerates a specified set of sessions.</span></span><br/>                                                              |
| [<span data-ttu-id="391a4-134">**EnumerateTargets**</span><span class="sxs-lookup"><span data-stu-id="391a4-134">**EnumerateTargets**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | <span data-ttu-id="391a4-135">Restituisce una matrice che contiene le destinazioni specificate presenti nell'archivio di plug-in di risorse.</span><span class="sxs-lookup"><span data-stu-id="391a4-135">Returns an array that contains the specified targets that are present in the resource plug-in store.</span></span><br/> |
| [<span data-ttu-id="391a4-136">**GetFarmProperty**</span><span class="sxs-lookup"><span data-stu-id="391a4-136">**GetFarmProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | <span data-ttu-id="391a4-137">Recupera una proprietà di una farm.</span><span class="sxs-lookup"><span data-stu-id="391a4-137">Retrieves a property of a farm.</span></span><br/>                                                                      |
| [<span data-ttu-id="391a4-138">**QueryEnvironment**</span><span class="sxs-lookup"><span data-stu-id="391a4-138">**QueryEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | <span data-ttu-id="391a4-139">Restituisce l'oggetto ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="391a4-139">Returns the specified environment object.</span></span><br/>                                                            |
| [<span data-ttu-id="391a4-140">**QuerySessionBySessionId**</span><span class="sxs-lookup"><span data-stu-id="391a4-140">**QuerySessionBySessionId**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | <span data-ttu-id="391a4-141">Restituisce l'oggetto sessione con l'ID di sessione specificato.</span><span class="sxs-lookup"><span data-stu-id="391a4-141">Returns the session object that has the specified session ID.</span></span><br/>                                        |
| [<span data-ttu-id="391a4-142">**QueryTarget**</span><span class="sxs-lookup"><span data-stu-id="391a4-142">**QueryTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | <span data-ttu-id="391a4-143">Restituisce la destinazione con il nome di destinazione e il nome della farm specificati.</span><span class="sxs-lookup"><span data-stu-id="391a4-143">Returns the target that has the specified target name and farm name.</span></span><br/>                                 |
| [<span data-ttu-id="391a4-144">**ReleaseTargetLock**</span><span class="sxs-lookup"><span data-stu-id="391a4-144">**ReleaseTargetLock**</span></span>](itssbresourcepluginstoreex-releasetargetlock.md)                                         | <span data-ttu-id="391a4-145">Rilascia un blocco su una destinazione.</span><span class="sxs-lookup"><span data-stu-id="391a4-145">Releases a lock on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="391a4-146">**RemoveEnvironmentFromStore**</span><span class="sxs-lookup"><span data-stu-id="391a4-146">**RemoveEnvironmentFromStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | <span data-ttu-id="391a4-147">Rimuove l'ambiente specificato dall'archivio di plug-in di risorse.</span><span class="sxs-lookup"><span data-stu-id="391a4-147">Removes the specified environment from the resource plug-in store.</span></span><br/>                                   |
| [<span data-ttu-id="391a4-148">**SaveEnvironment**</span><span class="sxs-lookup"><span data-stu-id="391a4-148">**SaveEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | <span data-ttu-id="391a4-149">Salva un ambiente.</span><span class="sxs-lookup"><span data-stu-id="391a4-149">Saves an environment.</span></span><br/>                                                                                |
| [<span data-ttu-id="391a4-150">**SaveSession**</span><span class="sxs-lookup"><span data-stu-id="391a4-150">**SaveSession**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | <span data-ttu-id="391a4-151">Salva una sessione.</span><span class="sxs-lookup"><span data-stu-id="391a4-151">Saves a session.</span></span><br/>                                                                                     |
| [<span data-ttu-id="391a4-152">**SaveTarget**</span><span class="sxs-lookup"><span data-stu-id="391a4-152">**SaveTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | <span data-ttu-id="391a4-153">Salva una destinazione.</span><span class="sxs-lookup"><span data-stu-id="391a4-153">Saves a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="391a4-154">**SetEnvironmentProperty**</span><span class="sxs-lookup"><span data-stu-id="391a4-154">**SetEnvironmentProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | <span data-ttu-id="391a4-155">Imposta una proprietà in un ambiente.</span><span class="sxs-lookup"><span data-stu-id="391a4-155">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="391a4-156">**SetEnvironmentPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="391a4-156">**SetEnvironmentPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | <span data-ttu-id="391a4-157">Imposta una proprietà in un ambiente.</span><span class="sxs-lookup"><span data-stu-id="391a4-157">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="391a4-158">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="391a4-158">**SetSessionState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | <span data-ttu-id="391a4-159">Imposta lo stato di una sessione.</span><span class="sxs-lookup"><span data-stu-id="391a4-159">Sets the state of a session.</span></span><br/>                                                                         |
| [<span data-ttu-id="391a4-160">**SetTargetProperty**</span><span class="sxs-lookup"><span data-stu-id="391a4-160">**SetTargetProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | <span data-ttu-id="391a4-161">Imposta una proprietà in una destinazione.</span><span class="sxs-lookup"><span data-stu-id="391a4-161">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="391a4-162">**SetTargetPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="391a4-162">**SetTargetPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | <span data-ttu-id="391a4-163">Imposta una proprietà in una destinazione.</span><span class="sxs-lookup"><span data-stu-id="391a4-163">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="391a4-164">**SetTargetState**</span><span class="sxs-lookup"><span data-stu-id="391a4-164">**SetTargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | <span data-ttu-id="391a4-165">Imposta lo stato di una destinazione.</span><span class="sxs-lookup"><span data-stu-id="391a4-165">Sets the state of a target.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="391a4-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="391a4-166">Requirements</span></span>



| <span data-ttu-id="391a4-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="391a4-167">Requirement</span></span> | <span data-ttu-id="391a4-168">Valore</span><span class="sxs-lookup"><span data-stu-id="391a4-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="391a4-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="391a4-169">Minimum supported client</span></span><br/> | <span data-ttu-id="391a4-170">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="391a4-170">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="391a4-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="391a4-171">Minimum supported server</span></span><br/> | <span data-ttu-id="391a4-172">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="391a4-172">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="391a4-173">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="391a4-173">End of server support</span></span><br/>    | <span data-ttu-id="391a4-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="391a4-174">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="391a4-175">IID</span><span class="sxs-lookup"><span data-stu-id="391a4-175">IID</span></span><br/>                      | <span data-ttu-id="391a4-176">IID \_ ITsSbResourcePluginStoreEx è definito come 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="391a4-176">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="391a4-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="391a4-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="391a4-178">**ITsSbResourcePluginStore**</span><span class="sxs-lookup"><span data-stu-id="391a4-178">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[<span data-ttu-id="391a4-179">Interfacce di virtualizzazione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="391a4-179">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





