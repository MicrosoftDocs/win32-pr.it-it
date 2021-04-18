---
description: Rappresenta l'associazione tra un'estensione del Commuter Ethernet padre e un'estensione del Commuter Ethernet figlio.
ms.assetid: a0a60214-d85d-4c64-b720-1c34abc25287
title: Classe Msvm_ParentEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentEthernetSwitchExtension
- Msvm_ParentEthernetSwitchExtension.Antecedent
- Msvm_ParentEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8e215a01c9de98baa545dbb32b8279db4555f9cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318319"
---
# <a name="msvm_parentethernetswitchextension-class"></a><span data-ttu-id="793ea-103">\_Classe MSVM ParentEthernetSwitchExtension</span><span class="sxs-lookup"><span data-stu-id="793ea-103">Msvm\_ParentEthernetSwitchExtension class</span></span>

<span data-ttu-id="793ea-104">Rappresenta l'associazione tra un'estensione del Commuter Ethernet padre e un'estensione del Commuter Ethernet figlio.</span><span class="sxs-lookup"><span data-stu-id="793ea-104">Represents the association between a parent Ethernet switch extension and a child Ethernet switch extension.</span></span>

<span data-ttu-id="793ea-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="793ea-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="793ea-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="793ea-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentEthernetSwitchExtension : CIM_Dependency
{
  Msvm_EthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="793ea-107">Members</span><span class="sxs-lookup"><span data-stu-id="793ea-107">Members</span></span>

<span data-ttu-id="793ea-108">La **classe \_ ParentEthernetSwitchExtension di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="793ea-108">The **Msvm\_ParentEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="793ea-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="793ea-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="793ea-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="793ea-110">Properties</span></span>

<span data-ttu-id="793ea-111">La **classe \_ ParentEthernetSwitchExtension di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="793ea-111">The **Msvm\_ParentEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="793ea-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="793ea-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793ea-113">Tipo di dati: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="793ea-113">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="793ea-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793ea-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="793ea-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="793ea-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="793ea-116">Riferimento a un'istanza della classe [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) che rappresenta l'estensione del comcambio padre.</span><span class="sxs-lookup"><span data-stu-id="793ea-116">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the parent switch extension.</span></span>

</dd> <dt>

<span data-ttu-id="793ea-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="793ea-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="793ea-118">Tipo di dati: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="793ea-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="793ea-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="793ea-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="793ea-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="793ea-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="793ea-121">Riferimento a un'istanza della classe [**\_ EthernetSwitchExtension di MSVM**](msvm-ethernetswitchextension.md) che rappresenta l'estensione del commutire figlio.</span><span class="sxs-lookup"><span data-stu-id="793ea-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the child switch extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="793ea-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="793ea-122">Requirements</span></span>



| <span data-ttu-id="793ea-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="793ea-123">Requirement</span></span> | <span data-ttu-id="793ea-124">Valore</span><span class="sxs-lookup"><span data-stu-id="793ea-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="793ea-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="793ea-125">Minimum supported client</span></span><br/> | <span data-ttu-id="793ea-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="793ea-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="793ea-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="793ea-127">Minimum supported server</span></span><br/> | <span data-ttu-id="793ea-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="793ea-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="793ea-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="793ea-129">Namespace</span></span><br/>                | <span data-ttu-id="793ea-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="793ea-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="793ea-131">MOF</span><span class="sxs-lookup"><span data-stu-id="793ea-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="793ea-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="793ea-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="793ea-133">DLL</span><span class="sxs-lookup"><span data-stu-id="793ea-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="793ea-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="793ea-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

