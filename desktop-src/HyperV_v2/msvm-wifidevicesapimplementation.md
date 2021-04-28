---
description: 'Msvm_WiFiDeviceSAPImplementation classe : associazione tra un punto di accesso del servizio (SAP) e la modalità di implementazione.'
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Msvm_WiFiDeviceSAPImplementation classe
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
ms.openlocfilehash: 99826ce3a37e19867cef1a6ddf276f5136b21a3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109249"
---
# <a name="msvm_wifidevicesapimplementation-class"></a><span data-ttu-id="c7cef-103">Classe Msvm \_ WiFiDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="c7cef-103">Msvm\_WiFiDeviceSAPImplementation class</span></span>

<span data-ttu-id="c7cef-104">Associazione tra un punto di accesso del servizio (SAP) e la modalità di implementazione.</span><span class="sxs-lookup"><span data-stu-id="c7cef-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="c7cef-105">La cardinalità di questa associazione è molti-a-molti.</span><span class="sxs-lookup"><span data-stu-id="c7cef-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="c7cef-106">Un sap può essere fornito da più di un dispositivo logico, operando in combinazione.</span><span class="sxs-lookup"><span data-stu-id="c7cef-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="c7cef-107">Qualsiasi dispositivo può fornire più di un SAP.</span><span class="sxs-lookup"><span data-stu-id="c7cef-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="c7cef-108">Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino in combinazione per fornire il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="c7cef-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="c7cef-109">Se esistono implementazioni diverse di sap, ognuna di queste implementazioni comporterebbe la creazione di singole istanze dell'oggetto SAP.</span><span class="sxs-lookup"><span data-stu-id="c7cef-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="c7cef-110">Queste singole istanze hanno quindi associazioni alle implementazioni univoche.</span><span class="sxs-lookup"><span data-stu-id="c7cef-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="c7cef-111">La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c7cef-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7cef-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7cef-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c7cef-113">Members</span><span class="sxs-lookup"><span data-stu-id="c7cef-113">Members</span></span>

<span data-ttu-id="c7cef-114">La **classe Msvm \_ WiFiDeviceSAPImplementation** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c7cef-114">The **Msvm\_WiFiDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="c7cef-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c7cef-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7cef-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c7cef-116">Properties</span></span>

<span data-ttu-id="c7cef-117">La **classe Msvm \_ WiFiDeviceSAPImplementation** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c7cef-117">The **Msvm\_WiFiDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7cef-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="c7cef-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7cef-119">Tipo di dati: **[ **Msvm \_ WiFiPort**](msvm-wifiport.md)**</span><span class="sxs-lookup"><span data-stu-id="c7cef-119">Data type: **[**Msvm\_WiFiPort**](msvm-wifiport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c7cef-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c7cef-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7cef-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="c7cef-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c7cef-122">Istanza della classe [**Msvm \_ WiFiPort**](msvm-wifiport.md) che rappresenta il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="c7cef-122">An instance of the [**Msvm\_WiFiPort**](msvm-wifiport.md) class that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="c7cef-123">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="c7cef-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7cef-124">Tipo di dati: **[ **Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="c7cef-124">Data type: **[**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c7cef-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c7cef-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7cef-126">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")</span><span class="sxs-lookup"><span data-stu-id="c7cef-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c7cef-127">Istanza della classe [**Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md) che rappresenta il punto di accesso del servizio implementato tramite il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="c7cef-127">An instance of the [**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md) class that represents the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7cef-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7cef-128">Requirements</span></span>



| <span data-ttu-id="c7cef-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7cef-129">Requirement</span></span> | <span data-ttu-id="c7cef-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c7cef-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7cef-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7cef-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c7cef-132">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c7cef-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c7cef-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7cef-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c7cef-134">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7cef-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7cef-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c7cef-135">Namespace</span></span><br/>                | <span data-ttu-id="c7cef-136">Virtualizzazione \\ radice \\ V2</span><span class="sxs-lookup"><span data-stu-id="c7cef-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c7cef-137">MOF</span><span class="sxs-lookup"><span data-stu-id="c7cef-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7cef-138"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7cef-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7cef-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c7cef-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7cef-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7cef-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

