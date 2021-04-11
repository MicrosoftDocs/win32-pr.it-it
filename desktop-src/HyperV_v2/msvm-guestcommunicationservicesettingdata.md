---
description: Rappresenta le impostazioni del servizio di comunicazione Guest.
ms.assetid: c36d3002-d43e-4284-b765-2795c941f023
title: Classe Msvm_GuestCommunicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestCommunicationServiceSettingData
- Msvm_GuestCommunicationServiceSettingData.Name
- Msvm_GuestCommunicationServiceSettingData.EnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5506689f5b266c428a790774c1fb98a1b0413b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129751"
---
# <a name="msvm_guestcommunicationservicesettingdata-class"></a><span data-ttu-id="fd3b4-103">\_Classe MSVM GuestCommunicationServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="fd3b4-103">Msvm\_GuestCommunicationServiceSettingData class</span></span>

<span data-ttu-id="fd3b4-104">Rappresenta le impostazioni del servizio di comunicazione Guest.</span><span class="sxs-lookup"><span data-stu-id="fd3b4-104">Represents the settings of the guest communication service.</span></span>

<span data-ttu-id="fd3b4-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fd3b4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd3b4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd3b4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestCommunicationServiceSettingData : CIM_SettingData
{
  string Name;
  uint16 EnabledStatePolicy;
};
```

## <a name="members"></a><span data-ttu-id="fd3b4-107">Members</span><span class="sxs-lookup"><span data-stu-id="fd3b4-107">Members</span></span>

<span data-ttu-id="fd3b4-108">La **classe \_ GuestCommunicationServiceSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fd3b4-108">The **Msvm\_GuestCommunicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fd3b4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd3b4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd3b4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd3b4-110">Properties</span></span>

<span data-ttu-id="fd3b4-111">La **classe \_ GuestCommunicationServiceSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fd3b4-111">The **Msvm\_GuestCommunicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd3b4-112">**EnabledStatePolicy**</span><span class="sxs-lookup"><span data-stu-id="fd3b4-112">**EnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3b4-113">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd3b4-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd3b4-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd3b4-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd3b4-115">EnabledStatePolicy è un'enumerazione Integer che indica lo stato abilitato, disabilitato o predefinito di **MSVM \_ GuestCommunicationServiceSettingData**.</span><span class="sxs-lookup"><span data-stu-id="fd3b4-115">EnabledStatePolicy is an integer enumeration that indicates the enabled, disabled or default state of the **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fd3b4-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="fd3b4-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fd3b4-117">Il servizio di comunicazione è impostato sullo stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="fd3b4-117">The communication service is set to the enabled state.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fd3b4-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="fd3b4-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fd3b4-119">Il servizio di comunicazione è impostato sullo stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="fd3b4-119">The communication service is set to the disabled state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="fd3b4-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Posticipato** (8)</span><span class="sxs-lookup"><span data-stu-id="fd3b4-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="fd3b4-121">Lo stato del servizio di comunicazione dipende da **DefaultEnabledStatePolicy** in **MSVM \_ GuestCommunicationServiceSettingData**.</span><span class="sxs-lookup"><span data-stu-id="fd3b4-121">The communication service state depends on **DefaultEnabledStatePolicy** in **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd3b4-122">**Nome**</span><span class="sxs-lookup"><span data-stu-id="fd3b4-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd3b4-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd3b4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd3b4-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd3b4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd3b4-125">GUID del servizio.</span><span class="sxs-lookup"><span data-stu-id="fd3b4-125">The GUID of the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd3b4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd3b4-126">Requirements</span></span>



| <span data-ttu-id="fd3b4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd3b4-127">Requirement</span></span> | <span data-ttu-id="fd3b4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="fd3b4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3b4-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd3b4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fd3b4-130">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fd3b4-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fd3b4-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd3b4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fd3b4-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fd3b4-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fd3b4-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fd3b4-133">Namespace</span></span><br/>                | <span data-ttu-id="fd3b4-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fd3b4-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fd3b4-135">MOF</span><span class="sxs-lookup"><span data-stu-id="fd3b4-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd3b4-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd3b4-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd3b4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fd3b4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd3b4-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fd3b4-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fd3b4-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd3b4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd3b4-140">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="fd3b4-140">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




