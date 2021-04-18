---
description: Associazione tra un'istanza della \_ classe MSVM EthernetSwitchPort e un'istanza della \_ classe MSVM EthernetPortData che rappresenta i dati raccolti sulla porta da un'estensione del commutire.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Classe Msvm_EthernetPortInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c78dca7adedcf52d93530efdab0da6113855c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312913"
---
# <a name="msvm_ethernetportinfo-class"></a><span data-ttu-id="b4ac3-103">\_Classe MSVM EthernetPortInfo</span><span class="sxs-lookup"><span data-stu-id="b4ac3-103">Msvm\_EthernetPortInfo class</span></span>

<span data-ttu-id="b4ac3-104">Associazione tra un'istanza della classe [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) e un'istanza della classe [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md) che rappresenta i dati raccolti sulla porta da un'estensione del commutire.</span><span class="sxs-lookup"><span data-stu-id="b4ac3-104">An association between an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class and an instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents data gathered about the port by a switch extension.</span></span>

<span data-ttu-id="b4ac3-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b4ac3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ac3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4ac3-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b4ac3-107">Members</span><span class="sxs-lookup"><span data-stu-id="b4ac3-107">Members</span></span>

<span data-ttu-id="b4ac3-108">La **classe \_ EthernetPortInfo di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b4ac3-108">The **Msvm\_EthernetPortInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="b4ac3-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4ac3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4ac3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4ac3-110">Properties</span></span>

<span data-ttu-id="b4ac3-111">La **classe \_ EthernetPortInfo di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b4ac3-111">The **Msvm\_EthernetPortInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4ac3-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b4ac3-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4ac3-113">Tipo di dati: **MSVM \_ EthernetSwitchPort**</span><span class="sxs-lookup"><span data-stu-id="b4ac3-113">Data type: **Msvm\_EthernetSwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="b4ac3-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4ac3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4ac3-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b4ac3-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b4ac3-116">Istanza della classe [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) che rappresenta la porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="b4ac3-116">An instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="b4ac3-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="b4ac3-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4ac3-118">Tipo di dati: **MSVM \_ EthernetPortData**</span><span class="sxs-lookup"><span data-stu-id="b4ac3-118">Data type: **Msvm\_EthernetPortData**</span></span>
</dt> <dt>

<span data-ttu-id="b4ac3-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4ac3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4ac3-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. dependent")</span><span class="sxs-lookup"><span data-stu-id="b4ac3-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b4ac3-121">Istanza della classe [**\_ EthernetPortData MSVM**](msvm-ethernetportdata.md) che rappresenta i dati della porta.</span><span class="sxs-lookup"><span data-stu-id="b4ac3-121">An instance of the [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md) class that represents the port data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4ac3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4ac3-122">Requirements</span></span>



| <span data-ttu-id="b4ac3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4ac3-123">Requirement</span></span> | <span data-ttu-id="b4ac3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b4ac3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ac3-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4ac3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b4ac3-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b4ac3-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b4ac3-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4ac3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b4ac3-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b4ac3-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b4ac3-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b4ac3-129">Namespace</span></span><br/>                | <span data-ttu-id="b4ac3-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b4ac3-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b4ac3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b4ac3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4ac3-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4ac3-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4ac3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b4ac3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4ac3-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b4ac3-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

