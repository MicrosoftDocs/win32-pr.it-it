---
description: Rappresenta un'associazione tra un punto di accesso al servizio e il dispositivo logico che lo implementa.
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Classe Msvm_FcDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc40f25e3b288155e713415aa512d629b538d1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307920"
---
# <a name="msvm_fcdevicesapimplementation-class"></a><span data-ttu-id="bcaf0-103">\_Classe MSVM FcDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="bcaf0-103">Msvm\_FcDeviceSAPImplementation class</span></span>

<span data-ttu-id="bcaf0-104">Rappresenta un'associazione tra un punto di accesso al servizio e il dispositivo logico che lo implementa.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="bcaf0-105">La cardinalità di questa associazione è molti-a-molti.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="bcaf0-106">Un punto di accesso al servizio (SAP) può essere fornito da più di un dispositivo logico, operando insieme.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="bcaf0-107">Qualsiasi dispositivo può fornire più di un SAP.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="bcaf0-108">Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino insieme per fornire il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="bcaf0-109">Se sono presenti implementazioni diverse di un SAP, ognuna di queste implementazioni genererà le singole creazioni di istanze dell'oggetto SAP.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="bcaf0-110">Queste singole creazioni di istanze avrebbero quindi le associazioni alle implementazioni univoche.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="bcaf0-111">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcaf0-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcaf0-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="bcaf0-113">Members</span><span class="sxs-lookup"><span data-stu-id="bcaf0-113">Members</span></span>

<span data-ttu-id="bcaf0-114">La **classe \_ FcDeviceSAPImplementation di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bcaf0-114">The **Msvm\_FcDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="bcaf0-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bcaf0-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bcaf0-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bcaf0-116">Properties</span></span>

<span data-ttu-id="bcaf0-117">La **classe \_ FcDeviceSAPImplementation di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-117">The **Msvm\_FcDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bcaf0-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="bcaf0-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcaf0-119">Tipo di dati: **CIM \_ FCPort**</span><span class="sxs-lookup"><span data-stu-id="bcaf0-119">Data type: **CIM\_FCPort**</span></span>
</dt> <dt>

<span data-ttu-id="bcaf0-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bcaf0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcaf0-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="bcaf0-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bcaf0-122">Riferimento a una classe derivata da **CIM \_ FCPort** che rappresenta il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-122">A reference to a class derived from **CIM\_FCPort** that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="bcaf0-123">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="bcaf0-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcaf0-124">Tipo di dati: **MSVM \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="bcaf0-124">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="bcaf0-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bcaf0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcaf0-126">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="bcaf0-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bcaf0-127">Riferimento a un'istanza della classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) che rappresenta il SAP che sta utilizzando l'attività **precedente**.</span><span class="sxs-lookup"><span data-stu-id="bcaf0-127">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcaf0-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcaf0-128">Requirements</span></span>



| <span data-ttu-id="bcaf0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcaf0-129">Requirement</span></span> | <span data-ttu-id="bcaf0-130">Valore</span><span class="sxs-lookup"><span data-stu-id="bcaf0-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcaf0-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcaf0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bcaf0-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bcaf0-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bcaf0-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcaf0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bcaf0-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bcaf0-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bcaf0-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bcaf0-135">Namespace</span></span><br/>                | <span data-ttu-id="bcaf0-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="bcaf0-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bcaf0-137">MOF</span><span class="sxs-lookup"><span data-stu-id="bcaf0-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcaf0-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcaf0-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcaf0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bcaf0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcaf0-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bcaf0-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

