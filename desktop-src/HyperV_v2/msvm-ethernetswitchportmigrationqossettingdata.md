---
description: Rappresenta le impostazioni QOS VFP.
ms.assetid: e58a7a8d-0301-43ea-9338-18bc8c458e2d
title: Classe Msvm_EthernetSwitchPortMigrationQosSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortMigrationQosSettingData
- Msvm_EthernetSwitchPortMigrationQosSettingData.QueueId
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_ReservationMode
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_LinkSpeedPercentage
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_DefaultReservation
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareLimits
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableSoftwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundReservedValue
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundMaximumMbps
- Msvm_EthernetSwitchPortMigrationQosSettingData.InboundMaximumMbps
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e279b24178c33c760477995ff744a0699cea1aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313855"
---
# <a name="msvm_ethernetswitchportmigrationqossettingdata-class"></a><span data-ttu-id="b2f06-103">\_Classe MSVM EthernetSwitchPortMigrationQosSettingData</span><span class="sxs-lookup"><span data-stu-id="b2f06-103">Msvm\_EthernetSwitchPortMigrationQosSettingData class</span></span>

<span data-ttu-id="b2f06-104">Rappresenta le impostazioni QOS VFP.</span><span class="sxs-lookup"><span data-stu-id="b2f06-104">Represents the VFP QOS settings.</span></span>

