---
description: Rappresenta lo stato configurato delle impostazioni di sicurezza per.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Classe Msvm_SecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312885"
---
# <a name="msvm_securitysettingdata-class"></a><span data-ttu-id="15125-103">\_Classe MSVM SecuritySettingData</span><span class="sxs-lookup"><span data-stu-id="15125-103">Msvm\_SecuritySettingData class</span></span>

<span data-ttu-id="15125-104">Rappresenta lo stato configurato delle impostazioni di sicurezza per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="15125-104">Represents the configured state of the security settings for a virtual machine.</span></span>

<span data-ttu-id="15125-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="15125-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15125-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15125-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a><span data-ttu-id="15125-107">Members</span><span class="sxs-lookup"><span data-stu-id="15125-107">Members</span></span>

<span data-ttu-id="15125-108">La **classe \_ SecuritySettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="15125-108">The **Msvm\_SecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="15125-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15125-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15125-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15125-110">Properties</span></span>

<span data-ttu-id="15125-111">La **classe \_ SecuritySettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="15125-111">The **Msvm\_SecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15125-112">**DataProtectionRequested**</span><span class="sxs-lookup"><span data-stu-id="15125-112">**DataProtectionRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15125-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="15125-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15125-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15125-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15125-115">Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="15125-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="15125-116">**true** per richiedere la protezione dei dati per una macchina virtuale. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="15125-116">**true** to request data protection for a VM; otherwise, **false**.</span></span> <span data-ttu-id="15125-117">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="15125-117">The default value is **false.**</span></span>

</dd> <dt>

<span data-ttu-id="15125-118">**EncryptStateAndVmMigrationTraffic**</span><span class="sxs-lookup"><span data-stu-id="15125-118">**EncryptStateAndVmMigrationTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15125-119">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="15125-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15125-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15125-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15125-121">Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="15125-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="15125-122">**true** per avere lo stato e il traffico di migrazione di una macchina virtuale crittografata; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="15125-122">**true** to have the state and migration traffic of a VM encrypted; otherwise, **false**.</span></span> <span data-ttu-id="15125-123">Il valore predefinito per una VM appena creata è **false**.</span><span class="sxs-lookup"><span data-stu-id="15125-123">The default value for a newly-created VM is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="15125-124">**KsdEnabled**</span><span class="sxs-lookup"><span data-stu-id="15125-124">**KsdEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15125-125">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="15125-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15125-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15125-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15125-127">Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="15125-127">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="15125-128">**true** per abilitare un dispositivo di archiviazione chiavi (KSD) per la macchina virtuale. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="15125-128">**true** to enable a key storage device (KSD) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="15125-129">Una macchina virtuale appena creata ha un KSD Disable.</span><span class="sxs-lookup"><span data-stu-id="15125-129">A newly-created VM has a disable KSD.</span></span>

</dd> <dt>

<span data-ttu-id="15125-130">**ShieldingRequested**</span><span class="sxs-lookup"><span data-stu-id="15125-130">**ShieldingRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15125-131">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="15125-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15125-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15125-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15125-133">Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="15125-133">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="15125-134">**true** per richiedere la schermatura per una macchina virtuale. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="15125-134">**true** to request shielding for a VM; otherwise, **false**.</span></span> <span data-ttu-id="15125-135">Una macchina virtuale appena creata ha uno stato richiesto per la schermatura iniziale di **false**.</span><span class="sxs-lookup"><span data-stu-id="15125-135">A newly-created VM has an initial shielding requested state of **false**.</span></span>

</dd> <dt>

<span data-ttu-id="15125-136">**TpmEnabled**</span><span class="sxs-lookup"><span data-stu-id="15125-136">**TpmEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15125-137">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="15125-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15125-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15125-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15125-139">Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="15125-139">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="15125-140">**true** per abilitare un modulo TPM (Trusted Platform nodul) per questa macchina virtuale. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="15125-140">**true** to enable a trusted platform nodule (TPM) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="15125-141">Una macchina virtuale appena creata dispone di un TPM disabilitato.</span><span class="sxs-lookup"><span data-stu-id="15125-141">A newly-created VM has a disable TPM.</span></span>

</dd> <dt>

<span data-ttu-id="15125-142">**VirtualizationBasedSecurityOptOut**</span><span class="sxs-lookup"><span data-stu-id="15125-142">**VirtualizationBasedSecurityOptOut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15125-143">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="15125-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15125-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15125-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15125-145">Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="15125-145">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="15125-146">**true** per non offrire una protezione basata sulla virtualizzazione delle macchine virtuali; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="15125-146">**true** to not offer a VM virtualization-based security; otherwise, **false**.</span></span> <span data-ttu-id="15125-147">L'impostazione predefinita per lo stato di rifiuto esplicito di una macchina virtuale appena creata è **false**.</span><span class="sxs-lookup"><span data-stu-id="15125-147">The default setting for a newly-crated VM's opt-out state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15125-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15125-148">Requirements</span></span>



| <span data-ttu-id="15125-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="15125-149">Requirement</span></span> | <span data-ttu-id="15125-150">Valore</span><span class="sxs-lookup"><span data-stu-id="15125-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15125-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15125-151">Minimum supported client</span></span><br/> | <span data-ttu-id="15125-152">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="15125-152">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="15125-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15125-153">Minimum supported server</span></span><br/> | <span data-ttu-id="15125-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="15125-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="15125-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="15125-155">Namespace</span></span><br/>                | <span data-ttu-id="15125-156">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="15125-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15125-157">MOF</span><span class="sxs-lookup"><span data-stu-id="15125-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15125-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15125-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15125-159">DLL</span><span class="sxs-lookup"><span data-stu-id="15125-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15125-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15125-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15125-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15125-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15125-162">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="15125-162">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

