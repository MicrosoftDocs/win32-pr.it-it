---
title: Classe Win32_RDMSCollectionProperties
description: Gestisce le proprietà di un insieme di desktop virtuali.
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSCollectionProperties Servizi Desktop remoto
- Classe Win32_RDMSCollectionProperties Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400519"
---
# <a name="win32_rdmscollectionproperties-class"></a><span data-ttu-id="0f2bd-105">Win32 \_ RDMSCollectionProperties (classe)</span><span class="sxs-lookup"><span data-stu-id="0f2bd-105">Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="0f2bd-106">Gestisce le proprietà di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-106">Manages the properties of a virtual desktop collection.</span></span>

<span data-ttu-id="0f2bd-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f2bd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f2bd-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a><span data-ttu-id="0f2bd-109">Members</span><span class="sxs-lookup"><span data-stu-id="0f2bd-109">Members</span></span>

<span data-ttu-id="0f2bd-110">La classe **Win32 \_ RDMSCollectionProperties** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0f2bd-110">The **Win32\_RDMSCollectionProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="0f2bd-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="0f2bd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="0f2bd-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0f2bd-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="0f2bd-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="0f2bd-113">Methods</span></span>

<span data-ttu-id="0f2bd-114">La classe **Win32 \_ RDMSCollectionProperties** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-114">The **Win32\_RDMSCollectionProperties** class has these methods.</span></span>



| <span data-ttu-id="0f2bd-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="0f2bd-115">Method</span></span>                                                                                        | <span data-ttu-id="0f2bd-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f2bd-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f2bd-117">**GetProvisioningProperties**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-117">**GetProvisioningProperties**</span></span>](getprovisioningproperties-win32-rdmscollectionproperties.md) | <span data-ttu-id="0f2bd-118">Recupera le proprietà di provisioning dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-118">Retrieves the provisioning properties of the virtual desktop collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0f2bd-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0f2bd-119">Properties</span></span>

<span data-ttu-id="0f2bd-120">La classe **Win32 \_ RDMSCollectionProperties** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-120">The **Win32\_RDMSCollectionProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f2bd-121">**Alias**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-121">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f2bd-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f2bd-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0f2bd-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f2bd-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0f2bd-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0f2bd-125">Ottiene l'alias della raccolta.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-125">Gets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="0f2bd-126">**ReferenceVirtualDesktopAdapters**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-126">**ReferenceVirtualDesktopAdapters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f2bd-127">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0f2bd-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0f2bd-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f2bd-129">Ottiene e imposta i nomi delle schede di rete virtuali della macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-129">Gets and sets the names of the virtual network adapters of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="0f2bd-130">**ReferenceVirtualDesktopArchitecture**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-130">**ReferenceVirtualDesktopArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f2bd-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f2bd-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0f2bd-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f2bd-133">Ottiene e imposta l'architettura del processore della macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-133">Gets and sets the processor architecture of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="0f2bd-134">**ReferenceVirtualDesktopGuid**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-134">**ReferenceVirtualDesktopGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f2bd-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f2bd-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0f2bd-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f2bd-137">Ottiene e imposta il GUID della macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-137">Gets and sets the GUID of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="0f2bd-138">**ReferenceVirtualDesktopHost**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-138">**ReferenceVirtualDesktopHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f2bd-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f2bd-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0f2bd-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f2bd-141">Ottiene e imposta il nome del server host della macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-141">Gets and sets the host server name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="0f2bd-142">**ReferenceVirtualDesktopMachineName**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-142">**ReferenceVirtualDesktopMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f2bd-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f2bd-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0f2bd-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f2bd-145">Ottiene e imposta il nome del computer della macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-145">Gets and sets the machine name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="0f2bd-146">**ReferenceVirtualDesktopName**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-146">**ReferenceVirtualDesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f2bd-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f2bd-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0f2bd-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f2bd-149">Ottiene e imposta il nome della macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-149">Gets and sets the name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="0f2bd-150">**ReferenceVirtualDesktopOsversion**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-150">**ReferenceVirtualDesktopOsversion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f2bd-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f2bd-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0f2bd-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f2bd-153">Ottiene e imposta la versione del sistema operativo della macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-153">Gets and sets the OS version of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="0f2bd-154">**ReferenceVirtualDesktopRamsizeMB**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-154">**ReferenceVirtualDesktopRamsizeMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f2bd-155">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f2bd-156">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0f2bd-156">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f2bd-157">Ottiene e imposta le dimensioni della memoria della macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-157">Gets and sets the memory size of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="0f2bd-158">**ReferenceVirtualDesktopRemoteFX**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-158">**ReferenceVirtualDesktopRemoteFX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f2bd-159">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0f2bd-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f2bd-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0f2bd-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f2bd-161">Ottiene e imposta un valore che indica se RemoteFX è abilitato per la macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-161">Gets and sets a value that indicates whether RemoteFX is enabled for the master VM.</span></span> <span data-ttu-id="0f2bd-162">**True** se RemoteFX è abilitato; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-162">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span> <span data-ttu-id="0f2bd-163">Il valore predefinito per questa proprietà è **false**.</span><span class="sxs-lookup"><span data-stu-id="0f2bd-163">The default value for this property is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f2bd-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f2bd-164">Requirements</span></span>



| <span data-ttu-id="0f2bd-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f2bd-165">Requirement</span></span> | <span data-ttu-id="0f2bd-166">Valore</span><span class="sxs-lookup"><span data-stu-id="0f2bd-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f2bd-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f2bd-167">Minimum supported client</span></span><br/> | <span data-ttu-id="0f2bd-168">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0f2bd-168">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0f2bd-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f2bd-169">Minimum supported server</span></span><br/> | <span data-ttu-id="0f2bd-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f2bd-170">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="0f2bd-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0f2bd-171">Namespace</span></span><br/>                | <span data-ttu-id="0f2bd-172">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="0f2bd-172">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0f2bd-173">MOF</span><span class="sxs-lookup"><span data-stu-id="0f2bd-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f2bd-174"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f2bd-174"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f2bd-175">DLL</span><span class="sxs-lookup"><span data-stu-id="0f2bd-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f2bd-176"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f2bd-176"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0f2bd-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f2bd-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f2bd-178">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="0f2bd-178">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

