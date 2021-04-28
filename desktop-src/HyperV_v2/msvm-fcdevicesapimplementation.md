---
description: "Msvm_FcDeviceSAPImplementation classe : rappresenta un'associazione tra un punto di accesso del servizio e il dispositivo logico che lo implementa."
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Msvm_FcDeviceSAPImplementation classe
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
ms.openlocfilehash: b0df7a198b3ee52d131800073f8be30d51d93181
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119029"
---
# <a name="msvm_fcdevicesapimplementation-class"></a><span data-ttu-id="6f8a2-103">Classe Msvm \_ FcDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="6f8a2-103">Msvm\_FcDeviceSAPImplementation class</span></span>

<span data-ttu-id="6f8a2-104">Rappresenta un'associazione tra un punto di accesso del servizio e il dispositivo logico che lo implementa.</span><span class="sxs-lookup"><span data-stu-id="6f8a2-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="6f8a2-105">La cardinalità di questa associazione è molti-a-molti.</span><span class="sxs-lookup"><span data-stu-id="6f8a2-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="6f8a2-106">Un punto di accesso al servizio (SAP) può essere fornito da più di un dispositivo logico, operando in combinazione.</span><span class="sxs-lookup"><span data-stu-id="6f8a2-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="6f8a2-107">Qualsiasi dispositivo può fornire più di un SAP.</span><span class="sxs-lookup"><span data-stu-id="6f8a2-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="6f8a2-108">Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino in combinazione per fornire il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="6f8a2-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="6f8a2-109">Se esistono implementazioni diverse di sap, ognuna di queste implementazioni comporterebbe la creazione di singole istanze dell'oggetto SAP.</span><span class="sxs-lookup"><span data-stu-id="6f8a2-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="6f8a2-110">Queste singole istanze hanno quindi associazioni alle implementazioni univoche.</span><span class="sxs-lookup"><span data-stu-id="6f8a2-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="6f8a2-111">La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6f8a2-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f8a2-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f8a2-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6f8a2-113">Members</span><span class="sxs-lookup"><span data-stu-id="6f8a2-113">Members</span></span>

<span data-ttu-id="6f8a2-114">La **classe Msvm \_ FcDeviceSAPImplementation** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6f8a2-114">The **Msvm\_FcDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="6f8a2-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f8a2-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f8a2-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f8a2-116">Properties</span></span>

<span data-ttu-id="6f8a2-117">La **classe Msvm \_ FcDeviceSAPImplementation** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6f8a2-117">The **Msvm\_FcDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f8a2-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="6f8a2-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f8a2-119">Tipo di dati: **CIM \_ FCPort**</span><span class="sxs-lookup"><span data-stu-id="6f8a2-119">Data type: **CIM\_FCPort**</span></span>
</dt> <dt>

<span data-ttu-id="6f8a2-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f8a2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f8a2-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="6f8a2-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6f8a2-122">Riferimento a una classe derivata da **CIM \_ FCPort** che rappresenta il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="6f8a2-122">A reference to a class derived from **CIM\_FCPort** that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="6f8a2-123">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="6f8a2-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f8a2-124">Tipo di dati: **Msvm \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="6f8a2-124">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="6f8a2-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f8a2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f8a2-126">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")</span><span class="sxs-lookup"><span data-stu-id="6f8a2-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6f8a2-127">Riferimento a un'istanza della [**classe Msvm \_ FcEndpoint**](msvm-fcendpoint.md) che rappresenta il sap che usa **l'attività precedente.**</span><span class="sxs-lookup"><span data-stu-id="6f8a2-127">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f8a2-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f8a2-128">Requirements</span></span>



| <span data-ttu-id="6f8a2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f8a2-129">Requirement</span></span> | <span data-ttu-id="6f8a2-130">Valore</span><span class="sxs-lookup"><span data-stu-id="6f8a2-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f8a2-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f8a2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6f8a2-132">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f8a2-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6f8a2-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f8a2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6f8a2-134">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f8a2-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f8a2-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6f8a2-135">Namespace</span></span><br/>                | <span data-ttu-id="6f8a2-136">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="6f8a2-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6f8a2-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6f8a2-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f8a2-138"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f8a2-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f8a2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6f8a2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f8a2-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f8a2-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

