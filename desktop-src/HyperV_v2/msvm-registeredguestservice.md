---
description: Rappresenta un'associazione tra un'istanza di MSVM \_ GuestServiceInterfaceComponent e un'istanza di MSVM \_ GuestService, che rappresenta un servizio in esecuzione nel guest.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Classe Msvm_RegisteredGuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 850d7f081b070fd34ef11bc56e8cd1f914e498b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756893"
---
# <a name="msvm_registeredguestservice-class"></a><span data-ttu-id="3360d-103">\_Classe MSVM RegisteredGuestService</span><span class="sxs-lookup"><span data-stu-id="3360d-103">Msvm\_RegisteredGuestService class</span></span>

<span data-ttu-id="3360d-104">Rappresenta un'associazione tra un'istanza di [**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) e un'istanza di [**MSVM \_ GuestService**](msvm-guestservice.md), che rappresenta un servizio in esecuzione nel guest.</span><span class="sxs-lookup"><span data-stu-id="3360d-104">Represents an association between an instance of [**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) and an instance of [**Msvm\_GuestService**](msvm-guestservice.md), which represents a service running in the guest.</span></span> <span data-ttu-id="3360d-105">Questa classe deriva dalla classe di [**\_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .</span><span class="sxs-lookup"><span data-stu-id="3360d-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="3360d-106">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3360d-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3360d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3360d-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3360d-108">Members</span><span class="sxs-lookup"><span data-stu-id="3360d-108">Members</span></span>

<span data-ttu-id="3360d-109">La **classe \_ RegisteredGuestService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3360d-109">The **Msvm\_RegisteredGuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="3360d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3360d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3360d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3360d-111">Properties</span></span>

<span data-ttu-id="3360d-112">La **classe \_ RegisteredGuestService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3360d-112">The **Msvm\_RegisteredGuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3360d-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3360d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3360d-114">Tipo di dati: **[ **MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="3360d-114">Data type: **[**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3360d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3360d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3360d-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="3360d-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3360d-117">Riferimento al componente dell'interfaccia del servizio Guest in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="3360d-117">Reference to the guest service interface component in this association.</span></span>

</dd> <dt>

<span data-ttu-id="3360d-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="3360d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3360d-119">Tipo di dati: **[ **MSVM \_ GuestService**](msvm-guestservice.md)**</span><span class="sxs-lookup"><span data-stu-id="3360d-119">Data type: **[**Msvm\_GuestService**](msvm-guestservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3360d-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3360d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3360d-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. dependent")</span><span class="sxs-lookup"><span data-stu-id="3360d-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3360d-122">Riferimento al servizio Guest registrato che dipende dalla proprietà **precedente** .</span><span class="sxs-lookup"><span data-stu-id="3360d-122">Reference to the registered guest service that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3360d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3360d-123">Requirements</span></span>



| <span data-ttu-id="3360d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3360d-124">Requirement</span></span> | <span data-ttu-id="3360d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3360d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3360d-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3360d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3360d-127">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3360d-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3360d-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3360d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3360d-129">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3360d-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3360d-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3360d-130">Namespace</span></span><br/>                | <span data-ttu-id="3360d-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3360d-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3360d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="3360d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3360d-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3360d-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3360d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3360d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3360d-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3360d-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3360d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3360d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3360d-137">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="3360d-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="3360d-138">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="3360d-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

