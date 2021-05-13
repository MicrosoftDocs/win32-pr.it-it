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
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841552"
---
# <a name="diskquotacontrol-object"></a><span data-ttu-id="0d995-103">Oggetto DiskQuotaControl</span><span class="sxs-lookup"><span data-stu-id="0d995-103">DiskQuotaControl object</span></span>

<span data-ttu-id="0d995-104">Consente a un amministratore di gestire le proprietà della quota disco di un volume.</span><span class="sxs-lookup"><span data-stu-id="0d995-104">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="0d995-105">L'file system NTFS consente a un amministratore di gestire l'utilizzo del disco in un volume condiviso allocando una quantità specificata di spazio su disco, o limite di *quota,* a ogni utente.</span><span class="sxs-lookup"><span data-stu-id="0d995-105">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or *quota limit*, to each user.</span></span> <span data-ttu-id="0d995-106">È possibile usare questo oggetto per impostare il limite di quota predefinito che verrà assegnato automaticamente a tutti i nuovi utenti.</span><span class="sxs-lookup"><span data-stu-id="0d995-106">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span>

## <a name="members"></a><span data-ttu-id="0d995-107">Membri</span><span class="sxs-lookup"><span data-stu-id="0d995-107">Members</span></span>

<span data-ttu-id="0d995-108">**L'oggetto DiskQuotaControl** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0d995-108">The **DiskQuotaControl** object has these types of members:</span></span>

