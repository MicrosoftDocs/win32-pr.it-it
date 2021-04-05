---
description: Stabilire una relazione tra un'istanza della classe MSVM \_ EmulatedEthernetPortSettingData o MSVM \_ SyntheticEthernetPortSettingData con un'istanza della \_ classe MSVM GuestNetworkAdapterConfiguration.
ms.assetid: 82262e67-1e72-4bad-974e-f18d00a94c3d
title: Classe Msvm_SettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingDataComponent
- Msvm_SettingDataComponent.GroupComponent
- Msvm_SettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18ed2d4f37b88509a7517861a9b9d842be86bd97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967822"
---
# <a name="msvm_settingdatacomponent-class"></a><span data-ttu-id="c093c-103">\_Classe MSVM SettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="c093c-103">Msvm\_SettingDataComponent class</span></span>

<span data-ttu-id="c093c-104">Stabilire una relazione tra un'istanza della classe [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) con un'istanza della classe [**MSVM \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="c093c-104">Establish a relationship between an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class with an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span>

<span data-ttu-id="c093c-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c093c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c093c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c093c-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData     REF GroupComponent;
  Msvm_GuestNetworkAdapterConfiguration REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="c093c-107">Members</span><span class="sxs-lookup"><span data-stu-id="c093c-107">Members</span></span>

<span data-ttu-id="c093c-108">La **classe \_ SettingDataComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c093c-108">The **Msvm\_SettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="c093c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c093c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c093c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c093c-110">Properties</span></span>

<span data-ttu-id="c093c-111">La **classe \_ SettingDataComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c093c-111">The **Msvm\_SettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c093c-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c093c-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c093c-113">Tipo di dati: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="c093c-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="c093c-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c093c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c093c-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**aggregazione**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c093c-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c093c-116">Riferimento a un'istanza della classe [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) che rappresenta una porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c093c-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="c093c-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c093c-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c093c-118">Tipo di dati: **[ **MSVM \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span><span class="sxs-lookup"><span data-stu-id="c093c-118">Data type: **[**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c093c-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c093c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c093c-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="c093c-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c093c-121">Riferimento a un'istanza della classe [**MSVM \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) che rappresenta una configurazione della scheda di rete Guest.</span><span class="sxs-lookup"><span data-stu-id="c093c-121">A reference to an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class that represents a guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c093c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c093c-122">Requirements</span></span>



| <span data-ttu-id="c093c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c093c-123">Requirement</span></span> | <span data-ttu-id="c093c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c093c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c093c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c093c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c093c-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c093c-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c093c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c093c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c093c-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c093c-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c093c-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c093c-129">Namespace</span></span><br/>                | <span data-ttu-id="c093c-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c093c-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c093c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c093c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c093c-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c093c-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c093c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c093c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c093c-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c093c-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

