---
description: Associazione tra un punto di accesso al servizio (SAP) e la relativa modalità di implementazione.
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Classe Msvm_WiFiDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debec96efb93e60ec18d75b62ffa0d13b0e0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879106"
---
# <a name="msvm_wifidevicesapimplementation-class"></a><span data-ttu-id="2e505-103">\_Classe MSVM WiFiDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="2e505-103">Msvm\_WiFiDeviceSAPImplementation class</span></span>

<span data-ttu-id="2e505-104">Associazione tra un punto di accesso al servizio (SAP) e la relativa modalità di implementazione.</span><span class="sxs-lookup"><span data-stu-id="2e505-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="2e505-105">La cardinalità di questa associazione è molti-a-molti.</span><span class="sxs-lookup"><span data-stu-id="2e505-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="2e505-106">Un SAP può essere fornito da più di un dispositivo logico, operando insieme.</span><span class="sxs-lookup"><span data-stu-id="2e505-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="2e505-107">Qualsiasi dispositivo può fornire più di un SAP.</span><span class="sxs-lookup"><span data-stu-id="2e505-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="2e505-108">Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino insieme per fornire il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="2e505-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="2e505-109">Se sono presenti implementazioni diverse di un SAP, ognuna di queste implementazioni genererà le singole creazioni di istanze dell'oggetto SAP.</span><span class="sxs-lookup"><span data-stu-id="2e505-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="2e505-110">Queste singole creazioni di istanze avrebbero quindi le associazioni alle implementazioni univoche.</span><span class="sxs-lookup"><span data-stu-id="2e505-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="2e505-111">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2e505-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e505-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e505-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2e505-113">Members</span><span class="sxs-lookup"><span data-stu-id="2e505-113">Members</span></span>

<span data-ttu-id="2e505-114">La **classe \_ WiFiDeviceSAPImplementation di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2e505-114">The **Msvm\_WiFiDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="2e505-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2e505-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e505-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2e505-116">Properties</span></span>

<span data-ttu-id="2e505-117">La **classe \_ WiFiDeviceSAPImplementation di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2e505-117">The **Msvm\_WiFiDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e505-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2e505-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e505-119">Tipo di dati: **[ **MSVM \_ WiFiPort**](msvm-wifiport.md)**</span><span class="sxs-lookup"><span data-stu-id="2e505-119">Data type: **[**Msvm\_WiFiPort**](msvm-wifiport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2e505-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2e505-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e505-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="2e505-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2e505-122">Istanza della classe [**MSVM \_ WiFiPort**](msvm-wifiport.md) che rappresenta il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2e505-122">An instance of the [**Msvm\_WiFiPort**](msvm-wifiport.md) class that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="2e505-123">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="2e505-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e505-124">Tipo di dati: **[ **MSVM \_ WiFiEndpoint**](msvm-wifiendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="2e505-124">Data type: **[**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2e505-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2e505-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e505-126">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="2e505-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2e505-127">Istanza della classe [**MSVM \_ WiFiEndpoint**](msvm-wifiendpoint.md) che rappresenta il punto di accesso al servizio implementato utilizzando il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2e505-127">An instance of the [**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md) class that represents the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e505-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e505-128">Requirements</span></span>



| <span data-ttu-id="2e505-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e505-129">Requirement</span></span> | <span data-ttu-id="2e505-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2e505-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e505-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e505-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2e505-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2e505-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2e505-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e505-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2e505-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2e505-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e505-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2e505-135">Namespace</span></span><br/>                | <span data-ttu-id="2e505-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2e505-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2e505-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2e505-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e505-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e505-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e505-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2e505-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e505-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e505-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

