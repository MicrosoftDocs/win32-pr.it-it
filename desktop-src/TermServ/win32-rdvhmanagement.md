---
title: Classe Win32_RdvhManagement
description: Viene descritto un servizio di gestione di Desktop remoto host virtuale (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Classe Win32_RdvhManagement Servizi Desktop remoto
- Classe Win32_RdvhManagement Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301741"
---
# <a name="win32_rdvhmanagement-class"></a><span data-ttu-id="70a62-105">Win32 \_ RdvhManagement (classe)</span><span class="sxs-lookup"><span data-stu-id="70a62-105">Win32\_RdvhManagement class</span></span>

<span data-ttu-id="70a62-106">Viene descritto un servizio di gestione di Desktop remoto host virtuale (RDVH).</span><span class="sxs-lookup"><span data-stu-id="70a62-106">Describes a Remote Desktop Virtual Host (RDVH) management service.</span></span>

<span data-ttu-id="70a62-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="70a62-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a62-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70a62-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a><span data-ttu-id="70a62-109">Members</span><span class="sxs-lookup"><span data-stu-id="70a62-109">Members</span></span>

<span data-ttu-id="70a62-110">La classe **Win32 \_ RdvhManagement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="70a62-110">The **Win32\_RdvhManagement** class has these types of members:</span></span>

-   [<span data-ttu-id="70a62-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="70a62-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="70a62-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="70a62-112">Methods</span></span>

<span data-ttu-id="70a62-113">La classe **Win32 \_ RdvhManagement** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="70a62-113">The **Win32\_RdvhManagement** class has these methods.</span></span>



| <span data-ttu-id="70a62-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="70a62-114">Method</span></span>                                                                                  | <span data-ttu-id="70a62-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70a62-115">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70a62-116">**RdvCreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="70a62-116">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="70a62-117">Crea il modello di disco utente della dimensione massima specificata e nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="70a62-117">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="70a62-118">Tutti i dischi utente creati avranno dimensioni massime corrispondenti alle dimensioni massime del modello.</span><span class="sxs-lookup"><span data-stu-id="70a62-118">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="70a62-119">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="70a62-119">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="70a62-120">Avvia una migrazione in tempo reale della macchina virtuale in scenari VDI</span><span class="sxs-lookup"><span data-stu-id="70a62-120">Initiates a live migration of virtual machine in VDI scenarios</span></span><br/>                                                                                               |
| [<span data-ttu-id="70a62-121">**RdvCopyBaseVmLocally**</span><span class="sxs-lookup"><span data-stu-id="70a62-121">**RdvCopyBaseVmLocally**</span></span>](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | <span data-ttu-id="70a62-122">Copia il percorso della macchina virtuale di base localmente nel server Host di virtualizzazione DR</span><span class="sxs-lookup"><span data-stu-id="70a62-122">Copies Base VM location locally to RDV Host server</span></span><br/>                                                                                                           |
| [<span data-ttu-id="70a62-123">**RdvCreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="70a62-123">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="70a62-124">Crea il modello di disco utente della dimensione massima specificata e nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="70a62-124">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="70a62-125">Tutti i dischi utente creati avranno dimensioni massime corrispondenti alle dimensioni massime del modello.</span><span class="sxs-lookup"><span data-stu-id="70a62-125">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="70a62-126">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="70a62-126">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="70a62-127">Avvia una migrazione in tempo reale di una macchina virtuale in scenari VDI.</span><span class="sxs-lookup"><span data-stu-id="70a62-127">Initiates a live migration of virtual machine in VDI scenarios.</span></span><br/>                                                                                              |
| [<span data-ttu-id="70a62-128">**RdvSetupVMPermissions**</span><span class="sxs-lookup"><span data-stu-id="70a62-128">**RdvSetupVMPermissions**</span></span>](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | <span data-ttu-id="70a62-129">Imposta le autorizzazioni nella macchina virtuale per il chiamante</span><span class="sxs-lookup"><span data-stu-id="70a62-129">Sets permissions in VM for the caller</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="70a62-130">**RdvUndoVMPermissions**</span><span class="sxs-lookup"><span data-stu-id="70a62-130">**RdvUndoVMPermissions**</span></span>](rdvundovmpermissions-win32-rdvhmanagement.md)               | <span data-ttu-id="70a62-131">Ripristina le autorizzazioni in una macchina virtuale impostata da RdvSetupVMPermissions</span><span class="sxs-lookup"><span data-stu-id="70a62-131">Reverts permissions in VM set by RdvSetupVMPermissions</span></span><br/>                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="70a62-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70a62-132">Requirements</span></span>



| <span data-ttu-id="70a62-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a62-133">Requirement</span></span> | <span data-ttu-id="70a62-134">Valore</span><span class="sxs-lookup"><span data-stu-id="70a62-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a62-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70a62-135">Minimum supported client</span></span><br/> | <span data-ttu-id="70a62-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="70a62-136">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="70a62-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70a62-137">Minimum supported server</span></span><br/> | <span data-ttu-id="70a62-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70a62-138">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="70a62-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="70a62-139">Namespace</span></span><br/>                | <span data-ttu-id="70a62-140">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="70a62-140">Root\\cimv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="70a62-141">MOF</span><span class="sxs-lookup"><span data-stu-id="70a62-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70a62-142"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70a62-142"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="70a62-143">DLL</span><span class="sxs-lookup"><span data-stu-id="70a62-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70a62-144"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70a62-144"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