-   [<span data-ttu-id="0d995-109">Eventi</span><span class="sxs-lookup"><span data-stu-id="0d995-109">Events</span></span>](#events)
-   [<span data-ttu-id="0d995-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="0d995-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0d995-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d995-111">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="0d995-112">Eventi</span><span class="sxs-lookup"><span data-stu-id="0d995-112">Events</span></span>

<span data-ttu-id="0d995-113">**L'oggetto DiskQuotaControl** include questi eventi.</span><span class="sxs-lookup"><span data-stu-id="0d995-113">The **DiskQuotaControl** object has these events.</span></span>



| <span data-ttu-id="0d995-114">Event</span><span class="sxs-lookup"><span data-stu-id="0d995-114">Event</span></span>                                                           | <span data-ttu-id="0d995-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d995-115">Description</span></span>                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d995-116">**OnUserNameChanged**</span><span class="sxs-lookup"><span data-stu-id="0d995-116">**OnUserNameChanged**</span></span>](diskquotacontrol-onusernamechanged.md) | <span data-ttu-id="0d995-117">Si verifica quando le informazioni sul nome per [**un oggetto DIDiskQuotaUser**](didiskquotauser-object.md) sono state risolte.</span><span class="sxs-lookup"><span data-stu-id="0d995-117">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="0d995-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="0d995-118">Methods</span></span>

<span data-ttu-id="0d995-119">**L'oggetto DiskQuotaControl** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0d995-119">The **DiskQuotaControl** object has these methods.</span></span>



| <span data-ttu-id="0d995-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="0d995-120">Method</span></span>                                                                                    | <span data-ttu-id="0d995-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d995-121">Description</span></span>                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d995-122">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="0d995-122">**AddUser**</span></span>](diskquotacontrol-adduser.md)                                               | <span data-ttu-id="0d995-123">Assegna una quota disco non predefinita a un nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="0d995-123">Assigns a nondefault disk quota to a new user.</span></span><br/>                                  |
| [<span data-ttu-id="0d995-124">**DeleteUser**</span><span class="sxs-lookup"><span data-stu-id="0d995-124">**DeleteUser**</span></span>](diskquotacontrol-deleteuser.md)                                         | <span data-ttu-id="0d995-125">Elimina un utente dal volume.</span><span class="sxs-lookup"><span data-stu-id="0d995-125">Deletes a user from the volume.</span></span><br/>                                                 |
| [<span data-ttu-id="0d995-126">**FindUser**</span><span class="sxs-lookup"><span data-stu-id="0d995-126">**FindUser**</span></span>](diskquotacontrol-finduser.md)                                             | <span data-ttu-id="0d995-127">Trova la voce di un utente, in base al nome, nel file di quota del volume.</span><span class="sxs-lookup"><span data-stu-id="0d995-127">Finds a user's entry, by name, in the volume's quota file.</span></span><br/>                      |
| [<span data-ttu-id="0d995-128">**GiveUserNameResolutionPriority**</span><span class="sxs-lookup"><span data-stu-id="0d995-128">**GiveUserNameResolutionPriority**</span></span>](diskquotacontrol-giveusernameresolutionpriority.md) | <span data-ttu-id="0d995-129">Posiziona l'oggetto utente specificato nella riga successiva per la risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0d995-129">Places the specified user object next in line for name resolution.</span></span><br/>              |
| [<span data-ttu-id="0d995-130">**Inizializzare**</span><span class="sxs-lookup"><span data-stu-id="0d995-130">**Initialize**</span></span>](diskquotacontrol-initialize.md)                                         | <span data-ttu-id="0d995-131">Apre un volume specificato e inizializza il relativo oggetto di controllo della quota.</span><span class="sxs-lookup"><span data-stu-id="0d995-131">Opens a specified volume and initializes its quota control object.</span></span><br/>              |
| [<span data-ttu-id="0d995-132">**InvalidateSidNameCache**</span><span class="sxs-lookup"><span data-stu-id="0d995-132">**InvalidateSidNameCache**</span></span>](diskquotacontrol-invalidatesidnamecache.md)                 | <span data-ttu-id="0d995-133">Invalida la cache dei nomi utente dell'ID di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0d995-133">Invalidates the security ID user name cache.</span></span><br/>                                    |
| [<span data-ttu-id="0d995-134">**ShutdownNameResolution**</span><span class="sxs-lookup"><span data-stu-id="0d995-134">**ShutdownNameResolution**</span></span>](diskquotacontrol-shutdownnameresolution.md)                 | <span data-ttu-id="0d995-135">Arresta il thread di risoluzione dei nomi utente.</span><span class="sxs-lookup"><span data-stu-id="0d995-135">Shuts down the user name resolution thread.</span></span><br/>                                     |
| [<span data-ttu-id="0d995-136">**TranslateLogonNameToSID**</span><span class="sxs-lookup"><span data-stu-id="0d995-136">**TranslateLogonNameToSID**</span></span>](diskquotacontrol-translatelogonnametosid.md)               | <span data-ttu-id="0d995-137">Converte un nome di accesso nell'ID di sicurezza utente corrispondente in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="0d995-137">Translates a logon name to the corresponding user security ID in string format.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0d995-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d995-138">Properties</span></span>

<span data-ttu-id="0d995-139">**L'oggetto DiskQuotaControl** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0d995-139">The **DiskQuotaControl** object has these properties.</span></span>



| <span data-ttu-id="0d995-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d995-140">Property</span></span>                                                                                   | <span data-ttu-id="0d995-141">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="0d995-141">Access type</span></span>           | <span data-ttu-id="0d995-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d995-142">Description</span></span>                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d995-143">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="0d995-143">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)<br/>                 | <span data-ttu-id="0d995-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0d995-144">Read/write</span></span><br/> | <span data-ttu-id="0d995-145">Imposta o ottiene il limite di quota predefinito.</span><span class="sxs-lookup"><span data-stu-id="0d995-145">Sets or gets the default quota limit.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="0d995-146">**DefaultQuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="0d995-146">**DefaultQuotaLimitText**</span></span>](diskquotacontrol-defaultquotalimittext.md)<br/>         | <span data-ttu-id="0d995-147">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d995-147">Read-only</span></span><br/>  | <span data-ttu-id="0d995-148">Ottiene il limite di quota predefinito come stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="0d995-148">Gets the default quota limit as a text string.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="0d995-149">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="0d995-149">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)<br/>         | <span data-ttu-id="0d995-150">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0d995-150">Read/write</span></span><br/> | <span data-ttu-id="0d995-151">Imposta o ottiene la soglia di quota predefinita.</span><span class="sxs-lookup"><span data-stu-id="0d995-151">Sets or gets the default quota threshold.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="0d995-152">**DefaultQuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="0d995-152">**DefaultQuotaThresholdText**</span></span>](diskquotacontrol-defaultquotathresholdtext.md)<br/> | <span data-ttu-id="0d995-153">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d995-153">Read-only</span></span><br/>  | <span data-ttu-id="0d995-154">Ottiene la soglia di quota predefinita come stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="0d995-154">Gets the default quota threshold as a text string.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="0d995-155">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="0d995-155">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)<br/>                         | <span data-ttu-id="0d995-156">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0d995-156">Read/write</span></span><br/> | <span data-ttu-id="0d995-157">Imposta o ottiene un valore booleano che indica se verrà effettuata una voce del registro eventi di sistema quando un utente supera il limite di quota assegnato.</span><span class="sxs-lookup"><span data-stu-id="0d995-157">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span><br/>     |
| [<span data-ttu-id="0d995-158">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="0d995-158">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)<br/>                 | <span data-ttu-id="0d995-159">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0d995-159">Read/write</span></span><br/> | <span data-ttu-id="0d995-160">Imposta o ottiene un valore booleano che indica se verrà effettuata una voce del registro eventi di sistema quando un utente supera la soglia di quota assegnata.</span><span class="sxs-lookup"><span data-stu-id="0d995-160">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span><br/> |
| [<span data-ttu-id="0d995-161">**QuotaFileIncomplete**</span><span class="sxs-lookup"><span data-stu-id="0d995-161">**QuotaFileIncomplete**</span></span>](diskquotacontrol-quotafileincomplete.md)<br/>             | <span data-ttu-id="0d995-162">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d995-162">Read-only</span></span><br/>  | <span data-ttu-id="0d995-163">Ottiene un valore booleano che indica se il file di quota per il volume è completo.</span><span class="sxs-lookup"><span data-stu-id="0d995-163">Gets a Boolean value that indicates whether the quota file for the volume is complete.</span></span><br/>                                                             |
| [<span data-ttu-id="0d995-164">**QuotaFileRebuilding**</span><span class="sxs-lookup"><span data-stu-id="0d995-164">**QuotaFileRebuilding**</span></span>](diskquotacontrol-quotafilerebuilding.md)<br/>             | <span data-ttu-id="0d995-165">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d995-165">Read-only</span></span><br/>  | <span data-ttu-id="0d995-166">Ottiene un valore booleano che indica se è in corso la ricompila del file di quota per il volume.</span><span class="sxs-lookup"><span data-stu-id="0d995-166">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span><br/>                                              |
| [<span data-ttu-id="0d995-167">**QuotaState**</span><span class="sxs-lookup"><span data-stu-id="0d995-167">**QuotaState**</span></span>](diskquotacontrol-quotastate.md)<br/>                               | <span data-ttu-id="0d995-168">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0d995-168">Read/write</span></span><br/> | <span data-ttu-id="0d995-169">Imposta o ottiene lo stato delle quote disco del volume.</span><span class="sxs-lookup"><span data-stu-id="0d995-169">Sets or gets the state of the volume's disk quotas.</span></span><br/>                                                                                                |
| [<span data-ttu-id="0d995-170">**UserNameResolution**</span><span class="sxs-lookup"><span data-stu-id="0d995-170">**UserNameResolution**</span></span>](diskquotacontrol-usernameresolution.md)<br/>               | <span data-ttu-id="0d995-171">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0d995-171">Read/write</span></span><br/> | <span data-ttu-id="0d995-172">Imposta o ottiene un valore che controlla la modalità di risoluzione del SID dell'utente nei nomi utente.</span><span class="sxs-lookup"><span data-stu-id="0d995-172">Sets or gets a value that controls how user SID are resolved to user names.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="0d995-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d995-173">Remarks</span></span>

