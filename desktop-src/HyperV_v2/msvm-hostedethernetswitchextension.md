---
description: Associa un compassatore Ethernet virtuale alle estensioni attualmente associate.
ms.assetid: d8c87fa2-6859-49ed-abd5-32a836b00e5a
title: Classe Msvm_HostedEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedEthernetSwitchExtension
- Msvm_HostedEthernetSwitchExtension.Antecedent
- Msvm_HostedEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cb952d42864fb6130ad6cbec09ef5eb68439f6a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752383"
---
# <a name="msvm_hostedethernetswitchextension-class"></a><span data-ttu-id="3a224-103">\_Classe MSVM HostedEthernetSwitchExtension</span><span class="sxs-lookup"><span data-stu-id="3a224-103">Msvm\_HostedEthernetSwitchExtension class</span></span>

<span data-ttu-id="3a224-104">Associa un compassatore Ethernet virtuale alle estensioni attualmente associate.</span><span class="sxs-lookup"><span data-stu-id="3a224-104">Associates a virtual Ethernet switch to the extensions currently bound to it.</span></span>

<span data-ttu-id="3a224-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3a224-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a224-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a224-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedEthernetSwitchExtension : CIM_HostedDependency
{
  Msvm_VirtualEthernetSwitch   REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3a224-107">Members</span><span class="sxs-lookup"><span data-stu-id="3a224-107">Members</span></span>

<span data-ttu-id="3a224-108">La **classe \_ HostedEthernetSwitchExtension di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3a224-108">The **Msvm\_HostedEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="3a224-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3a224-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a224-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3a224-110">Properties</span></span>

<span data-ttu-id="3a224-111">La **classe \_ HostedEthernetSwitchExtension di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3a224-111">The **Msvm\_HostedEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a224-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3a224-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a224-113">Tipo di dati: **[ **MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="3a224-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3a224-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a224-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a224-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="3a224-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3a224-116">Riferimento a un'istanza della classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) che rappresenta il Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="3a224-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="3a224-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="3a224-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a224-118">Tipo di dati: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="3a224-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3a224-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a224-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a224-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a224-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a224-121">Riferimento a un'istanza della classe [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) che rappresenta l'istanza dell'estensione del Commuter associata al Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="3a224-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the switch extension instance bound to the virtual switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a224-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a224-122">Requirements</span></span>



| <span data-ttu-id="3a224-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a224-123">Requirement</span></span> | <span data-ttu-id="3a224-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3a224-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a224-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a224-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3a224-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3a224-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3a224-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a224-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3a224-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3a224-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a224-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3a224-129">Namespace</span></span><br/>                | <span data-ttu-id="3a224-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3a224-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3a224-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3a224-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a224-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a224-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a224-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3a224-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a224-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a224-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

