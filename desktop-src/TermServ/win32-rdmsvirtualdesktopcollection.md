---
title: Classe Win32_RDMSVirtualDesktopCollection
description: Crea e gestisce un insieme di desktop virtuali.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a6da0c13b6ab223afc7afe6e92039a5388c6204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301446"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="7221d-105">Win32 \_ RDMSVirtualDesktopCollection (classe)</span><span class="sxs-lookup"><span data-stu-id="7221d-105">Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="7221d-106">Crea e gestisce un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="7221d-106">Creates and manages a virtual desktop collection.</span></span>

<span data-ttu-id="7221d-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7221d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7221d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7221d-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a><span data-ttu-id="7221d-109">Members</span><span class="sxs-lookup"><span data-stu-id="7221d-109">Members</span></span>

<span data-ttu-id="7221d-110">La classe **Win32 \_ RDMSVirtualDesktopCollection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7221d-110">The **Win32\_RDMSVirtualDesktopCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="7221d-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="7221d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7221d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7221d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7221d-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="7221d-113">Methods</span></span>

<span data-ttu-id="7221d-114">La classe **Win32 \_ RDMSVirtualDesktopCollection** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7221d-114">The **Win32\_RDMSVirtualDesktopCollection** class has these methods.</span></span>



| <span data-ttu-id="7221d-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="7221d-115">Method</span></span>                                                                                            | <span data-ttu-id="7221d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7221d-116">Description</span></span>                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7221d-117">**AddVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="7221d-117">**AddVirtualDesktop**</span></span>](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="7221d-118">Aggiunge un desktop virtuale a un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="7221d-118">Adds a virtual desktop to a virtual desktop collection.</span></span><br/>                                                                              |
| [<span data-ttu-id="7221d-119">**CancelPatch**</span><span class="sxs-lookup"><span data-stu-id="7221d-119">**CancelPatch**</span></span>](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | <span data-ttu-id="7221d-120">Annulla un processo di provisioning degli aggiornamenti software per le macchine virtuali in un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="7221d-120">Cancels a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>                                 |
| [<span data-ttu-id="7221d-121">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="7221d-121">**GetInt32Property**</span></span>](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="7221d-122">Recupera un valore di proprietà Integer da un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="7221d-122">Retrieves an integer property value from a virtual desktop collection.</span></span><br/>                                                               |
| [<span data-ttu-id="7221d-123">**GetPatchProperties**</span><span class="sxs-lookup"><span data-stu-id="7221d-123">**GetPatchProperties**</span></span>](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | <span data-ttu-id="7221d-124">Recupera le proprietà di un processo di provisioning degli aggiornamenti software per le macchine virtuali in un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="7221d-124">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>             |
| [<span data-ttu-id="7221d-125">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="7221d-125">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="7221d-126">Recupera un valore della proprietà stringa da un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="7221d-126">Retrieves a string property value from a virtual desktop collection.</span></span><br/>                                                                 |
| [<span data-ttu-id="7221d-127">**ProvisioningEnumerateJobs**</span><span class="sxs-lookup"><span data-stu-id="7221d-127">**ProvisioningEnumerateJobs**</span></span>](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | <span data-ttu-id="7221d-128">Enumera i processi di provisioning del desktop virtuale per questo servizio.</span><span class="sxs-lookup"><span data-stu-id="7221d-128">Enumerates virtual desktop provisioning jobs for this service.</span></span><br/>                                                                       |
| [<span data-ttu-id="7221d-129">**ProvisioningJobCancel**</span><span class="sxs-lookup"><span data-stu-id="7221d-129">**ProvisioningJobCancel**</span></span>](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | <span data-ttu-id="7221d-130">Annulla un processo di provisioning di un desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="7221d-130">Cancels a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="7221d-131">**ProvisioningJobExecute**</span><span class="sxs-lookup"><span data-stu-id="7221d-131">**ProvisioningJobExecute**</span></span>](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | <span data-ttu-id="7221d-132">Esegue un processo di provisioning di desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="7221d-132">Runs a virtual desktop provisioning job.</span></span><br/>                                                                                             |
| [<span data-ttu-id="7221d-133">**ProvisioningJobGetReport**</span><span class="sxs-lookup"><span data-stu-id="7221d-133">**ProvisioningJobGetReport**</span></span>](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | <span data-ttu-id="7221d-134">Ottiene un report sullo stato di un processo di provisioning di un desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="7221d-134">Gets a report about the status of a virtual desktop provisioning job.</span></span><br/>                                                                |
| [<span data-ttu-id="7221d-135">**ProvisioningPrepJob**</span><span class="sxs-lookup"><span data-stu-id="7221d-135">**ProvisioningPrepJob**</span></span>](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | <span data-ttu-id="7221d-136">Consente di creare un processo di provisioning di desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="7221d-136">Creates a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="7221d-137">**RemoveVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="7221d-137">**RemoveVirtualDesktop**</span></span>](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | <span data-ttu-id="7221d-138">Rimuove un desktop virtuale da un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="7221d-138">Removes a virtual desktop from a virtual desktop collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="7221d-139">**SchedulePatch**</span><span class="sxs-lookup"><span data-stu-id="7221d-139">**SchedulePatch**</span></span>](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | <span data-ttu-id="7221d-140">Pianifica un processo di provisioning degli aggiornamenti software che installa gli aggiornamenti software nelle macchine virtuali in un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="7221d-140">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span><br/> |
| [<span data-ttu-id="7221d-141">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="7221d-141">**SetInt32Property**</span></span>](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="7221d-142">Aggiorna un valore della proprietà Integer di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="7221d-142">Updates an integer property value of a virtual desktop collection.</span></span><br/>                                                                   |
| [<span data-ttu-id="7221d-143">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="7221d-143">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="7221d-144">Aggiorna il valore della proprietà di una stringa di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="7221d-144">Updates a string property value of a virtual desktop collection.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="7221d-145">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7221d-145">Properties</span></span>

<span data-ttu-id="7221d-146">La classe **Win32 \_ RDMSVirtualDesktopCollection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7221d-146">The **Win32\_RDMSVirtualDesktopCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7221d-147">**Alias**</span><span class="sxs-lookup"><span data-stu-id="7221d-147">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7221d-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-149">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7221d-150">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7221d-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7221d-151">Ottiene o imposta l'alias della raccolta.</span><span class="sxs-lookup"><span data-stu-id="7221d-151">Gets or sets the alias of the collection</span></span>

</dd> <dt>

<span data-ttu-id="7221d-152">**CollectionDescription**</span><span class="sxs-lookup"><span data-stu-id="7221d-152">**CollectionDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7221d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7221d-155">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7221d-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7221d-156">Ottiene o imposta la descrizione della raccolta.</span><span class="sxs-lookup"><span data-stu-id="7221d-156">Gets or sets the description of the collection</span></span>

</dd> <dt>

<span data-ttu-id="7221d-157">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="7221d-157">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-158">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7221d-158">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7221d-159">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7221d-160">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7221d-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7221d-161">Ottiene o imposta una matrice di valori che specificano le icone per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="7221d-161">Gets or sets an array of values that specify icons for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="7221d-162">**IsHA**</span><span class="sxs-lookup"><span data-stu-id="7221d-162">**IsHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-163">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7221d-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-164">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7221d-165">Ottiene o imposta un valore che indica se la raccolta contiene macchine virtuali a disponibilità elevata.</span><span class="sxs-lookup"><span data-stu-id="7221d-165">Gets or sets a values that indicates whether the collection contains highly available VMs.</span></span> <span data-ttu-id="7221d-166">**True** se la raccolta contiene macchine virtuali a disponibilità elevata; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7221d-166">**TRUE** if the collection contains highly available VMs; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7221d-167">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="7221d-167">**IsManaged**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-168">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7221d-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7221d-170">Ottiene o imposta un valore che indica se l'insieme è gestito.</span><span class="sxs-lookup"><span data-stu-id="7221d-170">Gets or sets a value that indicates whether the collection is managed.</span></span> <span data-ttu-id="7221d-171">**True** se l'insieme è gestito; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7221d-171">**TRUE** if the collection is managed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7221d-172">**IsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="7221d-172">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-173">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7221d-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-174">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7221d-175">Ottiene o imposta un valore che indica se un utente è un amministratore di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7221d-175">Gets or sets a values that indicates whether a user is an administrator on a VM.</span></span> <span data-ttu-id="7221d-176">**True** se l'utente è un amministratore di una macchina virtuale. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7221d-176">**TRUE** if the user is an administrator on a VM; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7221d-177">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7221d-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7221d-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-179">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7221d-180">Ottiene o imposta il nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="7221d-180">Gets or sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="7221d-181">**RollbackEnabled**</span><span class="sxs-lookup"><span data-stu-id="7221d-181">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-182">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7221d-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-183">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7221d-184">Ottiene o imposta un valore che indica se è stato eseguito il rollback di una macchina virtuale con uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7221d-184">Gets or sets a values that indicates whether a VM was rolled with a VM snapshot.</span></span> <span data-ttu-id="7221d-185">**True** se è stato eseguito il rollback della macchina virtuale con uno snapshot della macchina virtuale. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7221d-185">**TRUE** if the VM was rolled with a VM snapshot; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7221d-186">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7221d-186">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7221d-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-188">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7221d-189">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7221d-189">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7221d-190">Ottiene o imposta un descrittore di sicurezza in formato SSDL che controlla l'accesso alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="7221d-190">Gets or sets an SSDL formated security descriptor that controls access to the collection.</span></span>

</dd> <dt>

<span data-ttu-id="7221d-191">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="7221d-191">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-192">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7221d-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-193">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-193">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7221d-194">Ottiene o imposta un valore che indica se la raccolta viene visualizzata in Servizi terminal Accesso Web (Accesso Web TS).</span><span class="sxs-lookup"><span data-stu-id="7221d-194">Gets or sets a values that indicates whether the collection is displayed in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="7221d-195">**True** per visualizzare la raccolta in accesso Web di Servizi terminal; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7221d-195">**TRUE** to display the collection in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7221d-196">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7221d-196">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-197">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7221d-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-198">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7221d-199">Ottiene o imposta un valore che indica il tipo di sessioni della macchina virtuale ospitate dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="7221d-199">Gets or sets a value that indicates the type of virtual machine sessions hosted by the collection.</span></span>

<span data-ttu-id="7221d-200">Questa proprietà contiene uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="7221d-200">This property contains one of the following values:</span></span>

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="7221d-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)</span><span class="sxs-lookup"><span data-stu-id="7221d-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7221d-202">Macchine virtuali temporanee.</span><span class="sxs-lookup"><span data-stu-id="7221d-202">Temporary virtual machines.</span></span>

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="7221d-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)</span><span class="sxs-lookup"><span data-stu-id="7221d-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7221d-204">Macchine virtuali create manualmente.</span><span class="sxs-lookup"><span data-stu-id="7221d-204">Manually created virtual machines.</span></span>

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="7221d-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)</span><span class="sxs-lookup"><span data-stu-id="7221d-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7221d-206">Macchine virtuali generate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7221d-206">Auto-generated virtual machines.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7221d-207">**UserVHDSetting**</span><span class="sxs-lookup"><span data-stu-id="7221d-207">**UserVHDSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7221d-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-209">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7221d-210">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7221d-210">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7221d-211">Ottiene o imposta l'impostazione VHD dei dati utente per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="7221d-211">Gets or sets the user data VHD setting for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="7221d-212">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="7221d-212">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7221d-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7221d-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7221d-214">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7221d-214">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7221d-215">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7221d-215">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7221d-216">Ottiene o imposta le impostazioni del desktop per le macchine virtuali nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="7221d-216">Gets or sets he desktop settings for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7221d-217">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7221d-217">Requirements</span></span>



| <span data-ttu-id="7221d-218">Requisito</span><span class="sxs-lookup"><span data-stu-id="7221d-218">Requirement</span></span> | <span data-ttu-id="7221d-219">Valore</span><span class="sxs-lookup"><span data-stu-id="7221d-219">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7221d-220">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7221d-220">Minimum supported client</span></span><br/> | <span data-ttu-id="7221d-221">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7221d-221">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7221d-222">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7221d-222">Minimum supported server</span></span><br/> | <span data-ttu-id="7221d-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7221d-223">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7221d-224">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7221d-224">Namespace</span></span><br/>                | <span data-ttu-id="7221d-225">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="7221d-225">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7221d-226">MOF</span><span class="sxs-lookup"><span data-stu-id="7221d-226">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7221d-227"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7221d-227"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7221d-228">DLL</span><span class="sxs-lookup"><span data-stu-id="7221d-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7221d-229"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7221d-229"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7221d-230">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7221d-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7221d-231">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="7221d-231">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

