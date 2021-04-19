---
description: Rappresenta i dati dell'impostazione della funzionalità di mapping del team di porta.
ms.assetid: 7c9a392d-c95e-4b0d-8201-e50adabd21b2
title: Classe Msvm_EthernetSwitchPortTeamMappingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortTeamMappingSettingData
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterName
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterDeviceId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f0d7385499dcdf6e84c361de03950a4e78be0a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320015"
---
# <a name="msvm_ethernetswitchportteammappingsettingdata-class"></a><span data-ttu-id="fa9e8-103">\_Classe MSVM EthernetSwitchPortTeamMappingSettingData</span><span class="sxs-lookup"><span data-stu-id="fa9e8-103">Msvm\_EthernetSwitchPortTeamMappingSettingData class</span></span>

<span data-ttu-id="fa9e8-104">Rappresenta i dati dell'impostazione della funzionalità di mapping del team di porta.</span><span class="sxs-lookup"><span data-stu-id="fa9e8-104">Represents the port team mapping feature setting data.</span></span>

<span data-ttu-id="fa9e8-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fa9e8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa9e8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa9e8-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8D45D4BD-8C18-435C-98A7-D632A7C618FF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Team Mapping Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortTeamMappingSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string NetAdapterName = "";
  string NetAdapterDeviceId = "";
};
```

## <a name="members"></a><span data-ttu-id="fa9e8-107">Members</span><span class="sxs-lookup"><span data-stu-id="fa9e8-107">Members</span></span>

<span data-ttu-id="fa9e8-108">La **classe \_ EthernetSwitchPortTeamMappingSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fa9e8-108">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fa9e8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fa9e8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa9e8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fa9e8-110">Properties</span></span>

<span data-ttu-id="fa9e8-111">La **classe \_ EthernetSwitchPortTeamMappingSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fa9e8-111">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa9e8-112">**NetAdapterDeviceId**</span><span class="sxs-lookup"><span data-stu-id="fa9e8-112">**NetAdapterDeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa9e8-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa9e8-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa9e8-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fa9e8-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa9e8-115">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="fa9e8-115">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fa9e8-116">ID dispositivo della scheda fisica mappata preferita.</span><span class="sxs-lookup"><span data-stu-id="fa9e8-116">Device ID of the preferred mapped physical adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fa9e8-117">**NetAdapterName**</span><span class="sxs-lookup"><span data-stu-id="fa9e8-117">**NetAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa9e8-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fa9e8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa9e8-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fa9e8-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa9e8-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="fa9e8-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fa9e8-121">Nome della scheda fisica mappata preferita.</span><span class="sxs-lookup"><span data-stu-id="fa9e8-121">Name of the preferred mapped physical adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa9e8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa9e8-122">Requirements</span></span>



| <span data-ttu-id="fa9e8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa9e8-123">Requirement</span></span> | <span data-ttu-id="fa9e8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="fa9e8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa9e8-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa9e8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa9e8-126">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa9e8-126">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fa9e8-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa9e8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa9e8-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fa9e8-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fa9e8-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fa9e8-129">Namespace</span></span><br/>                | <span data-ttu-id="fa9e8-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fa9e8-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fa9e8-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fa9e8-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa9e8-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa9e8-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa9e8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fa9e8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa9e8-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa9e8-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fa9e8-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa9e8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa9e8-136">**\_EthernetSwitchPortFeatureSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="fa9e8-136">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

