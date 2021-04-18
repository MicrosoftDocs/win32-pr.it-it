---
description: Questa classe è deprecata. È invece consigliabile derivare dalla classe del \_ servizio CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: Classe CIM_NetworkService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b141e6e38f2fafefdf6e75670b975e0fcdd2961c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317214"
---
# <a name="cim_networkservice-class"></a><span data-ttu-id="0c499-104">\_Classe CIM NetworkService</span><span class="sxs-lookup"><span data-stu-id="0c499-104">CIM\_NetworkService class</span></span>

<span data-ttu-id="0c499-105">Questa classe è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0c499-105">This class is deprecated.</span></span> <span data-ttu-id="0c499-106">È invece consigliabile derivare dalla classe [**del \_ servizio CIM**](cim-service.md) .</span><span class="sxs-lookup"><span data-stu-id="0c499-106">Instead, we recommend deriving from the [**CIM\_Service**](cim-service.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c499-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c499-107">Syntax</span></span>

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a><span data-ttu-id="0c499-108">Members</span><span class="sxs-lookup"><span data-stu-id="0c499-108">Members</span></span>

<span data-ttu-id="0c499-109">La classe **CIM \_ NetworkService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0c499-109">The **CIM\_NetworkService** class has these types of members:</span></span>

-   [<span data-ttu-id="0c499-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c499-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c499-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c499-111">Properties</span></span>

<span data-ttu-id="0c499-112">La classe **CIM \_ NetworkService** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0c499-112">The **CIM\_NetworkService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c499-113">**Parole chiave**</span><span class="sxs-lookup"><span data-stu-id="0c499-113">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c499-114">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0c499-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c499-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c499-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c499-116">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore")</span><span class="sxs-lookup"><span data-stu-id="0c499-116">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="0c499-117">Questa proprietà è deprecata e non deve essere usata.</span><span class="sxs-lookup"><span data-stu-id="0c499-117">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="0c499-118">Descrizione deprecata: matrice di parole chiave che può essere utilizzata nelle query.</span><span class="sxs-lookup"><span data-stu-id="0c499-118">Deprecated description: An array of keywords that can be used in queries.</span></span>

 

</dd> <dt>

<span data-ttu-id="0c499-119">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="0c499-119">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c499-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c499-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c499-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c499-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c499-122">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")</span><span class="sxs-lookup"><span data-stu-id="0c499-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_ServiceAccessURI")</span></span>
</dt> </dl>

<span data-ttu-id="0c499-123">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0c499-123">This property is deprecated.</span></span> <span data-ttu-id="0c499-124">È invece consigliabile usare la classe **CIM \_ ServiceAccessURI** .</span><span class="sxs-lookup"><span data-stu-id="0c499-124">Instead, we recommend the **CIM\_ServiceAccessURI** class.</span></span>

> [!Note]  
> <span data-ttu-id="0c499-125">Descrizione deprecata: un URL che fornisce il protocollo, il percorso di rete e altre informazioni specifiche del servizio necessarie per accedere al servizio.</span><span class="sxs-lookup"><span data-stu-id="0c499-125">Deprecated description: A URL that provides the protocol, network location, and other service-specific information required in order to access the service.</span></span>

 

</dd> <dt>

<span data-ttu-id="0c499-126">**StartupConditions**</span><span class="sxs-lookup"><span data-stu-id="0c499-126">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c499-127">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0c499-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c499-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c499-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c499-129">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore")</span><span class="sxs-lookup"><span data-stu-id="0c499-129">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="0c499-130">Questa proprietà è deprecata e non deve essere usata.</span><span class="sxs-lookup"><span data-stu-id="0c499-130">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="0c499-131">Descrizione deprecata: le condizioni preliminari che devono essere soddisfatte affinché il servizio venga avviato correttamente.</span><span class="sxs-lookup"><span data-stu-id="0c499-131">Deprecated description: The pre-conditions that must be met in order for this service to start correctly.</span></span>

 

</dd> <dt>

<span data-ttu-id="0c499-132">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="0c499-132">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c499-133">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0c499-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c499-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c499-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c499-135">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore")</span><span class="sxs-lookup"><span data-stu-id="0c499-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="0c499-136">Questa proprietà è deprecata e non deve essere usata.</span><span class="sxs-lookup"><span data-stu-id="0c499-136">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="0c499-137">Deprecated Description: parametri che devono essere forniti al metodo **StartService** per poter avviare correttamente il servizio.</span><span class="sxs-lookup"><span data-stu-id="0c499-137">Deprecated description: The parameters that must be supplied to the **StartService** method in order for this service to start correctly.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c499-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c499-138">Requirements</span></span>



| <span data-ttu-id="0c499-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c499-139">Requirement</span></span> | <span data-ttu-id="0c499-140">Valore</span><span class="sxs-lookup"><span data-stu-id="0c499-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c499-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c499-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0c499-142">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0c499-142">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0c499-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c499-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0c499-144">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c499-144">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0c499-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0c499-145">Namespace</span></span><br/>                | <span data-ttu-id="0c499-146">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0c499-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0c499-147">MOF</span><span class="sxs-lookup"><span data-stu-id="0c499-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c499-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c499-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c499-149">DLL</span><span class="sxs-lookup"><span data-stu-id="0c499-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c499-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c499-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0c499-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c499-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c499-152">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="0c499-152">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

