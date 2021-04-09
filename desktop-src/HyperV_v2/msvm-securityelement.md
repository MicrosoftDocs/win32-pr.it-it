---
description: Rappresenta le impostazioni di sicurezza di runtime di un \_ ComputerSystem CIM.
ms.assetid: fa4448dc-9353-475f-ac9b-5c50f36360d8
title: Classe Msvm_SecurityElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityElement
- Msvm_SecurityElement.SystemCreationClassName
- Msvm_SecurityElement.SystemName
- Msvm_SecurityElement.CreationClassName
- Msvm_SecurityElement.Shielded
- Msvm_SecurityElement.EncryptStateAndVmMigrationTrafficEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f0de0fe1a515db0e7b1d8d49b96b61500703480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968761"
---
# <a name="msvm_securityelement-class"></a><span data-ttu-id="37d6b-103">\_Classe MSVM SecurityElement</span><span class="sxs-lookup"><span data-stu-id="37d6b-103">Msvm\_SecurityElement class</span></span>

<span data-ttu-id="37d6b-104">Rappresenta le impostazioni di sicurezza di runtime di un [**\_ ComputerSystem CIM**](cim-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="37d6b-104">Represents the runtime security settings of a [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="37d6b-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="37d6b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d6b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37d6b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityElement : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  boolean Shielded;
  boolean EncryptStateAndVmMigrationTrafficEnabled;
};
```

## <a name="members"></a><span data-ttu-id="37d6b-107">Members</span><span class="sxs-lookup"><span data-stu-id="37d6b-107">Members</span></span>

<span data-ttu-id="37d6b-108">La classe **MSVM \_ SecurityElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="37d6b-108">The **Msvm\_SecurityElement** class has these types of members:</span></span>

-   [<span data-ttu-id="37d6b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37d6b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37d6b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="37d6b-110">Properties</span></span>

<span data-ttu-id="37d6b-111">La classe **MSVM \_ SecurityElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="37d6b-111">The **Msvm\_SecurityElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37d6b-112">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37d6b-112">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d6b-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37d6b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d6b-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37d6b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37d6b-115">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="37d6b-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="37d6b-116">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="37d6b-116">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="37d6b-117">Quando viene usato con le altre proprietà chiave di questa classe, **CreationClassName** consente di identificare in modo univoco tutte le istanze di questa classe e delle relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="37d6b-117">When used with the other key properties of this class, **CreationClassName** allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="37d6b-118">**EncryptStateAndVmMigrationTrafficEnabled**</span><span class="sxs-lookup"><span data-stu-id="37d6b-118">**EncryptStateAndVmMigrationTrafficEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d6b-119">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="37d6b-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37d6b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37d6b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d6b-121">Indica se la macchina virtuale ha attualmente lo stato e il traffico di migrazione crittografati.</span><span class="sxs-lookup"><span data-stu-id="37d6b-121">Indicates whether the VM is currently having its state and migration traffic encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="37d6b-122">**Schermato**</span><span class="sxs-lookup"><span data-stu-id="37d6b-122">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d6b-123">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="37d6b-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37d6b-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37d6b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d6b-125">Indica se la macchina virtuale è attualmente schermata.</span><span class="sxs-lookup"><span data-stu-id="37d6b-125">Indicates whether the VM is currently shielded.</span></span>

</dd> <dt>

<span data-ttu-id="37d6b-126">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37d6b-126">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d6b-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37d6b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d6b-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37d6b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37d6b-129">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="37d6b-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="37d6b-130">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="37d6b-130">The creation class name of the scoping system.</span></span>

</dd> <dt>

<span data-ttu-id="37d6b-131">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="37d6b-131">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d6b-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="37d6b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d6b-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="37d6b-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37d6b-134">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="37d6b-134">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="37d6b-135">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="37d6b-135">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37d6b-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37d6b-136">Requirements</span></span>



| <span data-ttu-id="37d6b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="37d6b-137">Requirement</span></span> | <span data-ttu-id="37d6b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="37d6b-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37d6b-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37d6b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="37d6b-140">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="37d6b-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="37d6b-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37d6b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="37d6b-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="37d6b-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="37d6b-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="37d6b-143">Namespace</span></span><br/>                | <span data-ttu-id="37d6b-144">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="37d6b-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="37d6b-145">MOF</span><span class="sxs-lookup"><span data-stu-id="37d6b-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37d6b-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37d6b-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37d6b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="37d6b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37d6b-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37d6b-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37d6b-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37d6b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d6b-150">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="37d6b-150">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

