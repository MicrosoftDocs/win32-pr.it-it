---
description: Rappresenta le impostazioni di un sistema virtuale da importare. Utilizzato dal metodo smontaggio della \_ classe MSVM AssignableDeviceService.
ms.assetid: 49892e21-3e8d-4644-8cde-72966927f350
title: Classe Msvm_AssignableDeviceDismountSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceDismountSettingData
- Msvm_AssignableDeviceDismountSettingData.DeviceInstancePath
- Msvm_AssignableDeviceDismountSettingData.DeviceLocationPath
- Msvm_AssignableDeviceDismountSettingData.RequireAcsSupport
- Msvm_AssignableDeviceDismountSettingData.RequireDeviceMitigations
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5783ed9611c16d875211f29d364fe3eaff29b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314344"
---
# <a name="msvm_assignabledevicedismountsettingdata-class"></a><span data-ttu-id="b216c-104">\_Classe MSVM AssignableDeviceDismountSettingData</span><span class="sxs-lookup"><span data-stu-id="b216c-104">Msvm\_AssignableDeviceDismountSettingData class</span></span>

<span data-ttu-id="b216c-105">Rappresenta le impostazioni di un sistema virtuale da importare.</span><span class="sxs-lookup"><span data-stu-id="b216c-105">Represents the settings of a virtual system to import.</span></span> <span data-ttu-id="b216c-106">Utilizzato dal metodo [**smontaggio**](msvm-assignabledeviceservice-dismountassignabledevice.md) della classe [**MSVM \_ AssignableDeviceService**](msvm-assignabledeviceservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b216c-106">Used by the [**Dismount**](msvm-assignabledeviceservice-dismountassignabledevice.md) method of the [**Msvm\_AssignableDeviceService**](msvm-assignabledeviceservice.md) class.</span></span>

<span data-ttu-id="b216c-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b216c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b216c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b216c-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_AssignableDeviceDismountSettingData : CIM_SettingData
{
  string  DeviceInstancePath;
  string  DeviceLocationPath;
  boolean RequireAcsSupport;
  boolean RequireDeviceMitigations;
};
```

## <a name="members"></a><span data-ttu-id="b216c-109">Members</span><span class="sxs-lookup"><span data-stu-id="b216c-109">Members</span></span>

<span data-ttu-id="b216c-110">La **classe \_ AssignableDeviceDismountSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b216c-110">The **Msvm\_AssignableDeviceDismountSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b216c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b216c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b216c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b216c-112">Properties</span></span>

<span data-ttu-id="b216c-113">La **classe \_ AssignableDeviceDismountSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b216c-113">The **Msvm\_AssignableDeviceDismountSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b216c-114">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="b216c-114">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b216c-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b216c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b216c-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b216c-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b216c-117">ID istanza del dispositivo PNP.</span><span class="sxs-lookup"><span data-stu-id="b216c-117">PNP device instance ID.</span></span>

</dd> <dt>

<span data-ttu-id="b216c-118">**DeviceLocationPath**</span><span class="sxs-lookup"><span data-stu-id="b216c-118">**DeviceLocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b216c-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b216c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b216c-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b216c-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b216c-121">Percorso del dispositivo PNP.</span><span class="sxs-lookup"><span data-stu-id="b216c-121">PNP device location path.</span></span>

</dd> <dt>

<span data-ttu-id="b216c-122">**RequireAcsSupport**</span><span class="sxs-lookup"><span data-stu-id="b216c-122">**RequireAcsSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b216c-123">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b216c-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b216c-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b216c-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b216c-125">Indica se il supporto ACS necessario deve essere preposto prima di consentire lo smontaggio.</span><span class="sxs-lookup"><span data-stu-id="b216c-125">Indicates if the requisite ACS support should be in place before permitting the dismount.</span></span>

</dd> <dt>

<span data-ttu-id="b216c-126">**RequireDeviceMitigations**</span><span class="sxs-lookup"><span data-stu-id="b216c-126">**RequireDeviceMitigations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b216c-127">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b216c-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b216c-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b216c-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b216c-129">Indica se devono essere applicate le attenuazioni dei dispositivi prima di consentire lo smontaggio.</span><span class="sxs-lookup"><span data-stu-id="b216c-129">Indicates if device mitigations should be in place before permitting the dismount.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b216c-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b216c-130">Requirements</span></span>



| <span data-ttu-id="b216c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b216c-131">Requirement</span></span> | <span data-ttu-id="b216c-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b216c-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b216c-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b216c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b216c-134">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="b216c-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b216c-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b216c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b216c-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b216c-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b216c-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b216c-137">Namespace</span></span><br/>                | <span data-ttu-id="b216c-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b216c-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b216c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b216c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b216c-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b216c-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b216c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b216c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b216c-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b216c-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b216c-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b216c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b216c-144">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="b216c-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




