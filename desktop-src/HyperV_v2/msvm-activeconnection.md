---
description: Connette una porta di commutazione all'endpoint LAN a cui è connessa la porta.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Classe Msvm_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf682fac419658785cfe7594aa6fc17e4b2dd28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883950"
---
# <a name="msvm_activeconnection-class"></a><span data-ttu-id="ee8f8-103">\_Classe MSVM ActiveConnection</span><span class="sxs-lookup"><span data-stu-id="ee8f8-103">Msvm\_ActiveConnection class</span></span>

<span data-ttu-id="ee8f8-104">Connette una porta di commutazione all'endpoint LAN a cui è connessa la porta.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-104">Connects a switch port to the LAN endpoint to which the port is connected.</span></span> <span data-ttu-id="ee8f8-105">L'esistenza di questo oggetto significa che la porta di commutazione e l'endpoint LAN sono connessi attivamente e che la porta Ethernet associata all'endpoint LAN può comunicare con la rete tramite la porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-105">The existence of this object means that the switch port and the LAN endpoint are actively connected and the Ethernet port associated with the LAN endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="ee8f8-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee8f8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee8f8-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="ee8f8-108">Members</span><span class="sxs-lookup"><span data-stu-id="ee8f8-108">Members</span></span>

<span data-ttu-id="ee8f8-109">La **classe \_ ActiveConnection di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ee8f8-109">The **Msvm\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="ee8f8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee8f8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee8f8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee8f8-111">Properties</span></span>

<span data-ttu-id="ee8f8-112">La **classe \_ ActiveConnection di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-112">The **Msvm\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee8f8-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ee8f8-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee8f8-114">Tipo di dati: **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="ee8f8-114">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="ee8f8-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee8f8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee8f8-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="ee8f8-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ee8f8-117">Un riferimento a un'istanza della classe [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) che rappresenta il punto di accesso al servizio (SAP) configurato per comunicare o sta comunicando attivamente con SAP dipendente.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-117">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="ee8f8-118">In una connessione unidirezionale, questo SAP è quello che trasmette.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-118">In an unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="ee8f8-119">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="ee8f8-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee8f8-120">Tipo di dati: **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="ee8f8-120">Data type: **[**CIM\_LANEndpoint**](cim-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="ee8f8-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee8f8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee8f8-122">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="ee8f8-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ee8f8-123">Riferimento a un'istanza della classe [**MSVM \_ LANEndpoint**](cim-lanendpoint.md) che rappresenta il SAP configurato per comunicare o sta comunicando attivamente con l'attività SAP precedente.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-123">A reference to an instance of the [**Msvm\_LANEndpoint**](cim-lanendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="ee8f8-124">In una connessione unidirezionale, questo SAP è quello che riceve.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-124">In an unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="ee8f8-125">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="ee8f8-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee8f8-126">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ee8f8-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee8f8-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee8f8-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee8f8-128">Se questa proprietà è **true**, la connessione è unidirezionale; in caso contrario, la connessione è bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="ee8f8-129">Quando una connessione è unidirezionale, è necessario definire il "relatore" come riferimento **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="ee8f8-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="ee8f8-130">In una connessione bidirezionale non è rilevante se il punto di accesso selezionato è l'attività **precedente** o **dipendente**.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="ee8f8-131">Questa proprietà viene ereditata da [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ee8f8-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ee8f8-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="ee8f8-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee8f8-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ee8f8-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee8f8-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee8f8-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee8f8-135">Questa proprietà viene ereditata da [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ee8f8-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="ee8f8-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee8f8-137">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ee8f8-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee8f8-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ee8f8-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee8f8-139">Questa proprietà viene ereditata da [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee8f8-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee8f8-140">Remarks</span></span>

<span data-ttu-id="ee8f8-141">L'accesso alla **classe \_ ActiveConnection di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="ee8f8-141">Access to the **Msvm\_ActiveConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ee8f8-142">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ee8f8-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ee8f8-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="ee8f8-143">Examples</span></span>

<span data-ttu-id="ee8f8-144">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ee8f8-144">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee8f8-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee8f8-145">Requirements</span></span>



| <span data-ttu-id="ee8f8-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee8f8-146">Requirement</span></span> | <span data-ttu-id="ee8f8-147">Valore</span><span class="sxs-lookup"><span data-stu-id="ee8f8-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8f8-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee8f8-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ee8f8-149">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ee8f8-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ee8f8-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee8f8-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ee8f8-151">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ee8f8-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee8f8-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ee8f8-152">Namespace</span></span><br/>                | <span data-ttu-id="ee8f8-153">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ee8f8-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ee8f8-154">MOF</span><span class="sxs-lookup"><span data-stu-id="ee8f8-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee8f8-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee8f8-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee8f8-156">DLL</span><span class="sxs-lookup"><span data-stu-id="ee8f8-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee8f8-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ee8f8-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ee8f8-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee8f8-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8f8-159">**\_ACTIVECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="ee8f8-159">**CIM\_ActiveConnection**</span></span>](cim-activeconnection.md)
</dt> <dt>

<span data-ttu-id="ee8f8-160">[**\_ACTIVECONNECTION CIM**](/previous-versions//cc136779(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee8f8-160">[**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85))</span></span>
</dt> </dl>

 

