---
description: Rappresenta un'associazione tra un punto di accesso al servizio e il dispositivo logico che lo implementa.
ms.assetid: C0DDB199-AD97-4DD7-8056-BD6BD0CECFA8
title: Classe Msvm_EthernetDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetDeviceSAPImplementation
- Msvm_EthernetDeviceSAPImplementation.Antecedent
- Msvm_EthernetDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 96290eb0d572f4848fbf3805a44ce0ae173892c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345786"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a><span data-ttu-id="7c93a-103">\_Classe MSVM EthernetDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="7c93a-103">Msvm\_EthernetDeviceSAPImplementation class</span></span>

<span data-ttu-id="7c93a-104">Rappresenta un'associazione tra un punto di accesso al servizio e il dispositivo logico che lo implementa.</span><span class="sxs-lookup"><span data-stu-id="7c93a-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="7c93a-105">La cardinalità di questa associazione è molti-a-molti.</span><span class="sxs-lookup"><span data-stu-id="7c93a-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="7c93a-106">Un punto di accesso al servizio (SAP) può essere fornito da più di un dispositivo logico, operando insieme.</span><span class="sxs-lookup"><span data-stu-id="7c93a-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="7c93a-107">Qualsiasi dispositivo può fornire più di un SAP.</span><span class="sxs-lookup"><span data-stu-id="7c93a-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="7c93a-108">Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino insieme per fornire il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="7c93a-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="7c93a-109">Se sono presenti implementazioni diverse di un SAP, ognuna di queste implementazioni genererà le singole creazioni di istanze dell'oggetto SAP.</span><span class="sxs-lookup"><span data-stu-id="7c93a-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="7c93a-110">Queste singole creazioni di istanze avrebbero quindi le associazioni alle implementazioni univoche.</span><span class="sxs-lookup"><span data-stu-id="7c93a-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="7c93a-111">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7c93a-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c93a-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c93a-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7c93a-113">Members</span><span class="sxs-lookup"><span data-stu-id="7c93a-113">Members</span></span>

<span data-ttu-id="7c93a-114">La **classe \_ EthernetDeviceSAPImplementation di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7c93a-114">The **Msvm\_EthernetDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="7c93a-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7c93a-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c93a-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7c93a-116">Properties</span></span>

<span data-ttu-id="7c93a-117">La **classe \_ EthernetDeviceSAPImplementation di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7c93a-117">The **Msvm\_EthernetDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c93a-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="7c93a-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c93a-119">Tipo di dati: **[ **CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span><span class="sxs-lookup"><span data-stu-id="7c93a-119">Data type: **[**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span></span>
</dt> <dt>

<span data-ttu-id="7c93a-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c93a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c93a-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="7c93a-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7c93a-122">Riferimento a una classe derivata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) che rappresenta il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7c93a-122">A reference to a class derived from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="7c93a-123">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="7c93a-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c93a-124">Tipo di dati: **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="7c93a-124">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="7c93a-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c93a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c93a-126">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="7c93a-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7c93a-127">Riferimento a un'istanza della classe [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) che rappresenta il SAP che sta utilizzando l'attività **precedente**.</span><span class="sxs-lookup"><span data-stu-id="7c93a-127">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c93a-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c93a-128">Requirements</span></span>



| <span data-ttu-id="7c93a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c93a-129">Requirement</span></span> | <span data-ttu-id="7c93a-130">Valore</span><span class="sxs-lookup"><span data-stu-id="7c93a-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c93a-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c93a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7c93a-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7c93a-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7c93a-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c93a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7c93a-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7c93a-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c93a-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7c93a-135">Namespace</span></span><br/>                | <span data-ttu-id="7c93a-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7c93a-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7c93a-137">MOF</span><span class="sxs-lookup"><span data-stu-id="7c93a-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c93a-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c93a-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c93a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7c93a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c93a-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7c93a-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

