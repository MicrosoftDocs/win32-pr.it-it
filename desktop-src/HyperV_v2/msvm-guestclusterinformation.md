---
description: Usato nel metodo QueryGuestClusterInformation nella \_ classe MSVM VssService per recuperare informazioni sul cluster guest di cui fa parte la macchina virtuale.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Classe Msvm_GuestClusterInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307910"
---
# <a name="msvm_guestclusterinformation-class"></a><span data-ttu-id="9acec-103">\_Classe MSVM GuestClusterInformation</span><span class="sxs-lookup"><span data-stu-id="9acec-103">Msvm\_GuestClusterInformation class</span></span>

<span data-ttu-id="9acec-104">Usato nel metodo [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) nella classe [**MSVM \_ VssService**](msvm-vssservice.md) per recuperare informazioni sul cluster guest di cui fa parte la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9acec-104">Used in the [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) method in the [**Msvm\_VssService**](msvm-vssservice.md) class to retrieve information about the guest cluster the VM is part of.</span></span>

<span data-ttu-id="9acec-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9acec-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9acec-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9acec-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a><span data-ttu-id="9acec-107">Members</span><span class="sxs-lookup"><span data-stu-id="9acec-107">Members</span></span>

<span data-ttu-id="9acec-108">La **classe \_ GuestClusterInformation di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9acec-108">The **Msvm\_GuestClusterInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="9acec-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9acec-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9acec-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9acec-110">Properties</span></span>

<span data-ttu-id="9acec-111">La **classe \_ GuestClusterInformation di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9acec-111">The **Msvm\_GuestClusterInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9acec-112">**ClusterId**</span><span class="sxs-lookup"><span data-stu-id="9acec-112">**ClusterId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acec-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9acec-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9acec-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9acec-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9acec-115">Identificatore del cluster di failover di cui fa parte il sistema operativo guest della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9acec-115">The identifier of the failover cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="9acec-116">**ClusterSize**</span><span class="sxs-lookup"><span data-stu-id="9acec-116">**ClusterSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acec-117">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9acec-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9acec-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9acec-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9acec-119">Numero di nodi del cluster di cui fa parte il sistema operativo guest della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9acec-119">Number of nodes in the cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="9acec-120">**IsActiveActive**</span><span class="sxs-lookup"><span data-stu-id="9acec-120">**IsActiveActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acec-121">Tipo di dati: matrice **booleana**</span><span class="sxs-lookup"><span data-stu-id="9acec-121">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="9acec-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9acec-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9acec-123">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="9acec-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9acec-124">Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se la risorsa disco corrispondente nel cluster guest è condivisa tra le macchine virtuali in modalità attiva/attiva.</span><span class="sxs-lookup"><span data-stu-id="9acec-124">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is shared between VMs in active/active mode.</span></span>

</dd> <dt>

<span data-ttu-id="9acec-125">**IsClustered**</span><span class="sxs-lookup"><span data-stu-id="9acec-125">**IsClustered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acec-126">Tipo di dati: matrice **booleana**</span><span class="sxs-lookup"><span data-stu-id="9acec-126">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="9acec-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9acec-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9acec-128">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="9acec-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9acec-129">Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se il disco corrispondente è una risorsa cluster nel cluster guest.</span><span class="sxs-lookup"><span data-stu-id="9acec-129">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk is a cluster resource in the guest cluster.</span></span>

</dd> <dt>

<span data-ttu-id="9acec-130">**IsOnline**</span><span class="sxs-lookup"><span data-stu-id="9acec-130">**IsOnline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acec-131">Tipo di dati: matrice **booleana**</span><span class="sxs-lookup"><span data-stu-id="9acec-131">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="9acec-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9acec-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9acec-133">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="9acec-133">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9acec-134">Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se la risorsa disco corrispondente nel cluster guest è online.</span><span class="sxs-lookup"><span data-stu-id="9acec-134">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is online.</span></span>

</dd> <dt>

<span data-ttu-id="9acec-135">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="9acec-135">**IsOwned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acec-136">Tipo di dati: matrice **booleana**</span><span class="sxs-lookup"><span data-stu-id="9acec-136">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="9acec-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9acec-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9acec-138">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="9acec-138">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9acec-139">Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se la risorsa disco corrispondente nel cluster guest è attualmente di proprietà di questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9acec-139">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is currenly owned by this VM.</span></span>

</dd> <dt>

<span data-ttu-id="9acec-140">**LastResourceMoveTime**</span><span class="sxs-lookup"><span data-stu-id="9acec-140">**LastResourceMoveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acec-141">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9acec-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9acec-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9acec-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9acec-143">Il numero di tick dell'orologio quando una delle risorse disco condivise è stata spostata più di recente.</span><span class="sxs-lookup"><span data-stu-id="9acec-143">The clock tick count when one of the shared disk resources last moved.</span></span>

> [!Note]  
> <span data-ttu-id="9acec-144">Questa proprietà è stata aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="9acec-144">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="9acec-145">**SharedVirtualHardDiskPaths**</span><span class="sxs-lookup"><span data-stu-id="9acec-145">**SharedVirtualHardDiskPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acec-146">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="9acec-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9acec-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9acec-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9acec-148">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="9acec-148">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9acec-149">Una matrice di percorsi di dischi rigidi virtuali condivisi connessi alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9acec-149">An array of shared virtual hard disk paths connected to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="9acec-150">**SharedVirtualHardDisks**</span><span class="sxs-lookup"><span data-stu-id="9acec-150">**SharedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acec-151">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="9acec-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9acec-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9acec-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9acec-153">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="9acec-153">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9acec-154">Una matrice di dati di impostazione di allocazione risorse (RASD) che rappresentano i dischi rigidi virtuali condivisi connessi alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9acec-154">An array of Resource Allocation Setting Data (RASD) representing the shared virtual hard disks connected to the VM.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9acec-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9acec-155">Requirements</span></span>



| <span data-ttu-id="9acec-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="9acec-156">Requirement</span></span> | <span data-ttu-id="9acec-157">Valore</span><span class="sxs-lookup"><span data-stu-id="9acec-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9acec-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9acec-158">Minimum supported client</span></span><br/> | <span data-ttu-id="9acec-159">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9acec-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9acec-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9acec-160">Minimum supported server</span></span><br/> | <span data-ttu-id="9acec-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9acec-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9acec-162">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9acec-162">Namespace</span></span><br/>                | <span data-ttu-id="9acec-163">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9acec-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9acec-164">MOF</span><span class="sxs-lookup"><span data-stu-id="9acec-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9acec-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9acec-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9acec-166">DLL</span><span class="sxs-lookup"><span data-stu-id="9acec-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9acec-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9acec-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

