---
description: Rappresenta una voce di autorizzazione per un server di ripristino.
ms.assetid: 8c057b39-7102-4fbf-b4be-f18627a88834
title: Classe Msvm_ReplicationAuthorizationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationAuthorizationSettingData
- Msvm_ReplicationAuthorizationSettingData.InstanceID
- Msvm_ReplicationAuthorizationSettingData.Caption
- Msvm_ReplicationAuthorizationSettingData.Description
- Msvm_ReplicationAuthorizationSettingData.ElementName
- Msvm_ReplicationAuthorizationSettingData.AllowedPrimaryHostSystem
- Msvm_ReplicationAuthorizationSettingData.TrustGroup
- Msvm_ReplicationAuthorizationSettingData.ReplicaStorageLocation
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ba069de1bbe005e8a2a06891db8218ab313baa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231745"
---
# <a name="msvm_replicationauthorizationsettingdata-class"></a><span data-ttu-id="da0f7-103">\_Classe MSVM ReplicationAuthorizationSettingData</span><span class="sxs-lookup"><span data-stu-id="da0f7-103">Msvm\_ReplicationAuthorizationSettingData class</span></span>

<span data-ttu-id="da0f7-104">Rappresenta una voce di autorizzazione per un server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="da0f7-104">Represents an authorization entry for a recovery server.</span></span>

<span data-ttu-id="da0f7-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="da0f7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0f7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da0f7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationAuthorizationSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string AllowedPrimaryHostSystem;
  string TrustGroup;
  string ReplicaStorageLocation;
};
```

## <a name="members"></a><span data-ttu-id="da0f7-107">Members</span><span class="sxs-lookup"><span data-stu-id="da0f7-107">Members</span></span>

<span data-ttu-id="da0f7-108">La **classe \_ ReplicationAuthorizationSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="da0f7-108">The **Msvm\_ReplicationAuthorizationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="da0f7-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da0f7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da0f7-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da0f7-110">Properties</span></span>

<span data-ttu-id="da0f7-111">La **classe \_ ReplicationAuthorizationSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="da0f7-111">The **Msvm\_ReplicationAuthorizationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da0f7-112">**AllowedPrimaryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="da0f7-112">**AllowedPrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da0f7-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da0f7-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da0f7-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="da0f7-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="da0f7-115">Nome di dominio completo o nome di gruppo dei server primari autorizzati a eseguire la replica in questo server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="da0f7-115">The fully qualified domain name or group name of the primary servers that are allowed to replicate to this recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="da0f7-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="da0f7-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da0f7-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da0f7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da0f7-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da0f7-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da0f7-119">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da0f7-119">A short description of the object.</span></span> <span data-ttu-id="da0f7-120">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="da0f7-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="da0f7-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="da0f7-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da0f7-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da0f7-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da0f7-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da0f7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da0f7-124">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="da0f7-124">A description of the object.</span></span> <span data-ttu-id="da0f7-125">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="da0f7-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="da0f7-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="da0f7-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da0f7-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da0f7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da0f7-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da0f7-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da0f7-129">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da0f7-129">A display name for the object.</span></span> <span data-ttu-id="da0f7-130">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="da0f7-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="da0f7-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="da0f7-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da0f7-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da0f7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da0f7-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da0f7-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da0f7-134">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="da0f7-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="da0f7-135">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="da0f7-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="da0f7-136">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="da0f7-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="da0f7-137">**ReplicaStorageLocation**</span><span class="sxs-lookup"><span data-stu-id="da0f7-137">**ReplicaStorageLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da0f7-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da0f7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da0f7-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="da0f7-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="da0f7-140">Percorso in cui verranno archiviati i file di replica di **AllowedPrimaryHostSystem** .</span><span class="sxs-lookup"><span data-stu-id="da0f7-140">The location where replication files from the **AllowedPrimaryHostSystem** will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="da0f7-141">**TrustGroup**</span><span class="sxs-lookup"><span data-stu-id="da0f7-141">**TrustGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da0f7-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da0f7-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da0f7-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="da0f7-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="da0f7-144">Nome del gruppo di attendibilità per la voce di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="da0f7-144">The name of the trust group for the authorization entry.</span></span> <span data-ttu-id="da0f7-145">Vengono identificate le più voci di autorizzazione raggruppate insieme.</span><span class="sxs-lookup"><span data-stu-id="da0f7-145">This identifies the multiple authorization entries that are grouped together.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da0f7-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da0f7-146">Requirements</span></span>



| <span data-ttu-id="da0f7-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="da0f7-147">Requirement</span></span> | <span data-ttu-id="da0f7-148">Valore</span><span class="sxs-lookup"><span data-stu-id="da0f7-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da0f7-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da0f7-149">Minimum supported client</span></span><br/> | <span data-ttu-id="da0f7-150">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="da0f7-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="da0f7-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da0f7-151">Minimum supported server</span></span><br/> | <span data-ttu-id="da0f7-152">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="da0f7-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da0f7-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="da0f7-153">Namespace</span></span><br/>                | <span data-ttu-id="da0f7-154">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="da0f7-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="da0f7-155">MOF</span><span class="sxs-lookup"><span data-stu-id="da0f7-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da0f7-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da0f7-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="da0f7-157">DLL</span><span class="sxs-lookup"><span data-stu-id="da0f7-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da0f7-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="da0f7-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="da0f7-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da0f7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0f7-160">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="da0f7-160">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="da0f7-161">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="da0f7-161">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="da0f7-162">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="da0f7-162">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="da0f7-163">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="da0f7-163">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> </dl>

 

