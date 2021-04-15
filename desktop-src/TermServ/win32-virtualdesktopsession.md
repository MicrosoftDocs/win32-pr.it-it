---
title: Classe Win32_VirtualDesktopSession
description: Gestisce una sessione desktop virtuale.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Classe Win32_VirtualDesktopSession Servizi Desktop remoto
- Classe Win32_VirtualDesktopSession Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f343c1dc022dcb4759f813de956ade27e1aff213
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475449"
---
# <a name="win32_virtualdesktopsession-class"></a><span data-ttu-id="07ed2-105">Win32 \_ VirtualDesktopSession (classe)</span><span class="sxs-lookup"><span data-stu-id="07ed2-105">Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="07ed2-106">Gestisce una sessione desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="07ed2-106">Manages a virtual desktop session.</span></span>

<span data-ttu-id="07ed2-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="07ed2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="07ed2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07ed2-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a><span data-ttu-id="07ed2-109">Members</span><span class="sxs-lookup"><span data-stu-id="07ed2-109">Members</span></span>

<span data-ttu-id="07ed2-110">La classe **Win32 \_ VirtualDesktopSession** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="07ed2-110">The **Win32\_VirtualDesktopSession** class has these types of members:</span></span>

-   [<span data-ttu-id="07ed2-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="07ed2-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="07ed2-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07ed2-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="07ed2-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="07ed2-113">Methods</span></span>

<span data-ttu-id="07ed2-114">La classe **Win32 \_ VirtualDesktopSession** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="07ed2-114">The **Win32\_VirtualDesktopSession** class has these methods.</span></span>



| <span data-ttu-id="07ed2-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="07ed2-115">Method</span></span>                                                         | <span data-ttu-id="07ed2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07ed2-116">Description</span></span>                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="07ed2-117">**Disconnetti**</span><span class="sxs-lookup"><span data-stu-id="07ed2-117">**Disconnect**</span></span>](disconnect-win32-virtualdesktopsession.md)   | <span data-ttu-id="07ed2-118">Disconnette la sessione desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="07ed2-118">Disconnects the virtual desktop session.</span></span><br/>                        |
| [<span data-ttu-id="07ed2-119">**Disconnessione**</span><span class="sxs-lookup"><span data-stu-id="07ed2-119">**Logoff**</span></span>](logoff-win32-virtualdesktopsession.md)           | <span data-ttu-id="07ed2-120">Disconnette l'utente dalla sessione desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="07ed2-120">Logs off the user from the virtual desktop session.</span></span><br/>             |
| [<span data-ttu-id="07ed2-121">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="07ed2-121">**SendMessage**</span></span>](sendmessage-win32-virtualdesktopsession.md) | <span data-ttu-id="07ed2-122">Inviare un messaggio all'utente tramite la sessione desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="07ed2-122">Send a message to the user through the virtual desktop session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="07ed2-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07ed2-123">Properties</span></span>

<span data-ttu-id="07ed2-124">La classe **Win32 \_ VirtualDesktopSession** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="07ed2-124">The **Win32\_VirtualDesktopSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07ed2-125">**ClientMachineName**</span><span class="sxs-lookup"><span data-stu-id="07ed2-125">**ClientMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07ed2-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07ed2-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07ed2-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07ed2-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07ed2-128">Ottiene il nome del computer client connesso alla sessione.</span><span class="sxs-lookup"><span data-stu-id="07ed2-128">Gets the name of the client machine that is connected to the session.</span></span>

</dd> <dt>

<span data-ttu-id="07ed2-129">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="07ed2-129">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07ed2-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07ed2-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07ed2-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07ed2-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07ed2-132">Ottiene il nome dell'insieme di desktop virtuali che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="07ed2-132">Gets the name of the virtual desktop collection that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="07ed2-133">**ConnectState**</span><span class="sxs-lookup"><span data-stu-id="07ed2-133">**ConnectState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07ed2-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07ed2-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07ed2-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07ed2-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07ed2-136">Ottiene lo stato della connessione alla sessione.</span><span class="sxs-lookup"><span data-stu-id="07ed2-136">Gets the state of the connection to the session.</span></span>

</dd> <dt>

<span data-ttu-id="07ed2-137">**NomeDominio**</span><span class="sxs-lookup"><span data-stu-id="07ed2-137">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07ed2-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07ed2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07ed2-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07ed2-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07ed2-140">Ottiene il nome di dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="07ed2-140">Gets the domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="07ed2-141">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="07ed2-141">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07ed2-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07ed2-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07ed2-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07ed2-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07ed2-144">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="07ed2-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="07ed2-145">Ottiene l'ID della sessione desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="07ed2-145">Gets the ID of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="07ed2-146">**UserName**</span><span class="sxs-lookup"><span data-stu-id="07ed2-146">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07ed2-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07ed2-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07ed2-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07ed2-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07ed2-149">Ottiene il nome dell'account utente assegnato alla sessione.</span><span class="sxs-lookup"><span data-stu-id="07ed2-149">Gets the name of the user account that is assigned to the session.</span></span>

</dd> <dt>

<span data-ttu-id="07ed2-150">**VMHostName**</span><span class="sxs-lookup"><span data-stu-id="07ed2-150">**VMHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07ed2-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07ed2-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07ed2-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07ed2-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07ed2-153">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="07ed2-153">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="07ed2-154">Ottiene il nome del server host di virtualizzazione Desktop remoto che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="07ed2-154">Gets the name of the Remote Desktop virtualization host server that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="07ed2-155">**VMName**</span><span class="sxs-lookup"><span data-stu-id="07ed2-155">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07ed2-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07ed2-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07ed2-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07ed2-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07ed2-158">Ottiene il nome della macchina virtuale assegnata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="07ed2-158">Gets the name of the virtual machine that is assigned to the session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07ed2-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07ed2-159">Requirements</span></span>



| <span data-ttu-id="07ed2-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="07ed2-160">Requirement</span></span> | <span data-ttu-id="07ed2-161">Valore</span><span class="sxs-lookup"><span data-stu-id="07ed2-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="07ed2-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07ed2-162">Minimum supported client</span></span><br/> | <span data-ttu-id="07ed2-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07ed2-163">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="07ed2-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07ed2-164">Minimum supported server</span></span><br/> | <span data-ttu-id="07ed2-165">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="07ed2-165">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="07ed2-166">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07ed2-166">Namespace</span></span><br/>                | <span data-ttu-id="07ed2-167">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="07ed2-167">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="07ed2-168">MOF</span><span class="sxs-lookup"><span data-stu-id="07ed2-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07ed2-169"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07ed2-169"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="07ed2-170">DLL</span><span class="sxs-lookup"><span data-stu-id="07ed2-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07ed2-171"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07ed2-171"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="07ed2-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07ed2-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ed2-173">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="07ed2-173">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

