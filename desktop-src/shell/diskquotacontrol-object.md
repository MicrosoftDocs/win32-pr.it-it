---
description: Consente a un amministratore di gestire le proprietà della quota disco di un volume.
title: Oggetto DiskQuotaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 843f33ee79e70309a47f170bb1935f94f45c8f2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994901"
---
# <a name="diskquotacontrol-object"></a><span data-ttu-id="8bb88-103">Oggetto DiskQuotaControl</span><span class="sxs-lookup"><span data-stu-id="8bb88-103">DiskQuotaControl object</span></span>

<span data-ttu-id="8bb88-104">Consente a un amministratore di gestire le proprietà della quota disco di un volume.</span><span class="sxs-lookup"><span data-stu-id="8bb88-104">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="8bb88-105">Il file system NTFS consente a un amministratore di gestire l'utilizzo del disco in un volume condiviso allocando a ogni utente una quantità di spazio su disco specificata o un *limite di quota*.</span><span class="sxs-lookup"><span data-stu-id="8bb88-105">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or *quota limit*, to each user.</span></span> <span data-ttu-id="8bb88-106">È possibile utilizzare questo oggetto per impostare il limite di quota predefinito che verrà assegnato automaticamente a tutti i nuovi utenti.</span><span class="sxs-lookup"><span data-stu-id="8bb88-106">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span>

## <a name="members"></a><span data-ttu-id="8bb88-107">Membri</span><span class="sxs-lookup"><span data-stu-id="8bb88-107">Members</span></span>

<span data-ttu-id="8bb88-108">L'oggetto **DiskQuotaControl** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8bb88-108">The **DiskQuotaControl** object has these types of members:</span></span>

