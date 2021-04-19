---
description: Rappresenta le impostazioni di offload del Commuter.
ms.assetid: 4e00544e-a8db-4337-af3f-f651bfcf6b05
title: Classe Msvm_EthernetSwitchHardwareOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadSettingData
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssMinQueuePairs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ef0e22143ffd424ee3acee616504e45d8125bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320032"
---
# <a name="msvm_ethernetswitchhardwareoffloadsettingdata-class"></a><span data-ttu-id="03bc9-103">\_Classe MSVM EthernetSwitchHardwareOffloadSettingData</span><span class="sxs-lookup"><span data-stu-id="03bc9-103">Msvm\_EthernetSwitchHardwareOffloadSettingData class</span></span>

<span data-ttu-id="03bc9-104">Rappresenta le impostazioni di offload del Commuter.</span><span class="sxs-lookup"><span data-stu-id="03bc9-104">Represents the switch offload settings.</span></span>

<span data-ttu-id="03bc9-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="03bc9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="03bc9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03bc9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1550e863-4337-4917-a040-5a27dbc58b59"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("2"), InterfaceRevision("0"), DisplayName("Ethernet Switch Hardware Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  boolean DefaultQueueVrssEnabled = TRUE;
  boolean DefaultQueueVmmqEnabled = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 16;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 2;
  uint32  DefaultQueueVrssMinQueuePairs = 1;
};
```

## <a name="members"></a><span data-ttu-id="03bc9-107">Members</span><span class="sxs-lookup"><span data-stu-id="03bc9-107">Members</span></span>

<span data-ttu-id="03bc9-108">La **classe \_ EthernetSwitchHardwareOffloadSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="03bc9-108">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="03bc9-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03bc9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03bc9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03bc9-110">Properties</span></span>

<span data-ttu-id="03bc9-111">La **classe \_ EthernetSwitchHardwareOffloadSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="03bc9-111">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03bc9-112">**DefaultQueueVmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="03bc9-112">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03bc9-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="03bc9-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="03bc9-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-115">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03bc9-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03bc9-116">Specifica le impostazioni VMMQ per la coda predefinita di vswitch.</span><span class="sxs-lookup"><span data-stu-id="03bc9-116">Specifies the VMMQ settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="03bc9-117">**DefaultQueueVmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="03bc9-117">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03bc9-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03bc9-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="03bc9-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-120">Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03bc9-120">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03bc9-121">Specifica il numero di code per la coda predefinita.</span><span class="sxs-lookup"><span data-stu-id="03bc9-121">Specifies the number of queues for the default queue.</span></span>

</dd> <dt>

<span data-ttu-id="03bc9-122">**DefaultQueueVrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="03bc9-122">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03bc9-123">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="03bc9-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="03bc9-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-125">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03bc9-125">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03bc9-126">Specifica le impostazioni VRss per la coda predefinita di vswitch.</span><span class="sxs-lookup"><span data-stu-id="03bc9-126">Specifies the VRss settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="03bc9-127">**DefaultQueueVrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="03bc9-127">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03bc9-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="03bc9-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03bc9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-130">Qualificatori: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03bc9-130">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03bc9-131">Indica se la CPU VMQ primaria è esclusa dalla tabella di riferimento indiretto VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="03bc9-131">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="03bc9-132">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="03bc9-132">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="03bc9-133">**DefaultQueueVrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="03bc9-133">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03bc9-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="03bc9-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03bc9-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-136">Qualificatori: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03bc9-136">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03bc9-137">Indica se eseguire sempre la distribuzione VRSS per la coda predefinita, indipendentemente dallo stato RSS del vPort esterno.</span><span class="sxs-lookup"><span data-stu-id="03bc9-137">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="03bc9-138">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="03bc9-138">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="03bc9-139">**DefaultQueueVrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="03bc9-139">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03bc9-140">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03bc9-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03bc9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-142">Qualificatori: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03bc9-142">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03bc9-143">Indica il numero minimo di code utilizzate per VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="03bc9-143">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="03bc9-144">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="03bc9-144">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="03bc9-145">**DefaultQueueVrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="03bc9-145">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03bc9-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03bc9-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03bc9-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03bc9-148">Qualificatori: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03bc9-148">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03bc9-149">Indica il modo in cui le code VRSS/VMMQ vengono indirizzate a processori host diversi.</span><span class="sxs-lookup"><span data-stu-id="03bc9-149">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="03bc9-150">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="03bc9-150">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03bc9-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03bc9-151">Requirements</span></span>



| <span data-ttu-id="03bc9-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="03bc9-152">Requirement</span></span> | <span data-ttu-id="03bc9-153">Valore</span><span class="sxs-lookup"><span data-stu-id="03bc9-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03bc9-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03bc9-154">Minimum supported client</span></span><br/> | <span data-ttu-id="03bc9-155">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="03bc9-155">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="03bc9-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03bc9-156">Minimum supported server</span></span><br/> | <span data-ttu-id="03bc9-157">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="03bc9-157">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="03bc9-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03bc9-158">Namespace</span></span><br/>                | <span data-ttu-id="03bc9-159">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="03bc9-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="03bc9-160">MOF</span><span class="sxs-lookup"><span data-stu-id="03bc9-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03bc9-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03bc9-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03bc9-162">DLL</span><span class="sxs-lookup"><span data-stu-id="03bc9-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03bc9-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03bc9-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="03bc9-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03bc9-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03bc9-165">**\_EthernetSwitchFeatureSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="03bc9-165">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




