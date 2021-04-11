---
description: Classe Association tra un componente dell'interfaccia del servizio Guest e la risorsa del servizio Guest.
ms.assetid: 4c16c3ab-4137-40ab-be2e-f385d8e36a41
title: Classe Msvm_GuestServiceInterfaceSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceSettingDataComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.GroupComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 988975fea1fd519a5e3917faeb73d345334d74b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226258"
---
# <a name="msvm_guestserviceinterfacesettingdatacomponent-class"></a><span data-ttu-id="2c7d1-103">\_Classe MSVM GuestServiceInterfaceSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="2c7d1-103">Msvm\_GuestServiceInterfaceSettingDataComponent class</span></span>

<span data-ttu-id="2c7d1-104">Classe Association tra un componente dell'interfaccia del servizio Guest e la risorsa del servizio Guest.</span><span class="sxs-lookup"><span data-stu-id="2c7d1-104">Association class between a guest service interface component and the guest service resource.</span></span>

<span data-ttu-id="2c7d1-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2c7d1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c7d1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c7d1-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceSettingDataComponent : CIM_Component
{
  Msvm_GuestServiceInterfaceComponentSettingData REF GroupComponent;
  CIM_SettingData                                REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="2c7d1-107">Members</span><span class="sxs-lookup"><span data-stu-id="2c7d1-107">Members</span></span>

<span data-ttu-id="2c7d1-108">La **classe \_ GuestServiceInterfaceSettingDataComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2c7d1-108">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="2c7d1-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c7d1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c7d1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c7d1-110">Properties</span></span>

<span data-ttu-id="2c7d1-111">La **classe \_ GuestServiceInterfaceSettingDataComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2c7d1-111">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c7d1-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2c7d1-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7d1-113">Tipo di dati: **MSVM \_ GuestServiceInterfaceComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="2c7d1-113">Data type: **Msvm\_GuestServiceInterfaceComponentSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="2c7d1-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c7d1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c7d1-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="2c7d1-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2c7d1-116">[**\_ GuestServiceInterfaceComponentSettingData MSVM**](msvm-guestserviceinterfacecomponentsettingdata.md) che fa riferimento al componente dell'interfaccia del servizio Guest.</span><span class="sxs-lookup"><span data-stu-id="2c7d1-116">A [**Msvm\_GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) referencing the guest service interface component.</span></span>

</dd> <dt>

<span data-ttu-id="2c7d1-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2c7d1-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c7d1-118">Tipo di dati: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="2c7d1-118">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="2c7d1-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c7d1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c7d1-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="2c7d1-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2c7d1-121">Un [**\_ SettingData CIM**](cim-settingdata.md) che fa riferimento alla risorsa del servizio Guest.</span><span class="sxs-lookup"><span data-stu-id="2c7d1-121">A [**CIM\_SettingData**](cim-settingdata.md) that references the guest service resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c7d1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c7d1-122">Requirements</span></span>



| <span data-ttu-id="2c7d1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c7d1-123">Requirement</span></span> | <span data-ttu-id="2c7d1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2c7d1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7d1-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c7d1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2c7d1-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2c7d1-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2c7d1-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c7d1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2c7d1-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2c7d1-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2c7d1-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2c7d1-129">Namespace</span></span><br/>                | <span data-ttu-id="2c7d1-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2c7d1-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2c7d1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2c7d1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c7d1-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c7d1-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c7d1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2c7d1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c7d1-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c7d1-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2c7d1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c7d1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c7d1-136">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="2c7d1-136">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