-   [<span data-ttu-id="8bb88-109">Eventi</span><span class="sxs-lookup"><span data-stu-id="8bb88-109">Events</span></span>](#events)
-   [<span data-ttu-id="8bb88-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="8bb88-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8bb88-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8bb88-111">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="8bb88-112">Eventi</span><span class="sxs-lookup"><span data-stu-id="8bb88-112">Events</span></span>

<span data-ttu-id="8bb88-113">L'oggetto **DiskQuotaControl** presenta questi eventi.</span><span class="sxs-lookup"><span data-stu-id="8bb88-113">The **DiskQuotaControl** object has these events.</span></span>



| <span data-ttu-id="8bb88-114">Event</span><span class="sxs-lookup"><span data-stu-id="8bb88-114">Event</span></span>                                                           | <span data-ttu-id="8bb88-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bb88-115">Description</span></span>                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bb88-116">**OnUserNameChanged**</span><span class="sxs-lookup"><span data-stu-id="8bb88-116">**OnUserNameChanged**</span></span>](diskquotacontrol-onusernamechanged.md) | <span data-ttu-id="8bb88-117">Si verifica quando sono state risolte le informazioni sul nome per un oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) .</span><span class="sxs-lookup"><span data-stu-id="8bb88-117">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="8bb88-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="8bb88-118">Methods</span></span>

<span data-ttu-id="8bb88-119">L'oggetto **DiskQuotaControl** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8bb88-119">The **DiskQuotaControl** object has these methods.</span></span>



| <span data-ttu-id="8bb88-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="8bb88-120">Method</span></span>                                                                                    | <span data-ttu-id="8bb88-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bb88-121">Description</span></span>                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bb88-122">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="8bb88-122">**AddUser**</span></span>](diskquotacontrol-adduser.md)                                               | <span data-ttu-id="8bb88-123">Assegna una quota disco non predefinita a un nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="8bb88-123">Assigns a nondefault disk quota to a new user.</span></span><br/>                                  |
| [<span data-ttu-id="8bb88-124">**DeleteUser**</span><span class="sxs-lookup"><span data-stu-id="8bb88-124">**DeleteUser**</span></span>](diskquotacontrol-deleteuser.md)                                         | <span data-ttu-id="8bb88-125">Elimina un utente dal volume.</span><span class="sxs-lookup"><span data-stu-id="8bb88-125">Deletes a user from the volume.</span></span><br/>                                                 |
| [<span data-ttu-id="8bb88-126">**FindUser**</span><span class="sxs-lookup"><span data-stu-id="8bb88-126">**FindUser**</span></span>](diskquotacontrol-finduser.md)                                             | <span data-ttu-id="8bb88-127">Trova la voce di un utente, in base al nome, nel file di quota del volume.</span><span class="sxs-lookup"><span data-stu-id="8bb88-127">Finds a user's entry, by name, in the volume's quota file.</span></span><br/>                      |
| [<span data-ttu-id="8bb88-128">**GiveUserNameResolutionPriority**</span><span class="sxs-lookup"><span data-stu-id="8bb88-128">**GiveUserNameResolutionPriority**</span></span>](diskquotacontrol-giveusernameresolutionpriority.md) | <span data-ttu-id="8bb88-129">Inserisce l'oggetto utente specificato accanto alla riga per la risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8bb88-129">Places the specified user object next in line for name resolution.</span></span><br/>              |
| [<span data-ttu-id="8bb88-130">**Inizializzare**</span><span class="sxs-lookup"><span data-stu-id="8bb88-130">**Initialize**</span></span>](diskquotacontrol-initialize.md)                                         | <span data-ttu-id="8bb88-131">Apre un volume specificato e inizializza il relativo oggetto di controllo della quota.</span><span class="sxs-lookup"><span data-stu-id="8bb88-131">Opens a specified volume and initializes its quota control object.</span></span><br/>              |
| [<span data-ttu-id="8bb88-132">**InvalidateSidNameCache**</span><span class="sxs-lookup"><span data-stu-id="8bb88-132">**InvalidateSidNameCache**</span></span>](diskquotacontrol-invalidatesidnamecache.md)                 | <span data-ttu-id="8bb88-133">Invalida la cache del nome utente dell'ID di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8bb88-133">Invalidates the security ID user name cache.</span></span><br/>                                    |
| [<span data-ttu-id="8bb88-134">**ShutdownNameResolution**</span><span class="sxs-lookup"><span data-stu-id="8bb88-134">**ShutdownNameResolution**</span></span>](diskquotacontrol-shutdownnameresolution.md)                 | <span data-ttu-id="8bb88-135">Arresta il thread di risoluzione del nome utente.</span><span class="sxs-lookup"><span data-stu-id="8bb88-135">Shuts down the user name resolution thread.</span></span><br/>                                     |
| [<span data-ttu-id="8bb88-136">**TranslateLogonNameToSID**</span><span class="sxs-lookup"><span data-stu-id="8bb88-136">**TranslateLogonNameToSID**</span></span>](diskquotacontrol-translatelogonnametosid.md)               | <span data-ttu-id="8bb88-137">Converte un nome di accesso nell'ID di sicurezza utente corrispondente in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="8bb88-137">Translates a logon name to the corresponding user security ID in string format.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8bb88-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8bb88-138">Properties</span></span>

<span data-ttu-id="8bb88-139">L'oggetto **DiskQuotaControl** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8bb88-139">The **DiskQuotaControl** object has these properties.</span></span>



| <span data-ttu-id="8bb88-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8bb88-140">Property</span></span>                                                                                   | <span data-ttu-id="8bb88-141">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="8bb88-141">Access type</span></span>           | <span data-ttu-id="8bb88-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bb88-142">Description</span></span>                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bb88-143">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="8bb88-143">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)<br/>                 | <span data-ttu-id="8bb88-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8bb88-144">Read/write</span></span><br/> | <span data-ttu-id="8bb88-145">Ottiene o imposta il limite di quota predefinito.</span><span class="sxs-lookup"><span data-stu-id="8bb88-145">Sets or gets the default quota limit.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="8bb88-146">**DefaultQuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="8bb88-146">**DefaultQuotaLimitText**</span></span>](diskquotacontrol-defaultquotalimittext.md)<br/>         | <span data-ttu-id="8bb88-147">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="8bb88-147">Read-only</span></span><br/>  | <span data-ttu-id="8bb88-148">Ottiene il limite di quota predefinito come stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="8bb88-148">Gets the default quota limit as a text string.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="8bb88-149">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="8bb88-149">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)<br/>         | <span data-ttu-id="8bb88-150">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8bb88-150">Read/write</span></span><br/> | <span data-ttu-id="8bb88-151">Ottiene o imposta la soglia di quota predefinita.</span><span class="sxs-lookup"><span data-stu-id="8bb88-151">Sets or gets the default quota threshold.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="8bb88-152">**DefaultQuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="8bb88-152">**DefaultQuotaThresholdText**</span></span>](diskquotacontrol-defaultquotathresholdtext.md)<br/> | <span data-ttu-id="8bb88-153">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="8bb88-153">Read-only</span></span><br/>  | <span data-ttu-id="8bb88-154">Ottiene la soglia di quota predefinita come stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="8bb88-154">Gets the default quota threshold as a text string.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="8bb88-155">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="8bb88-155">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)<br/>                         | <span data-ttu-id="8bb88-156">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8bb88-156">Read/write</span></span><br/> | <span data-ttu-id="8bb88-157">Imposta o ottiene un valore booleano che indica se verrà eseguita una voce del registro eventi di sistema quando un utente supera il limite di quota assegnato.</span><span class="sxs-lookup"><span data-stu-id="8bb88-157">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span><br/>     |
| [<span data-ttu-id="8bb88-158">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="8bb88-158">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)<br/>                 | <span data-ttu-id="8bb88-159">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8bb88-159">Read/write</span></span><br/> | <span data-ttu-id="8bb88-160">Imposta o ottiene un valore booleano che indica se verrà eseguita una voce del registro eventi di sistema quando un utente supera la soglia di quota assegnata.</span><span class="sxs-lookup"><span data-stu-id="8bb88-160">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span><br/> |
| [<span data-ttu-id="8bb88-161">**QuotaFileIncomplete**</span><span class="sxs-lookup"><span data-stu-id="8bb88-161">**QuotaFileIncomplete**</span></span>](diskquotacontrol-quotafileincomplete.md)<br/>             | <span data-ttu-id="8bb88-162">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="8bb88-162">Read-only</span></span><br/>  | <span data-ttu-id="8bb88-163">Ottiene un valore booleano che indica se il file di quota per il volume è completo.</span><span class="sxs-lookup"><span data-stu-id="8bb88-163">Gets a Boolean value that indicates whether the quota file for the volume is complete.</span></span><br/>                                                             |
| [<span data-ttu-id="8bb88-164">**QuotaFileRebuilding**</span><span class="sxs-lookup"><span data-stu-id="8bb88-164">**QuotaFileRebuilding**</span></span>](diskquotacontrol-quotafilerebuilding.md)<br/>             | <span data-ttu-id="8bb88-165">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="8bb88-165">Read-only</span></span><br/>  | <span data-ttu-id="8bb88-166">Ottiene un valore booleano che indica se il file di quota per il volume è attualmente in fase di ricompilazione.</span><span class="sxs-lookup"><span data-stu-id="8bb88-166">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span><br/>                                              |
| [<span data-ttu-id="8bb88-167">**QuotaState**</span><span class="sxs-lookup"><span data-stu-id="8bb88-167">**QuotaState**</span></span>](diskquotacontrol-quotastate.md)<br/>                               | <span data-ttu-id="8bb88-168">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8bb88-168">Read/write</span></span><br/> | <span data-ttu-id="8bb88-169">Imposta o ottiene lo stato delle quote disco del volume.</span><span class="sxs-lookup"><span data-stu-id="8bb88-169">Sets or gets the state of the volume's disk quotas.</span></span><br/>                                                                                                |
| [<span data-ttu-id="8bb88-170">**UserNameResolution**</span><span class="sxs-lookup"><span data-stu-id="8bb88-170">**UserNameResolution**</span></span>](diskquotacontrol-usernameresolution.md)<br/>               | <span data-ttu-id="8bb88-171">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="8bb88-171">Read/write</span></span><br/> | <span data-ttu-id="8bb88-172">Imposta o ottiene un valore che controlla la modalità di risoluzione dei SID utente nei nomi utente.</span><span class="sxs-lookup"><span data-stu-id="8bb88-172">Sets or gets a value that controls how user SID are resolved to user names.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="8bb88-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="8bb88-173">Remarks</span></span>

