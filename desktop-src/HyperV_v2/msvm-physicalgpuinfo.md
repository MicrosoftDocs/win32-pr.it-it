---
description: Contiene informazioni su una GPU (Graphics Processing Unit) RemoteFX.
ms.assetid: 86B47AAE-DBFF-43EF-88C6-44836D6C3AFA
title: Classe Msvm_PhysicalGPUInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PhysicalGPUInfo
- Msvm_PhysicalGPUInfo.InstanceID
- Msvm_PhysicalGPUInfo.Caption
- Msvm_PhysicalGPUInfo.Description
- Msvm_PhysicalGPUInfo.ElementName
- Msvm_PhysicalGPUInfo.Name
- Msvm_PhysicalGPUInfo.ID
- Msvm_PhysicalGPUInfo.TotalVideoMemory
- Msvm_PhysicalGPUInfo.AvailableVideoMemory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cd4ccf65b364620e84063ea6398c59dd0e467f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318315"
---
# <a name="msvm_physicalgpuinfo-class"></a><span data-ttu-id="ba5a8-103">\_Classe MSVM PhysicalGPUInfo</span><span class="sxs-lookup"><span data-stu-id="ba5a8-103">Msvm\_PhysicalGPUInfo class</span></span>

<span data-ttu-id="ba5a8-104">Contiene informazioni su una GPU (Graphics Processing Unit) RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-104">Contains information about a RemoteFX physical graphics processing unit (GPU).</span></span>

<span data-ttu-id="ba5a8-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba5a8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba5a8-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PhysicalGPUInfo : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  string ID;
  uint64 TotalVideoMemory;
  uint64 AvailableVideoMemory;
};
```

## <a name="members"></a><span data-ttu-id="ba5a8-107">Members</span><span class="sxs-lookup"><span data-stu-id="ba5a8-107">Members</span></span>

<span data-ttu-id="ba5a8-108">La **classe \_ PhysicalGPUInfo di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ba5a8-108">The **Msvm\_PhysicalGPUInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="ba5a8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba5a8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba5a8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba5a8-110">Properties</span></span>

<span data-ttu-id="ba5a8-111">La **classe \_ PhysicalGPUInfo di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-111">The **Msvm\_PhysicalGPUInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba5a8-112">**AvailableVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-112">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba5a8-113">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ba5a8-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba5a8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba5a8-115">Quantità di memoria video inutilizzata, in byte, sulla GPU fisica che può essere utilizzata da RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-115">The amount of unused video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="ba5a8-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba5a8-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba5a8-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba5a8-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba5a8-119">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-119">A short description of the object.</span></span> <span data-ttu-id="ba5a8-120">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ba5a8-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ba5a8-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba5a8-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba5a8-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba5a8-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba5a8-124">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="ba5a8-124">A description of the object.</span></span> <span data-ttu-id="ba5a8-125">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ba5a8-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ba5a8-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba5a8-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba5a8-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba5a8-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba5a8-129">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-129">A display name for the object.</span></span> <span data-ttu-id="ba5a8-130">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ba5a8-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ba5a8-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-131">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba5a8-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba5a8-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba5a8-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba5a8-134">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="ba5a8-134">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="ba5a8-135">Identificatore univoco della GPU fisica.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-135">The unique identifier of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="ba5a8-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba5a8-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba5a8-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba5a8-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba5a8-139">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ba5a8-140">Stringa che identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-140">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ba5a8-141">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ba5a8-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ba5a8-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba5a8-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba5a8-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba5a8-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba5a8-145">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="ba5a8-145">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="ba5a8-146">Nome visualizzato della GPU fisica.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-146">The display name of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="ba5a8-147">**TotalVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-147">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba5a8-148">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ba5a8-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba5a8-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba5a8-150">Quantità totale di memoria video, in byte, sulla GPU fisica che può essere utilizzata da RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-150">The total amount of video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba5a8-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba5a8-151">Requirements</span></span>



| <span data-ttu-id="ba5a8-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba5a8-152">Requirement</span></span> | <span data-ttu-id="ba5a8-153">Valore</span><span class="sxs-lookup"><span data-stu-id="ba5a8-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba5a8-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba5a8-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ba5a8-155">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ba5a8-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ba5a8-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba5a8-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ba5a8-157">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ba5a8-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba5a8-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ba5a8-158">Namespace</span></span><br/>                | <span data-ttu-id="ba5a8-159">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ba5a8-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ba5a8-160">MOF</span><span class="sxs-lookup"><span data-stu-id="ba5a8-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba5a8-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba5a8-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba5a8-162">DLL</span><span class="sxs-lookup"><span data-stu-id="ba5a8-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba5a8-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba5a8-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ba5a8-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba5a8-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba5a8-165">**\_ManagementName CIM**</span><span class="sxs-lookup"><span data-stu-id="ba5a8-165">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

