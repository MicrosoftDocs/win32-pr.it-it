---
description: Rappresenta lo stato configurato del dispositivo TPM.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Classe Msvm_TPMSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527667"
---
# <a name="msvm_tpmsettingdata-class"></a><span data-ttu-id="cc78e-103">\_Classe MSVM TPMSettingData</span><span class="sxs-lookup"><span data-stu-id="cc78e-103">Msvm\_TPMSettingData class</span></span>

<span data-ttu-id="cc78e-104">Rappresenta lo stato configurato del dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="cc78e-104">Represents the configured state of the TPM device.</span></span>

<span data-ttu-id="cc78e-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cc78e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc78e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc78e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a><span data-ttu-id="cc78e-107">Members</span><span class="sxs-lookup"><span data-stu-id="cc78e-107">Members</span></span>

<span data-ttu-id="cc78e-108">La **classe \_ TPMSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cc78e-108">The **Msvm\_TPMSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="cc78e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cc78e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc78e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cc78e-110">Properties</span></span>

<span data-ttu-id="cc78e-111">La **classe \_ TPMSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc78e-111">The **Msvm\_TPMSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc78e-112">**Dataprotected**</span><span class="sxs-lookup"><span data-stu-id="cc78e-112">**DataProtected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc78e-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cc78e-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc78e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cc78e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc78e-115">Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc78e-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc78e-116">**true** per impostare un criterio per proteggere i dati di una macchina virtuale. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="cc78e-116">**true** to set a policy to protect a VM's data; otherwise, **false**.</span></span> <span data-ttu-id="cc78e-117">Un TPM appena creato è disabilitato, quindi lo stato di protezione dati iniziale è **false**.</span><span class="sxs-lookup"><span data-stu-id="cc78e-117">A newly created TPM is disabled, so the initial data protection state is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="cc78e-118">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="cc78e-118">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc78e-119">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc78e-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc78e-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cc78e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc78e-121">Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc78e-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc78e-122">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="cc78e-122">The enabled and disabled states of an element.</span></span> <span data-ttu-id="cc78e-123">Il valore predefinito è **disabled**.</span><span class="sxs-lookup"><span data-stu-id="cc78e-123">The default value is **Disabled**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cc78e-124">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="cc78e-124">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cc78e-125">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="cc78e-125">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cc78e-126">**Protector**</span><span class="sxs-lookup"><span data-stu-id="cc78e-126">**KeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc78e-127">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cc78e-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cc78e-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cc78e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc78e-129">Qualificatori: [**obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span><span class="sxs-lookup"><span data-stu-id="cc78e-129">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="cc78e-130">La protezione con chiave dal client del servizio sorveglianza host.</span><span class="sxs-lookup"><span data-stu-id="cc78e-130">The key protector from Host Guardian Service client.</span></span>

</dd> <dt>

<span data-ttu-id="cc78e-131">**LastKnownGoodKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="cc78e-131">**LastKnownGoodKeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc78e-132">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cc78e-132">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cc78e-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cc78e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc78e-134">Qualificatori: [**obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span><span class="sxs-lookup"><span data-stu-id="cc78e-134">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="cc78e-135">L'ultima protezione con chiave valida nota ha crittografato correttamente lo stato del dispositivo TPM nell'ultimo avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cc78e-135">The last known good key protector successfully encrypted TPM device state in the last VM boot.</span></span>

<span data-ttu-id="cc78e-136">Questa proprietà è di sola lettura per il client WMI e può essere modificata solo dal dispositivo TPM della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cc78e-136">This property is read-only for the WMI client, and can only be modified by the VM TPM device.</span></span>

</dd> <dt>

<span data-ttu-id="cc78e-137">**Schermato**</span><span class="sxs-lookup"><span data-stu-id="cc78e-137">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc78e-138">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cc78e-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc78e-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cc78e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc78e-140">Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc78e-140">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc78e-141">**true** per definire un criterio per la schermatura di una macchina virtuale. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="cc78e-141">**true** to define a policy that shields a virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="cc78e-142">Un TPM appena creato è disabilitato, quindi lo stato di schermatura iniziale è **false**.</span><span class="sxs-lookup"><span data-stu-id="cc78e-142">A newly created TPM is disabled, so the initial shielding state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc78e-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc78e-143">Requirements</span></span>



| <span data-ttu-id="cc78e-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc78e-144">Requirement</span></span> | <span data-ttu-id="cc78e-145">Valore</span><span class="sxs-lookup"><span data-stu-id="cc78e-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc78e-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc78e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cc78e-147">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cc78e-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="cc78e-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc78e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cc78e-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cc78e-149">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cc78e-150">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="cc78e-150">End of client support</span></span><br/>    | <span data-ttu-id="cc78e-151">Windows 10</span><span class="sxs-lookup"><span data-stu-id="cc78e-151">Windows 10</span></span><br/>                                                                                   |
| <span data-ttu-id="cc78e-152">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="cc78e-152">End of server support</span></span><br/>    | <span data-ttu-id="cc78e-153">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cc78e-153">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cc78e-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cc78e-154">Namespace</span></span><br/>                | <span data-ttu-id="cc78e-155">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="cc78e-155">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cc78e-156">MOF</span><span class="sxs-lookup"><span data-stu-id="cc78e-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc78e-157"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc78e-157"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc78e-158">DLL</span><span class="sxs-lookup"><span data-stu-id="cc78e-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc78e-159"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cc78e-159"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cc78e-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc78e-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc78e-161">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="cc78e-161">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

