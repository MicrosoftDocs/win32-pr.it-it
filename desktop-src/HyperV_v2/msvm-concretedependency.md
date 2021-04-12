---
description: Definisce l'associazione tra un'estensione del Commuter Ethernet installata e un'estensione del commutire Ethernet.
ms.assetid: 306658ed-03a4-49fa-8704-f4b83a4bdd4f
title: Classe Msvm_ConcreteDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteDependency
- Msvm_ConcreteDependency.Antecedent
- Msvm_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c74a8431b03389a106cd127933a2c78b842385f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226869"
---
# <a name="msvm_concretedependency-class"></a><span data-ttu-id="99937-103">\_Classe MSVM ConcreteDependency</span><span class="sxs-lookup"><span data-stu-id="99937-103">Msvm\_ConcreteDependency class</span></span>

<span data-ttu-id="99937-104">Definisce l'associazione tra un'estensione del Commuter Ethernet installata e un'estensione del commutire Ethernet.</span><span class="sxs-lookup"><span data-stu-id="99937-104">Defines the association between an installed Ethernet switch extension and an Ethernet switch extension.</span></span>

<span data-ttu-id="99937-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="99937-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="99937-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99937-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteDependency : CIM_ConcreteDependency
{
  Msvm_InstalledEthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension          REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="99937-107">Members</span><span class="sxs-lookup"><span data-stu-id="99937-107">Members</span></span>

<span data-ttu-id="99937-108">La **classe \_ ConcreteDependency di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="99937-108">The **Msvm\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="99937-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="99937-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99937-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="99937-110">Properties</span></span>

<span data-ttu-id="99937-111">La **classe \_ ConcreteDependency di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="99937-111">The **Msvm\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99937-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="99937-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99937-113">Tipo di dati: **[ **MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="99937-113">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="99937-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="99937-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99937-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="99937-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="99937-116">Riferimento a un'istanza della classe [**MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) che rappresenta un componente di estensione del Commuter Ethernet installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="99937-116">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents a virtual Ethernet switch extension component installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="99937-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="99937-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99937-118">Tipo di dati: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="99937-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="99937-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="99937-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99937-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="99937-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="99937-121">Riferimento a un'istanza della classe [**\_ EthernetSwitchExtension di MSVM**](msvm-ethernetswitchextension.md) che rappresenta l'occorrenza dell'attività **precedente** associata a un comswitch Ethernet virtuale specifico.</span><span class="sxs-lookup"><span data-stu-id="99937-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the occurrence of the **Antecedent** bound to a specific virtual Ethernet switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99937-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99937-122">Requirements</span></span>



| <span data-ttu-id="99937-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="99937-123">Requirement</span></span> | <span data-ttu-id="99937-124">Valore</span><span class="sxs-lookup"><span data-stu-id="99937-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99937-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99937-125">Minimum supported client</span></span><br/> | <span data-ttu-id="99937-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="99937-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="99937-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99937-127">Minimum supported server</span></span><br/> | <span data-ttu-id="99937-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="99937-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99937-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="99937-129">Namespace</span></span><br/>                | <span data-ttu-id="99937-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="99937-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="99937-131">MOF</span><span class="sxs-lookup"><span data-stu-id="99937-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99937-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99937-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="99937-133">DLL</span><span class="sxs-lookup"><span data-stu-id="99937-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99937-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="99937-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