<span data-ttu-id="0d995-174">Un amministratore può usare **l'oggetto DiskQuotaControl** per eseguire una serie di attività, tra cui:</span><span class="sxs-lookup"><span data-stu-id="0d995-174">An administrator can use the **DiskQuotaControl** object to do a number of tasks, including the following:</span></span>

-   <span data-ttu-id="0d995-175">Abilitazione e disabilitazione del sistema di quota disco del volume.</span><span class="sxs-lookup"><span data-stu-id="0d995-175">Enabling and disabling the volume's disk quota system.</span></span>
-   <span data-ttu-id="0d995-176">Recupero dello stato del sistema di quote nel volume.</span><span class="sxs-lookup"><span data-stu-id="0d995-176">Obtaining the status of the quota system on the volume.</span></span>
-   <span data-ttu-id="0d995-177">Negazione dello spazio su disco agli utenti che superano il limite di quota.</span><span class="sxs-lookup"><span data-stu-id="0d995-177">Denying disk space to users exceeding their quota limit.</span></span>
-   <span data-ttu-id="0d995-178">Specifica dei valori predefiniti di soglia di avviso e limite di quota che verranno assegnati ai nuovi utenti.</span><span class="sxs-lookup"><span data-stu-id="0d995-178">Specifying the default warning threshold and quota limit values that will be assigned to new users.</span></span>
-   <span data-ttu-id="0d995-179">Aggiunta e rimozione di utenti.</span><span class="sxs-lookup"><span data-stu-id="0d995-179">Adding and removing users.</span></span>

