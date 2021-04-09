---
description: Contiene un riepilogo delle informazioni sul sistema di computer virtuale specificato.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Classe Msvm_ComputerSystemSummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35248bcfa14609e8db25b148088b6feb8d161116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879297"
---
# <a name="msvm_computersystemsummaryinformation-class"></a><span data-ttu-id="02403-103">\_Classe MSVM ComputerSystemSummaryInformation</span><span class="sxs-lookup"><span data-stu-id="02403-103">Msvm\_ComputerSystemSummaryInformation class</span></span>

<span data-ttu-id="02403-104">Contiene un riepilogo delle informazioni sul sistema di computer virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="02403-104">Contains an information summary about the specified virtual computer system.</span></span>

<span data-ttu-id="02403-105">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="02403-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="02403-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02403-106">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="02403-107">Members</span><span class="sxs-lookup"><span data-stu-id="02403-107">Members</span></span>

<span data-ttu-id="02403-108">La **classe \_ ComputerSystemSummaryInformation di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="02403-108">The **Msvm\_ComputerSystemSummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="02403-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02403-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02403-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02403-110">Properties</span></span>

<span data-ttu-id="02403-111">La **classe \_ ComputerSystemSummaryInformation di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="02403-111">The **Msvm\_ComputerSystemSummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02403-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="02403-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02403-113">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="02403-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="02403-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="02403-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02403-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="02403-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="02403-116">Oggetto [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta un'istanza della rappresentazione normalizzata della risorsa gestita.</span><span class="sxs-lookup"><span data-stu-id="02403-116">A [**CIM\_ComputerSystem**](cim-computersystem.md) object that is an instance in the normalized representation of the managed resource.</span></span>

> [!Note]
>
> <span data-ttu-id="02403-117">DataType aggiornato da [**MSVM \_ ComputerSystem**](msvm-computersystem.md) in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="02403-117">Datatype upgraded from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="02403-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="02403-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02403-119">Tipo di dati: **MSVM \_ SummaryInformationBase**</span><span class="sxs-lookup"><span data-stu-id="02403-119">Data type: **Msvm\_SummaryInformationBase**</span></span>
</dt> <dt>

<span data-ttu-id="02403-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="02403-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02403-121">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="02403-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="02403-122">Istanza di [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) che rappresenta una vista denormalizzata o aggregata della risorsa gestita rappresentata dal [**\_ ComputerSystem MSVM**](msvm-computersystem.md) a cui fa riferimento la proprietà precedente.</span><span class="sxs-lookup"><span data-stu-id="02403-122">An instance of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) that represents a de-normalized or aggregate view of the managed resource that is represented by the [**Msvm\_ComputerSystem**](msvm-computersystem.md) referenced by the Antecedent property.</span></span>

> [!Note]
>
> <span data-ttu-id="02403-123">DataType aggiornato da [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="02403-123">Datatype updated from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) in Windows 10, version 1703.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02403-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02403-124">Requirements</span></span>



| <span data-ttu-id="02403-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="02403-125">Requirement</span></span> | <span data-ttu-id="02403-126">Valore</span><span class="sxs-lookup"><span data-stu-id="02403-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02403-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02403-127">Minimum supported client</span></span><br/> | <span data-ttu-id="02403-128">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="02403-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="02403-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02403-129">Minimum supported server</span></span><br/> | <span data-ttu-id="02403-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="02403-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="02403-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="02403-131">Namespace</span></span><br/>                | <span data-ttu-id="02403-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="02403-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="02403-133">MOF</span><span class="sxs-lookup"><span data-stu-id="02403-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02403-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02403-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02403-135">DLL</span><span class="sxs-lookup"><span data-stu-id="02403-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02403-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02403-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02403-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02403-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02403-138">**\_ELEMENTVIEW CIM**</span><span class="sxs-lookup"><span data-stu-id="02403-138">**CIM\_ElementView**</span></span>](cim-elementview.md)
</dt> </dl>

 

