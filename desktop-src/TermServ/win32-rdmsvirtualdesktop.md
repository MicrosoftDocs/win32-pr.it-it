---
title: Classe Win32_RDMSVirtualDesktop
description: Rappresenta un desktop virtuale.
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSVirtualDesktop Servizi Desktop remoto
- Classe Win32_RDMSVirtualDesktop Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301447"
---
# <a name="win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="0d9d2-105">Win32 \_ RDMSVirtualDesktop (classe)</span><span class="sxs-lookup"><span data-stu-id="0d9d2-105">Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="0d9d2-106">Rappresenta un desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-106">Represents a virtual desktop.</span></span>

<span data-ttu-id="0d9d2-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d9d2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d9d2-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a><span data-ttu-id="0d9d2-109">Members</span><span class="sxs-lookup"><span data-stu-id="0d9d2-109">Members</span></span>

<span data-ttu-id="0d9d2-110">La classe **Win32 \_ RDMSVirtualDesktop** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0d9d2-110">The **Win32\_RDMSVirtualDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="0d9d2-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="0d9d2-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="0d9d2-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d9d2-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0d9d2-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="0d9d2-113">Methods</span></span>

<span data-ttu-id="0d9d2-114">La classe **Win32 \_ RDMSVirtualDesktop** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-114">The **Win32\_RDMSVirtualDesktop** class has these methods.</span></span>



| <span data-ttu-id="0d9d2-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="0d9d2-115">Method</span></span>                                                                                              | <span data-ttu-id="0d9d2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d9d2-116">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d9d2-117">**GetUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-117">**GetUserAssignment**</span></span>](getuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="0d9d2-118">Recupera il nome utente e il nome di dominio dell'utente assegnato al desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-118">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span><br/> |
| [<span data-ttu-id="0d9d2-119">**GetVirtualDesktopAssignedToUser**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-119">**GetVirtualDesktopAssignedToUser**</span></span>](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | <span data-ttu-id="0d9d2-120">Recupera il desktop virtuale assegnato all'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-120">Retrieves the virtual desktop that is assigned to the specified user.</span></span><br/>                       |
| [<span data-ttu-id="0d9d2-121">**GetVirtualDesktopDetails**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-121">**GetVirtualDesktopDetails**</span></span>](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | <span data-ttu-id="0d9d2-122">Recupera le informazioni aggiuntive sul desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-122">Retrieves the additional information about the virtual desktop.</span></span><br/>                             |
| [<span data-ttu-id="0d9d2-123">**GetVirtualDesktopState**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-123">**GetVirtualDesktopState**</span></span>](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="0d9d2-124">Recupera lo stato del desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-124">Retrieves the state of the virtual desktop.</span></span><br/>                                                 |
| [<span data-ttu-id="0d9d2-125">**RemoveUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-125">**RemoveUserAssignment**</span></span>](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | <span data-ttu-id="0d9d2-126">Rimuove l'assegnazione utente dal desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-126">Removes the user assignment from the virtual desktop.</span></span><br/>                                       |
| [<span data-ttu-id="0d9d2-127">**SetUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-127">**SetUserAssignment**</span></span>](setuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="0d9d2-128">Assegna un desktop virtuale a un utente.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-128">Assigns a virtual desktop to a user.</span></span><br/>                                                        |
| [<span data-ttu-id="0d9d2-129">**SetVirtualDesktopState**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-129">**SetVirtualDesktopState**</span></span>](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="0d9d2-130">Aggiorna lo stato del desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-130">Updates the state of the virtual desktop.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="0d9d2-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d9d2-131">Properties</span></span>

<span data-ttu-id="0d9d2-132">La classe **Win32 \_ RDMSVirtualDesktop** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-132">The **Win32\_RDMSVirtualDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d9d2-133">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-133">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9d2-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d9d2-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-136">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0d9d2-136">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d9d2-137">Ottiene l'alias dell'insieme di desktop virtuali che gestisce la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-137">Gets the alias to the virtual desktop collection that manages the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0d9d2-138">**HostName**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-138">**HostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9d2-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d9d2-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d9d2-141">Ottiene il nome del computer che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-141">Gets the name of the machine that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0d9d2-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9d2-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d9d2-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-145">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0d9d2-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0d9d2-146">Ottiene il nome dell'oggetto della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-146">Gets the name of the of virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0d9d2-147">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-147">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9d2-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d9d2-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-150">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0d9d2-150">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d9d2-151">Ottiene lo stato della sessione desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-151">Gets the state of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="0d9d2-152">**SessionUserName**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-152">**SessionUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9d2-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d9d2-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-155">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0d9d2-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d9d2-156">Ottiene il nome utente dell'utente che ha eseguito l'accesso alla sessione desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-156">Gets the username of the user that is logged in to the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="0d9d2-157">**Status**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9d2-158">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d9d2-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d9d2-160">Ottiene lo stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-160">Gets the status of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0d9d2-161">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-161">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9d2-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d9d2-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-164">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0d9d2-164">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d9d2-165">Ottiene il nome di dominio dell'utente assegnato al desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-165">Gets the domain name of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="0d9d2-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9d2-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d9d2-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-169">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0d9d2-169">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d9d2-170">Ottiene il nome utente dell'utente assegnato al desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-170">Gets the username of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="0d9d2-171">**VMState**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-171">**VMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d9d2-172">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d9d2-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d9d2-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d9d2-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d9d2-174">Ottiene lo stato del desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d9d2-174">Gets the state of the virtual desktop.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d9d2-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d9d2-175">Requirements</span></span>



| <span data-ttu-id="0d9d2-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d9d2-176">Requirement</span></span> | <span data-ttu-id="0d9d2-177">Valore</span><span class="sxs-lookup"><span data-stu-id="0d9d2-177">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9d2-178">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d9d2-178">Minimum supported client</span></span><br/> | <span data-ttu-id="0d9d2-179">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0d9d2-179">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0d9d2-180">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d9d2-180">Minimum supported server</span></span><br/> | <span data-ttu-id="0d9d2-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d9d2-181">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="0d9d2-182">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d9d2-182">Namespace</span></span><br/>                | <span data-ttu-id="0d9d2-183">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="0d9d2-183">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0d9d2-184">MOF</span><span class="sxs-lookup"><span data-stu-id="0d9d2-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d9d2-185"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d9d2-185"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d9d2-186">DLL</span><span class="sxs-lookup"><span data-stu-id="0d9d2-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d9d2-187"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d9d2-187"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0d9d2-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d9d2-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d9d2-189">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="0d9d2-189">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