<span data-ttu-id="0d995-180">**L'oggetto DiskQuotaControl** consente di impostare i valori predefiniti globali per il volume per proprietà quali i limiti di quota.</span><span class="sxs-lookup"><span data-stu-id="0d995-180">The **DiskQuotaControl** object allows you to set global default values for the volume for properties such as quota limits.</span></span> <span data-ttu-id="0d995-181">Tuttavia, ogni utente è rappresentato da un [**oggetto DIDiskQuotaUser**](didiskquotauser-object.md) che può essere usato per specificare singole impostazioni di quota.</span><span class="sxs-lookup"><span data-stu-id="0d995-181">However, each user is represented by a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to specify individual quota settings.</span></span>

<span data-ttu-id="0d995-182">Esistono diversi modi per ottenere l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) di un utente:</span><span class="sxs-lookup"><span data-stu-id="0d995-182">There are several ways to obtain a user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object:</span></span>

-   <span data-ttu-id="0d995-183">Gli [**oggetti DIDiskQuotaUser**](didiskquotauser-object.md) per tutti gli utenti con quote nel volume vengono esposti come raccolta e possono essere enumerati.</span><span class="sxs-lookup"><span data-stu-id="0d995-183">The [**DIDiskQuotaUser**](didiskquotauser-object.md) objects for all users with quotas on the volume are exposed as a collection, and can be enumerated.</span></span> <span data-ttu-id="0d995-184">Per informazioni su come enumerare **gli oggetti DIDiskQuotaUser,** vedere Enumerazione degli utenti della **quota** del disco nella sezione Osservazioni di **DIDiskQuotaUser.**</span><span class="sxs-lookup"><span data-stu-id="0d995-184">For a discussion of how to enumerate **DIDiskQuotaUser** objects, see **Enumerating Disk Quota Users** in the Remarks section of **DIDiskQuotaUser**.</span></span>
-   <span data-ttu-id="0d995-185">Quando si aggiunge un nuovo utente, il [**metodo AddUser**](diskquotacontrol-adduser.md) restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0d995-185">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>
-   <span data-ttu-id="0d995-186">Se si ha il nome dell'utente, il [**metodo FindUser**](diskquotacontrol-finduser.md) restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0d995-186">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

<span data-ttu-id="0d995-187">Questo oggetto rende disponibili le funzionalità essenziali dell'interfaccia IDiskQuotaControl per gli script e le applicazioni basate Visual Basic Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0d995-187">This object makes the essential functionality of the IDiskQuotaControl interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d995-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d995-188">Requirements</span></span>



| <span data-ttu-id="0d995-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d995-189">Requirement</span></span> | <span data-ttu-id="0d995-190">Valore</span><span class="sxs-lookup"><span data-stu-id="0d995-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d995-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d995-191">Minimum supported client</span></span><br/> | <span data-ttu-id="0d995-192">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d995-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d995-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d995-193">Minimum supported server</span></span><br/> | <span data-ttu-id="0d995-194">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d995-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0d995-195">DLL</span><span class="sxs-lookup"><span data-stu-id="0d995-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d995-196"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="0d995-196"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d995-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d995-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d995-198">**Oggetto shell**</span><span class="sxs-lookup"><span data-stu-id="0d995-198">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