<span data-ttu-id="8bb88-174">Un amministratore può utilizzare l'oggetto **DiskQuotaControl** per eseguire una serie di attività, incluse le seguenti:</span><span class="sxs-lookup"><span data-stu-id="8bb88-174">An administrator can use the **DiskQuotaControl** object to do a number of tasks, including the following:</span></span>

-   <span data-ttu-id="8bb88-175">Abilitazione e disabilitazione del sistema di quota disco del volume.</span><span class="sxs-lookup"><span data-stu-id="8bb88-175">Enabling and disabling the volume's disk quota system.</span></span>
-   <span data-ttu-id="8bb88-176">Ottenere lo stato del sistema di quota nel volume.</span><span class="sxs-lookup"><span data-stu-id="8bb88-176">Obtaining the status of the quota system on the volume.</span></span>
-   <span data-ttu-id="8bb88-177">La negazione dello spazio su disco agli utenti supera il limite di quota.</span><span class="sxs-lookup"><span data-stu-id="8bb88-177">Denying disk space to users exceeding their quota limit.</span></span>
-   <span data-ttu-id="8bb88-178">Specifica della soglia di avviso e dei valori di limite di quota predefiniti che verranno assegnati ai nuovi utenti.</span><span class="sxs-lookup"><span data-stu-id="8bb88-178">Specifying the default warning threshold and quota limit values that will be assigned to new users.</span></span>
-   <span data-ttu-id="8bb88-179">Aggiunta e rimozione di utenti.</span><span class="sxs-lookup"><span data-stu-id="8bb88-179">Adding and removing users.</span></span>

