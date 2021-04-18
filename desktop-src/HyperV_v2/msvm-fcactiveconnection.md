---
description: Connette una porta di commutazione all'endpoint Fibre Channel a cui è connessa la porta.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Classe Msvm_FcActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307923"
---
# <a name="msvm_fcactiveconnection-class"></a><span data-ttu-id="23721-103">\_Classe MSVM FcActiveConnection</span><span class="sxs-lookup"><span data-stu-id="23721-103">Msvm\_FcActiveConnection class</span></span>

<span data-ttu-id="23721-104">Connette una porta di commutazione all'endpoint Fibre Channel a cui è connessa la porta.</span><span class="sxs-lookup"><span data-stu-id="23721-104">Connects a switch port to the Fibre Channel endpoint to which the port is connected.</span></span> <span data-ttu-id="23721-105">L'esistenza di questo oggetto significa che la porta di commutazione e l'endpoint Fibre Channel sono connessi attivamente e la porta Fibre Channel associata all'endpoint Fibre Channel può comunicare con la rete tramite la porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="23721-105">The existence of this object means that the switch port and the Fibre Channel endpoint are actively connected, and the Fibre Channel port associated with the Fibre Channel endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="23721-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="23721-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23721-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23721-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="23721-108">Members</span><span class="sxs-lookup"><span data-stu-id="23721-108">Members</span></span>

<span data-ttu-id="23721-109">La **classe \_ FcActiveConnection di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="23721-109">The **Msvm\_FcActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="23721-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23721-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23721-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23721-111">Properties</span></span>

<span data-ttu-id="23721-112">La **classe \_ FcActiveConnection di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="23721-112">The **Msvm\_FcActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23721-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="23721-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23721-114">Tipo di dati: **MSVM \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="23721-114">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="23721-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23721-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23721-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="23721-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="23721-117">Un riferimento a un'istanza della classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) che rappresenta il punto di accesso al servizio (SAP) configurato per comunicare o sta comunicando attivamente con SAP dipendente.</span><span class="sxs-lookup"><span data-stu-id="23721-117">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="23721-118">In una connessione unidirezionale, questo SAP è quello che trasmette.</span><span class="sxs-lookup"><span data-stu-id="23721-118">In a unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="23721-119">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="23721-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23721-120">Tipo di dati: **MSVM \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="23721-120">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="23721-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23721-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23721-122">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="23721-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="23721-123">Riferimento a un'istanza della classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) che rappresenta il SAP configurato per comunicare o sta comunicando attivamente con l'attività SAP precedente.</span><span class="sxs-lookup"><span data-stu-id="23721-123">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="23721-124">In una connessione unidirezionale, questo SAP è quello che riceve.</span><span class="sxs-lookup"><span data-stu-id="23721-124">In a unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="23721-125">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="23721-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23721-126">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23721-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23721-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23721-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23721-128">Se questa proprietà è **true**, la connessione è unidirezionale; in caso contrario, la connessione è bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="23721-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="23721-129">Quando una connessione è unidirezionale, è necessario definire il "relatore" come riferimento **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="23721-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="23721-130">In una connessione bidirezionale non è rilevante se il punto di accesso selezionato è l'attività **precedente** o **dipendente**.</span><span class="sxs-lookup"><span data-stu-id="23721-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="23721-131">Questa proprietà viene ereditata da [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23721-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="23721-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="23721-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23721-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23721-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23721-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23721-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23721-135">Questa proprietà viene ereditata da [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="23721-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23721-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="23721-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23721-137">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23721-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23721-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23721-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23721-139">Questa proprietà viene ereditata da [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="23721-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23721-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23721-140">Requirements</span></span>



| <span data-ttu-id="23721-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="23721-141">Requirement</span></span> | <span data-ttu-id="23721-142">Valore</span><span class="sxs-lookup"><span data-stu-id="23721-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23721-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23721-143">Minimum supported client</span></span><br/> | <span data-ttu-id="23721-144">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="23721-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23721-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23721-145">Minimum supported server</span></span><br/> | <span data-ttu-id="23721-146">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="23721-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23721-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="23721-147">Namespace</span></span><br/>                | <span data-ttu-id="23721-148">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="23721-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23721-149">MOF</span><span class="sxs-lookup"><span data-stu-id="23721-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23721-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23721-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23721-151">DLL</span><span class="sxs-lookup"><span data-stu-id="23721-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23721-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23721-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