<span data-ttu-id="b2f06-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b2f06-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f06-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2f06-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("FD2A5DE3-DC6C-4320-82A5-234D3AF55297"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("E9B59CFA-2BE1-4B21-828F-B6FBDBDDC017"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VFP QOS Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortMigrationQosSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  QueueId = "";
  uint8   Switch_ReservationMode = 0;
  uint8   Switch_LinkSpeedPercentage = 0;
  uint64  Switch_DefaultReservation = 0;
  boolean Switch_EnableHardwareLimits = FALSE;
  boolean Switch_EnableHardwareReservations = FALSE;
  boolean Switch_EnableSoftwareReservations = TRUE;
  uint64  OutboundReservedValue = 0;
  uint64  OutboundMaximumMbps = 0;
  uint64  InboundMaximumMbps = 0;
};
```

## <a name="members"></a><span data-ttu-id="b2f06-107">Members</span><span class="sxs-lookup"><span data-stu-id="b2f06-107">Members</span></span>

<span data-ttu-id="b2f06-108">La **classe \_ EthernetSwitchPortMigrationQosSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b2f06-108">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b2f06-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2f06-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2f06-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2f06-110">Properties</span></span>

<span data-ttu-id="b2f06-111">La **classe \_ EthernetSwitchPortMigrationQosSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b2f06-111">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2f06-112">**InboundMaximumMbps**</span><span class="sxs-lookup"><span data-stu-id="b2f06-112">**InboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f06-113">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b2f06-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2f06-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-115">Qualificatori: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b2f06-115">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b2f06-116">Valore del limite della larghezza di banda per il traffico in ingresso.</span><span class="sxs-lookup"><span data-stu-id="b2f06-116">The bandwidth cap value for inbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="b2f06-117">**OutboundMaximumMbps**</span><span class="sxs-lookup"><span data-stu-id="b2f06-117">**OutboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f06-118">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b2f06-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2f06-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-120">Qualificatori: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b2f06-120">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b2f06-121">Valore del limite della larghezza di banda per il traffico in uscita.</span><span class="sxs-lookup"><span data-stu-id="b2f06-121">The bandwidth cap value for outbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="b2f06-122">**OutboundReservedValue**</span><span class="sxs-lookup"><span data-stu-id="b2f06-122">**OutboundReservedValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f06-123">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b2f06-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2f06-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-125">Qualificatori: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b2f06-125">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b2f06-126">Valore di prenotazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="b2f06-126">The bandwidth reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="b2f06-127">**QueueId**</span><span class="sxs-lookup"><span data-stu-id="b2f06-127">**QueueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f06-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2f06-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2f06-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-130">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b2f06-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b2f06-131">ID della coda QOS.</span><span class="sxs-lookup"><span data-stu-id="b2f06-131">The ID of the QOS queue.</span></span>

</dd> <dt>

<span data-ttu-id="b2f06-132">**Cambia \_ DefaultReservation**</span><span class="sxs-lookup"><span data-stu-id="b2f06-132">**Switch\_DefaultReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f06-133">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b2f06-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2f06-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-135">Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b2f06-135">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b2f06-136">Valore di prenotazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="b2f06-136">The default reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="b2f06-137">**Cambia \_ EnableHardwareLimits**</span><span class="sxs-lookup"><span data-stu-id="b2f06-137">**Switch\_EnableHardwareLimits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f06-138">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b2f06-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2f06-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-140">Qualificatori: **WmiDataId** (5), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="b2f06-140">Qualifiers: **WmiDataId** (5), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="b2f06-141">Indica se vengono tentati gli offload hardware per i limiti, se disponibili.</span><span class="sxs-lookup"><span data-stu-id="b2f06-141">Indicates whether hardware offloads for limits are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="b2f06-142">**Cambia \_ EnableHardwareReservations**</span><span class="sxs-lookup"><span data-stu-id="b2f06-142">**Switch\_EnableHardwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f06-143">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b2f06-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2f06-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-145">Qualificatori: **WmiDataId** (6), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="b2f06-145">Qualifiers: **WmiDataId** (6), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="b2f06-146">Indica se vengono tentati gli offload hardware per le prenotazioni se disponibili.</span><span class="sxs-lookup"><span data-stu-id="b2f06-146">Indicates whether hardware offloads for reservations are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="b2f06-147">**Cambia \_ EnableSoftwareReservations**</span><span class="sxs-lookup"><span data-stu-id="b2f06-147">**Switch\_EnableSoftwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f06-148">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b2f06-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-149">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2f06-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-150">Qualificatori: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b2f06-150">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b2f06-151">Indica se è disponibile la prenotazione basata su software.</span><span class="sxs-lookup"><span data-stu-id="b2f06-151">Indicates whether software based reservation is available.</span></span>

</dd> <dt>

<span data-ttu-id="b2f06-152">**Cambia \_ LinkSpeedPercentage**</span><span class="sxs-lookup"><span data-stu-id="b2f06-152">**Switch\_LinkSpeedPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f06-153">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b2f06-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2f06-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-155">Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b2f06-155">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b2f06-156">Percentuale di velocità del collegamento da usare per la prenotazione.</span><span class="sxs-lookup"><span data-stu-id="b2f06-156">The link speed percentage to be used for reservation.</span></span>

</dd> <dt>

<span data-ttu-id="b2f06-157">**Cambia \_ ReservationMode**</span><span class="sxs-lookup"><span data-stu-id="b2f06-157">**Switch\_ReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f06-158">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b2f06-158">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-159">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b2f06-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2f06-160">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="b2f06-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b2f06-161">Modalità di prenotazione QOS sull'opzione.</span><span class="sxs-lookup"><span data-stu-id="b2f06-161">The QOS reservation mode on the switch.</span></span>

<dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="b2f06-162">**Absolute** (0)</span><span class="sxs-lookup"><span data-stu-id="b2f06-162">**Absolute** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="b2f06-163">**Peso** (1)</span><span class="sxs-lookup"><span data-stu-id="b2f06-163">**Weight** (1)</span></span>


<span data-ttu-id="b2f06-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b2f06-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b2f06-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2f06-165">Requirements</span></span>



| <span data-ttu-id="b2f06-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2f06-166">Requirement</span></span> | <span data-ttu-id="b2f06-167">Valore</span><span class="sxs-lookup"><span data-stu-id="b2f06-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f06-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2f06-168">Minimum supported client</span></span><br/> | <span data-ttu-id="b2f06-169">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2f06-169">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b2f06-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2f06-170">Minimum supported server</span></span><br/> | <span data-ttu-id="b2f06-171">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b2f06-171">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b2f06-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2f06-172">Namespace</span></span><br/>                | <span data-ttu-id="b2f06-173">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b2f06-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b2f06-174">MOF</span><span class="sxs-lookup"><span data-stu-id="b2f06-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2f06-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2f06-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2f06-176">DLL</span><span class="sxs-lookup"><span data-stu-id="b2f06-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2f06-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2f06-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2f06-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2f06-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f06-179">**\_EthernetSwitchPortFeatureSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2f06-179">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