<span data-ttu-id="8bb88-180">L'oggetto **DiskQuotaControl** consente di impostare i valori predefiniti globali per il volume per le proprietà, ad esempio i limiti di quota.</span><span class="sxs-lookup"><span data-stu-id="8bb88-180">The **DiskQuotaControl** object allows you to set global default values for the volume for properties such as quota limits.</span></span> <span data-ttu-id="8bb88-181">Tuttavia, ogni utente è rappresentato da un oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) che può essere usato per specificare le singole impostazioni di quota.</span><span class="sxs-lookup"><span data-stu-id="8bb88-181">However, each user is represented by a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to specify individual quota settings.</span></span>

<span data-ttu-id="8bb88-182">Sono disponibili diversi modi per ottenere un oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente:</span><span class="sxs-lookup"><span data-stu-id="8bb88-182">There are several ways to obtain a user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object:</span></span>

-   <span data-ttu-id="8bb88-183">Gli oggetti [**DIDiskQuotaUser**](didiskquotauser-object.md) per tutti gli utenti con quote nel volume vengono esposti come raccolta e possono essere enumerati.</span><span class="sxs-lookup"><span data-stu-id="8bb88-183">The [**DIDiskQuotaUser**](didiskquotauser-object.md) objects for all users with quotas on the volume are exposed as a collection, and can be enumerated.</span></span> <span data-ttu-id="8bb88-184">Per informazioni su come enumerare gli oggetti **DIDiskQuotaUser** , vedere **enumerazione degli utenti di quote disco** nella sezione Osservazioni di **DIDiskQuotaUser**.</span><span class="sxs-lookup"><span data-stu-id="8bb88-184">For a discussion of how to enumerate **DIDiskQuotaUser** objects, see **Enumerating Disk Quota Users** in the Remarks section of **DIDiskQuotaUser**.</span></span>
-   <span data-ttu-id="8bb88-185">Quando si aggiunge un nuovo utente, il metodo [**adduser**](diskquotacontrol-adduser.md) restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8bb88-185">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>
-   <span data-ttu-id="8bb88-186">Se si ha il nome dell'utente, il metodo [**FindUser**](diskquotacontrol-finduser.md) restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8bb88-186">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

<span data-ttu-id="8bb88-187">Questo oggetto rende disponibili le funzionalità essenziali dell'interfaccia IDiskQuotaControl per gli script e le applicazioni basate su Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8bb88-187">This object makes the essential functionality of the IDiskQuotaControl interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb88-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bb88-188">Requirements</span></span>



| <span data-ttu-id="8bb88-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bb88-189">Requirement</span></span> | <span data-ttu-id="8bb88-190">Valore</span><span class="sxs-lookup"><span data-stu-id="8bb88-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb88-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bb88-191">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb88-192">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8bb88-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8bb88-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bb88-193">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb88-194">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8bb88-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8bb88-195">DLL</span><span class="sxs-lookup"><span data-stu-id="8bb88-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bb88-196"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="8bb88-196"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb88-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bb88-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb88-198">**Oggetto Shell**</span><span class="sxs-lookup"><span data-stu-id="8bb88-198">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




