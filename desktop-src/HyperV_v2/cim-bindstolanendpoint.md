---
description: Rappresenta un'associazione in cui un \_ oggetto CIM serviceAccessPoint o CIM \_ ProtocolEndpoint dipende da un oggetto CIM \_ LANEndpoint sottostante nello stesso sistema.
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: Classe CIM_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dff1cf243b54739509343d6d8958aa2a54f464b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315921"
---
# <a name="cim_bindstolanendpoint-class"></a><span data-ttu-id="887d6-103">CIM \_ BindsToLANEndpoint (classe)</span><span class="sxs-lookup"><span data-stu-id="887d6-103">CIM\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="887d6-104">Rappresenta un'associazione in cui un oggetto CIM [**\_ serviceAccessPoint**](cim-serviceaccesspoint.md) o [**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md) dipende da un oggetto [**CIM \_ LANEndpoint**](cim-lanendpoint.md) sottostante nello stesso sistema.</span><span class="sxs-lookup"><span data-stu-id="887d6-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object depends on an underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object on the same system.</span></span>

## <a name="syntax"></a><span data-ttu-id="887d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="887d6-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a><span data-ttu-id="887d6-106">Members</span><span class="sxs-lookup"><span data-stu-id="887d6-106">Members</span></span>

<span data-ttu-id="887d6-107">La classe **CIM \_ BindsToLANEndpoint** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="887d6-107">The **CIM\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="887d6-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="887d6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="887d6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="887d6-109">Properties</span></span>

<span data-ttu-id="887d6-110">La classe **CIM \_ BindsToLANEndpoint** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="887d6-110">The **CIM\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="887d6-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="887d6-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="887d6-112">Tipo di dati: **CIM \_ LANEndpoint**</span><span class="sxs-lookup"><span data-stu-id="887d6-112">Data type: **CIM\_LANEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="887d6-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="887d6-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="887d6-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="887d6-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="887d6-115">Oggetto [**\_ LANEndpoint CIM**](cim-lanendpoint.md) sottostante.</span><span class="sxs-lookup"><span data-stu-id="887d6-115">The underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="887d6-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="887d6-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="887d6-117">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="887d6-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="887d6-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="887d6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="887d6-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="887d6-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="887d6-120">Oggetto [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md) o [**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md) dipendente dalla [**\_ LANEndpoint CIM**](cim-lanendpoint.md).</span><span class="sxs-lookup"><span data-stu-id="887d6-120">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object that is dependent on the [**CIM\_LANEndpoint**](cim-lanendpoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="887d6-121">**FrameType**</span><span class="sxs-lookup"><span data-stu-id="887d6-121">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="887d6-122">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="887d6-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="887d6-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="887d6-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="887d6-124">Metodo di framing per il punto di accesso al servizio o l'endpoint del protocollo di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="887d6-124">The framing method for the upper layer service access point or protocol endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="887d6-125">802.3 RAW è noto solo per l'uso con il protocollo IPX.</span><span class="sxs-lookup"><span data-stu-id="887d6-125">Raw802.3 is only known to be used with the IPX protocol.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="887d6-126">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="887d6-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="887d6-127">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="887d6-127">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.2"></span>

<span data-ttu-id="887d6-128">**802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="887d6-128">**802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

<span data-ttu-id="887d6-129">**Snap** (3)</span><span class="sxs-lookup"><span data-stu-id="887d6-129">**SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

<span data-ttu-id="887d6-130">Non **elaborato 802.3** (4)</span><span class="sxs-lookup"><span data-stu-id="887d6-130">**Raw802.3** (4)</span></span>


<span data-ttu-id="887d6-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="887d6-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="887d6-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="887d6-132">Requirements</span></span>



| <span data-ttu-id="887d6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="887d6-133">Requirement</span></span> | <span data-ttu-id="887d6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="887d6-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="887d6-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="887d6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="887d6-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="887d6-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="887d6-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="887d6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="887d6-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="887d6-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="887d6-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="887d6-139">Namespace</span></span><br/>                | <span data-ttu-id="887d6-140">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="887d6-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="887d6-141">MOF</span><span class="sxs-lookup"><span data-stu-id="887d6-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="887d6-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="887d6-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="887d6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="887d6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="887d6-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="887d6-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="887d6-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="887d6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887d6-146">**\_BINDSTO CIM**</span><span class="sxs-lookup"><span data-stu-id="887d6-146">**CIM\_BindsTo**</span></span>](cim-bindsto.md)
</dt> </dl>

 

