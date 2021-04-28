---
description: "Msvm_EthernetDeviceSAPImplementation classe : rappresenta un'associazione tra un punto di accesso del servizio e il dispositivo logico che lo implementa."
ms.assetid: C0DDB199-AD97-4DD7-8056-BD6BD0CECFA8
title: Msvm_EthernetDeviceSAPImplementation classe
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
ms.openlocfilehash: fddce9505ca2f8692044239d294904eb17c95ffa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111949"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a><span data-ttu-id="6680e-103">Classe Msvm \_ EthernetDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="6680e-103">Msvm\_EthernetDeviceSAPImplementation class</span></span>

<span data-ttu-id="6680e-104">Rappresenta un'associazione tra un punto di accesso del servizio e il dispositivo logico che lo implementa.</span><span class="sxs-lookup"><span data-stu-id="6680e-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="6680e-105">La cardinalità di questa associazione è molti-a-molti.</span><span class="sxs-lookup"><span data-stu-id="6680e-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="6680e-106">Un punto di accesso al servizio (SAP) può essere fornito da più di un dispositivo logico, operando in combinazione.</span><span class="sxs-lookup"><span data-stu-id="6680e-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="6680e-107">Qualsiasi dispositivo può fornire più di un SAP.</span><span class="sxs-lookup"><span data-stu-id="6680e-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="6680e-108">Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino in combinazione per fornire il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="6680e-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="6680e-109">Se esistono implementazioni diverse di sap, ognuna di queste implementazioni comporterebbe la creazione di singole istanze dell'oggetto SAP.</span><span class="sxs-lookup"><span data-stu-id="6680e-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="6680e-110">Queste singole istanze hanno quindi associazioni alle implementazioni univoche.</span><span class="sxs-lookup"><span data-stu-id="6680e-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="6680e-111">La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6680e-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6680e-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6680e-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6680e-113">Members</span><span class="sxs-lookup"><span data-stu-id="6680e-113">Members</span></span>

<span data-ttu-id="6680e-114">La **classe Msvm \_ EthernetDeviceSAPImplementation** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6680e-114">The **Msvm\_EthernetDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="6680e-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6680e-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6680e-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6680e-116">Properties</span></span>

<span data-ttu-id="6680e-117">La **classe Msvm \_ EthernetDeviceSAPImplementation** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6680e-117">The **Msvm\_EthernetDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6680e-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="6680e-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6680e-119">Tipo di dati: **[ **CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span><span class="sxs-lookup"><span data-stu-id="6680e-119">Data type: **[**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span></span>
</dt> <dt>

<span data-ttu-id="6680e-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6680e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6680e-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="6680e-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6680e-122">Riferimento a una classe derivata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) che rappresenta il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="6680e-122">A reference to a class derived from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="6680e-123">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="6680e-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6680e-124">Tipo di dati: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="6680e-124">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6680e-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6680e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6680e-126">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")</span><span class="sxs-lookup"><span data-stu-id="6680e-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6680e-127">Riferimento a un'istanza della [**classe Msvm \_ LANEndpoint**](msvm-lanendpoint.md) che rappresenta il sap che usa **antecedente**.</span><span class="sxs-lookup"><span data-stu-id="6680e-127">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6680e-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6680e-128">Requirements</span></span>



| <span data-ttu-id="6680e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6680e-129">Requirement</span></span> | <span data-ttu-id="6680e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="6680e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6680e-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6680e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6680e-132">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6680e-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6680e-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6680e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6680e-134">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="6680e-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6680e-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6680e-135">Namespace</span></span><br/>                | <span data-ttu-id="6680e-136">Virtualizzazione \\ radice \\ V2</span><span class="sxs-lookup"><span data-stu-id="6680e-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6680e-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6680e-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6680e-138"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="6680e-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6680e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6680e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6680e-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6680e-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

