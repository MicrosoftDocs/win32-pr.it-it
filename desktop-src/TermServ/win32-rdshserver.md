---
title: Classe Win32_RDSHServer
description: Gestisce un server host sessione Desktop remoto (RDSH).
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDSHServer Servizi Desktop remoto
- Classe Win32_RDSHServer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340722"
---
# <a name="win32_rdshserver-class"></a><span data-ttu-id="a0b01-105">Win32 \_ RDSHServer (classe)</span><span class="sxs-lookup"><span data-stu-id="a0b01-105">Win32\_RDSHServer class</span></span>

<span data-ttu-id="a0b01-106">Gestisce un server host sessione Desktop remoto (RDSH).</span><span class="sxs-lookup"><span data-stu-id="a0b01-106">Manages a Remote Desktop Session Host (RDSH) server.</span></span>

<span data-ttu-id="a0b01-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a0b01-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b01-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0b01-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a><span data-ttu-id="a0b01-109">Members</span><span class="sxs-lookup"><span data-stu-id="a0b01-109">Members</span></span>

<span data-ttu-id="a0b01-110">La classe **Win32 \_ RDSHServer** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a0b01-110">The **Win32\_RDSHServer** class has these types of members:</span></span>

-   [<span data-ttu-id="a0b01-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a0b01-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0b01-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a0b01-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a0b01-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="a0b01-113">Methods</span></span>

<span data-ttu-id="a0b01-114">La classe **Win32 \_ RDSHServer** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a0b01-114">The **Win32\_RDSHServer** class has these methods.</span></span>



| <span data-ttu-id="a0b01-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="a0b01-115">Method</span></span>                                                                          | <span data-ttu-id="a0b01-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0b01-116">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0b01-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="a0b01-117">**GetInt32Property**</span></span>](getint32property-win32-rdshserver.md)                   | <span data-ttu-id="a0b01-118">Recupera un valore di proprietà Integer di un oggetto **Win32 \_ RDSHServer** .</span><span class="sxs-lookup"><span data-stu-id="a0b01-118">Retrieves an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="a0b01-119">**GetPendingStartServerList**</span><span class="sxs-lookup"><span data-stu-id="a0b01-119">**GetPendingStartServerList**</span></span>](win32-rdshserver-getpendingstartserverlist.md) | <span data-ttu-id="a0b01-120">Recupera un elenco di server in attesa di avvio.</span><span class="sxs-lookup"><span data-stu-id="a0b01-120">Retrieves a list of server waiting to start.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="a0b01-121">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="a0b01-121">**GetStringProperty**</span></span>](getstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="a0b01-122">Recupera un valore della proprietà di stringa di un oggetto **Win32 \_ RDSHServer** .</span><span class="sxs-lookup"><span data-stu-id="a0b01-122">Retrieves a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="a0b01-123">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="a0b01-123">**SetInt32Property**</span></span>](setint32property-win32-rdshserver.md)                   | <span data-ttu-id="a0b01-124">Aggiorna un valore della proprietà Integer di un oggetto **Win32 \_ RDSHServer** .</span><span class="sxs-lookup"><span data-stu-id="a0b01-124">Updates an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="a0b01-125">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="a0b01-125">**SetStringProperty**</span></span>](setstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="a0b01-126">Aggiorna il valore di una proprietà di stringa di un oggetto **Win32 \_ RDSHServer** .</span><span class="sxs-lookup"><span data-stu-id="a0b01-126">Updates a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="a0b01-127">**TestAndSetState**</span><span class="sxs-lookup"><span data-stu-id="a0b01-127">**TestAndSetState**</span></span>](win32-rdshserver-testandsetstate.md)                     | <span data-ttu-id="a0b01-128">Confronta lo stato corrente con il comparand specificato. Se le due corrispondenze, lo stato viene impostato su un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="a0b01-128">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="a0b01-129">Indipendentemente dalla corrispondenza, viene restituito anche lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="a0b01-129">Regardless of the match, the current state is also returned.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a0b01-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a0b01-130">Properties</span></span>

<span data-ttu-id="a0b01-131">La classe **Win32 \_ RDSHServer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a0b01-131">The **Win32\_RDSHServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0b01-132">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="a0b01-132">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b01-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0b01-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b01-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0b01-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a0b01-135">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0b01-135">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0b01-136">Ottiene e imposta l'alias della raccolta RDSH a cui è assegnato il server RDSH.</span><span class="sxs-lookup"><span data-stu-id="a0b01-136">Gets and sets the alias to the RDSH collection to which the RDSH server is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="a0b01-137">**ConnectionBroker**</span><span class="sxs-lookup"><span data-stu-id="a0b01-137">**ConnectionBroker**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b01-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0b01-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b01-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0b01-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a0b01-140">Ottiene e imposta il nome del broker di Connessione Desktop remoto (RDCB) che gestisce l'accesso degli utenti al server RDSH.</span><span class="sxs-lookup"><span data-stu-id="a0b01-140">Gets and sets the name of the Remote Desktop Connection Broker (RDCB) that manages user access to the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="a0b01-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a0b01-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b01-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0b01-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0b01-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0b01-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a0b01-144">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a0b01-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a0b01-145">Ottiene e imposta il nome del server RDSH.</span><span class="sxs-lookup"><span data-stu-id="a0b01-145">Gets and sets the name of the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="a0b01-146">**ServerState**</span><span class="sxs-lookup"><span data-stu-id="a0b01-146">**ServerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0b01-147">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0b01-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0b01-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0b01-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0b01-149">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0b01-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0b01-150">Descrive lo stato del server.</span><span class="sxs-lookup"><span data-stu-id="a0b01-150">Describes the state of the server.</span></span> <span data-ttu-id="a0b01-151">Qualsiasi valore diverso da **target \_ Running** (3) è riservato e deve essere considerato uno stato non valido.</span><span class="sxs-lookup"><span data-stu-id="a0b01-151">Any value other than **TARGET\_RUNNING** (3) is reserved and should be consider an invalid state.</span></span>

<span data-ttu-id="a0b01-152">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="a0b01-152">The possible values are.</span></span>

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

<span data-ttu-id="a0b01-153">**Destinazione \_ SCONOSCIUTO** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b01-153">**TARGET\_UNKNOWN** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

<span data-ttu-id="a0b01-154">**Destinazione \_ IN esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b01-154">**TARGET\_RUNNING** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

<span data-ttu-id="a0b01-155">**Destinazione \_ NON valido** (8)</span><span class="sxs-lookup"><span data-stu-id="a0b01-155">**TARGET\_INVALID** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

<span data-ttu-id="a0b01-156">**Destinazione \_ INIZIO** (9)</span><span class="sxs-lookup"><span data-stu-id="a0b01-156">**TARGET\_STARTING** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

<span data-ttu-id="a0b01-157">**Destinazione \_ ARRESTO** in corso (10)</span><span class="sxs-lookup"><span data-stu-id="a0b01-157">**TARGET\_STOPPING** (10)</span></span>


<span data-ttu-id="a0b01-158"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a0b01-158"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="a0b01-159">**Windows server 2012 R2 e Windows server 2012:** Questa proprietà non è disponibile prima di Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a0b01-159">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0b01-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0b01-160">Requirements</span></span>



| <span data-ttu-id="a0b01-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0b01-161">Requirement</span></span> | <span data-ttu-id="a0b01-162">Valore</span><span class="sxs-lookup"><span data-stu-id="a0b01-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b01-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0b01-163">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b01-164">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a0b01-164">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a0b01-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0b01-165">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b01-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0b01-166">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a0b01-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a0b01-167">Namespace</span></span><br/>                | <span data-ttu-id="a0b01-168">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="a0b01-168">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a0b01-169">MOF</span><span class="sxs-lookup"><span data-stu-id="a0b01-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0b01-170"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0b01-170"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0b01-171">DLL</span><span class="sxs-lookup"><span data-stu-id="a0b01-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0b01-172"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0b01-172"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a0b01-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0b01-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b01-174">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="a0b01-174">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

