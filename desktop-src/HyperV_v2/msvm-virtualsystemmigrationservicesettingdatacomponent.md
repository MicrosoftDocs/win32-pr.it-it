---
description: Associazione utilizzata per rappresentare le impostazioni della rete di migrazione del sistema virtuale del servizio di migrazione del sistema virtuale.
ms.assetid: 5704dce7-1db3-4049-8c61-58bfa9596766
title: Classe Msvm_VirtualSystemMigrationServiceSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingDataComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.GroupComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ba69ebd6cfd50b30923db2ecc87e7e5aeebcaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305987"
---
# <a name="msvm_virtualsystemmigrationservicesettingdatacomponent-class"></a><span data-ttu-id="f1e99-103">\_Classe MSVM VirtualSystemMigrationServiceSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="f1e99-103">Msvm\_VirtualSystemMigrationServiceSettingDataComponent class</span></span>

<span data-ttu-id="f1e99-104">Associazione utilizzata per rappresentare le impostazioni della rete di migrazione del sistema virtuale del servizio di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1e99-104">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span>

<span data-ttu-id="f1e99-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f1e99-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e99-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1e99-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingDataComponent : CIM_Component
{
  Msvm_VirtualSystemMigrationServiceSettingData REF GroupComponent;
  Msvm_VirtualSystemMigrationNetworkSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="f1e99-107">Members</span><span class="sxs-lookup"><span data-stu-id="f1e99-107">Members</span></span>

<span data-ttu-id="f1e99-108">La **classe \_ VirtualSystemMigrationServiceSettingDataComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f1e99-108">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="f1e99-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1e99-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1e99-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1e99-110">Properties</span></span>

<span data-ttu-id="f1e99-111">La **classe \_ VirtualSystemMigrationServiceSettingDataComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f1e99-111">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1e99-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f1e99-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1e99-113">Tipo di dati: **MSVM \_ VirtualSystemMigrationServiceSettingData**</span><span class="sxs-lookup"><span data-stu-id="f1e99-113">Data type: **Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="f1e99-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1e99-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1e99-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**aggregazione**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f1e99-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f1e99-116">Riferimento a un'istanza della classe [**MSVM \_ VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) che rappresenta le impostazioni del servizio di migrazione.</span><span class="sxs-lookup"><span data-stu-id="f1e99-116">A reference to an instance of the [**Msvm\_VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) class that represents the migration service settings.</span></span>

</dd> <dt>

<span data-ttu-id="f1e99-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f1e99-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1e99-118">Tipo di dati: **MSVM \_ VirtualSystemMigrationNetworkSettingData**</span><span class="sxs-lookup"><span data-stu-id="f1e99-118">Data type: **Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="f1e99-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1e99-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1e99-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="f1e99-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f1e99-121">Riferimento a un'istanza della classe [**MSVM \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) che rappresenta le impostazioni della rete di migrazione.</span><span class="sxs-lookup"><span data-stu-id="f1e99-121">A reference to an instance of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represents the migration network settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1e99-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1e99-122">Requirements</span></span>



| <span data-ttu-id="f1e99-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1e99-123">Requirement</span></span> | <span data-ttu-id="f1e99-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f1e99-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e99-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1e99-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e99-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f1e99-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f1e99-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1e99-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e99-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f1e99-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1e99-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f1e99-129">Namespace</span></span><br/>                | <span data-ttu-id="f1e99-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1e99-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f1e99-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f1e99-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1e99-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1e99-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1e99-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f1e99-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1e99-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1e99-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

