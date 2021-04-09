---
description: Questa associazione stabilisce un punto di accesso al servizio (SAP) come richiedente dei servizi del protocollo da un endpoint del protocollo.
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Classe Msvm_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2fa01c8e9e7df40a2907e6e43a9cb4b507a53d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968326"
---
# <a name="msvm_bindstolanendpoint-class"></a><span data-ttu-id="3cc9c-103">\_Classe MSVM BindsToLANEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cc9c-103">Msvm\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="3cc9c-104">Questa associazione stabilisce un punto di accesso al servizio (SAP) come richiedente dei servizi del protocollo da un endpoint del protocollo.</span><span class="sxs-lookup"><span data-stu-id="3cc9c-104">This association establishes a service access point (SAP) as a requester of protocol services from a protocol endpoint.</span></span> <span data-ttu-id="3cc9c-105">In genere, questa associazione viene eseguita tra i succhi e gli endpoint in un singolo sistema.</span><span class="sxs-lookup"><span data-stu-id="3cc9c-105">Typically, this association runs between SAPs and endpoints on a single system.</span></span> <span data-ttu-id="3cc9c-106">Poiché un endpoint di protocollo è un tipo di SAP, questa associazione può essere usata per stabilire una sovrapposizione di due protocolli, con il livello superiore rappresentato dall'oggetto **dipendente** e il livello inferiore rappresentato dall'attività **precedente**.</span><span class="sxs-lookup"><span data-stu-id="3cc9c-106">Because a protocol endpoint is a kind of SAP, this binding can be used to establish a layering of two protocols, with the upper layer represented by the **Dependent** and the lower layer represented by the **Antecedent**.</span></span>

<span data-ttu-id="3cc9c-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3cc9c-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc9c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3cc9c-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a><span data-ttu-id="3cc9c-109">Members</span><span class="sxs-lookup"><span data-stu-id="3cc9c-109">Members</span></span>

<span data-ttu-id="3cc9c-110">La **classe \_ BindsToLANEndpoint di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3cc9c-110">The **Msvm\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="3cc9c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3cc9c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3cc9c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3cc9c-112">Properties</span></span>

<span data-ttu-id="3cc9c-113">La **classe \_ BindsToLANEndpoint di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3cc9c-113">The **Msvm\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3cc9c-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3cc9c-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cc9c-115">Tipo di dati: **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="3cc9c-115">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3cc9c-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3cc9c-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cc9c-117">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="3cc9c-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3cc9c-118">Riferimento a una classe [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) che rappresenta la porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="3cc9c-118">A reference to an [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the switch port.</span></span> <span data-ttu-id="3cc9c-119">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="3cc9c-119">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="3cc9c-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="3cc9c-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cc9c-121">Tipo di dati: **[ **MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="3cc9c-121">Data type: **[**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3cc9c-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3cc9c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cc9c-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="3cc9c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3cc9c-124">Riferimento al [**\_ VLANEndpoint MSVM**](msvm-vlanendpoint.md) associato alla porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="3cc9c-124">A reference to the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) associated with the switch port.</span></span> <span data-ttu-id="3cc9c-125">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="3cc9c-125">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="3cc9c-126">**FrameType**</span><span class="sxs-lookup"><span data-stu-id="3cc9c-126">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cc9c-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3cc9c-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3cc9c-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3cc9c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cc9c-129">Descrive il metodo di framing per il livello superiore SAP o endpoint associato all'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="3cc9c-129">Describes the framing method for the upper layer SAP or endpoint that is bound to the LAN endpoint.</span></span> <span data-ttu-id="3cc9c-130">Questa proprietà viene ereditata da **CIM \_ BindsToLANEndpoint** ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="3cc9c-130">This property is inherited from **CIM\_BindsToLANEndpoint**, and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3cc9c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3cc9c-131">Requirements</span></span>



| <span data-ttu-id="3cc9c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cc9c-132">Requirement</span></span> | <span data-ttu-id="3cc9c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="3cc9c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc9c-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3cc9c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3cc9c-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3cc9c-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3cc9c-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3cc9c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3cc9c-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3cc9c-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3cc9c-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3cc9c-138">Namespace</span></span><br/>                | <span data-ttu-id="3cc9c-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3cc9c-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3cc9c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3cc9c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cc9c-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cc9c-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cc9c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3cc9c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cc9c-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3cc9c-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

