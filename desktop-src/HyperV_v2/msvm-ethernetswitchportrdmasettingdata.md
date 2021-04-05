---
description: Rappresenta i dati dell'impostazione della funzionalità RDMA della porta.
ms.assetid: a9b8c98f-194e-4eec-8d4a-961b1a439e62
title: Classe Msvm_EthernetSwitchPortRdmaSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRdmaSettingData
- Msvm_EthernetSwitchPortRdmaSettingData.RdmaOffloadWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98d4f06923bfcfa16d564b296e3b544d9aad6275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885864"
---
# <a name="msvm_ethernetswitchportrdmasettingdata-class"></a><span data-ttu-id="37c87-103">\_Classe MSVM EthernetSwitchPortRdmaSettingData</span><span class="sxs-lookup"><span data-stu-id="37c87-103">Msvm\_EthernetSwitchPortRdmaSettingData class</span></span>

<span data-ttu-id="37c87-104">Rappresenta i dati dell'impostazione della funzionalità RDMA della porta.</span><span class="sxs-lookup"><span data-stu-id="37c87-104">Represents the port RDMA feature setting data.</span></span>

<span data-ttu-id="37c87-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="37c87-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37c87-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37c87-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("7A498FC4-8572-4FDC-92AB-7A6FC7042D53"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Rdma Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRdmaSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32 RdmaOffloadWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="37c87-107">Members</span><span class="sxs-lookup"><span data-stu-id="37c87-107">Members</span></span>

<span data-ttu-id="37c87-108">La **classe \_ EthernetSwitchPortRdmaSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="37c87-108">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="37c87-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37c87-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37c87-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37c87-110">Properties</span></span>

<span data-ttu-id="37c87-111">La **classe \_ EthernetSwitchPortRdmaSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="37c87-111">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37c87-112">**RdmaOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="37c87-112">**RdmaOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37c87-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37c87-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37c87-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="37c87-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37c87-115">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37c87-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37c87-116">Il peso assegnato a questa porta per RDMA Guest.</span><span class="sxs-lookup"><span data-stu-id="37c87-116">The weight assigned to this port for Guest RDMA.</span></span> <span data-ttu-id="37c87-117">Il peso è l'importanza relativa durante l'assegnazione delle risorse RDMA.</span><span class="sxs-lookup"><span data-stu-id="37c87-117">The weight is the relative importance when assigning RDMA resources.</span></span> <span data-ttu-id="37c87-118">L'impostazione della proprietà **RdmaOffloadWeight** su 0 Disabilita RDMA sulla porta.</span><span class="sxs-lookup"><span data-stu-id="37c87-118">Setting the **RdmaOffloadWeight** property to 0 disables RDMA on the port.</span></span> <span data-ttu-id="37c87-119">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="37c87-119">The default is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37c87-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37c87-120">Requirements</span></span>



| <span data-ttu-id="37c87-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="37c87-121">Requirement</span></span> | <span data-ttu-id="37c87-122">Valore</span><span class="sxs-lookup"><span data-stu-id="37c87-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c87-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37c87-123">Minimum supported client</span></span><br/> | <span data-ttu-id="37c87-124">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="37c87-124">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="37c87-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37c87-125">Minimum supported server</span></span><br/> | <span data-ttu-id="37c87-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="37c87-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="37c87-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="37c87-127">Namespace</span></span><br/>                | <span data-ttu-id="37c87-128">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="37c87-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="37c87-129">MOF</span><span class="sxs-lookup"><span data-stu-id="37c87-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37c87-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37c87-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37c87-131">DLL</span><span class="sxs-lookup"><span data-stu-id="37c87-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37c87-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37c87-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37c87-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37c87-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c87-134">**\_EthernetSwitchPortFeatureSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="37c87-134">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

 




