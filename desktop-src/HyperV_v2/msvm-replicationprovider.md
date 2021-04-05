---
description: Rappresenta i provider disponibili per la replica.
ms.assetid: CAAD1CFC-6473-4642-8366-0A5625AE1F70
title: Classe Msvm_ReplicationProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationProvider
- Msvm_ReplicationProvider.InstanceID
- Msvm_ReplicationProvider.Caption
- Msvm_ReplicationProvider.Description
- Msvm_ReplicationProvider.ElementName
- Msvm_ReplicationProvider.Name
- Msvm_ReplicationProvider.OperationalStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8cc821b6bdd5d6f5d1c1085a804799c662f9d62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882165"
---
# <a name="msvm_replicationprovider-class"></a><span data-ttu-id="7d35f-103">\_Classe MSVM ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="7d35f-103">Msvm\_ReplicationProvider class</span></span>

<span data-ttu-id="7d35f-104">Rappresenta i provider disponibili per la replica.</span><span class="sxs-lookup"><span data-stu-id="7d35f-104">Represents the available providers for replication.</span></span>

<span data-ttu-id="7d35f-105">La sintassi seguente è semplificata dal codice MOF e include queste proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7d35f-105">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d35f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d35f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationProvider : CIM_ManagedSystemElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  uint16 OperationalStatus[];
};
```

## <a name="members"></a><span data-ttu-id="7d35f-107">Members</span><span class="sxs-lookup"><span data-stu-id="7d35f-107">Members</span></span>

<span data-ttu-id="7d35f-108">La **classe \_ ReplicationProvider di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7d35f-108">The **Msvm\_ReplicationProvider** class has these types of members:</span></span>

-   [<span data-ttu-id="7d35f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7d35f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d35f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7d35f-110">Properties</span></span>

<span data-ttu-id="7d35f-111">La **classe \_ ReplicationProvider di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7d35f-111">The **Msvm\_ReplicationProvider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d35f-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7d35f-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d35f-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d35f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d35f-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7d35f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d35f-115">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="7d35f-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="7d35f-116">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7d35f-116">A short description of the object.</span></span> <span data-ttu-id="7d35f-117">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7d35f-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="7d35f-118">Per questo oggetto, il valore è:</span><span class="sxs-lookup"><span data-stu-id="7d35f-118">For this object, the value is:</span></span>

<span data-ttu-id="7d35f-119">"Provider di replica"</span><span class="sxs-lookup"><span data-stu-id="7d35f-119">"Replication Provider"</span></span>

</dd> <dt>

<span data-ttu-id="7d35f-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7d35f-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d35f-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d35f-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d35f-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7d35f-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d35f-123">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="7d35f-123">A description of the object.</span></span> <span data-ttu-id="7d35f-124">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7d35f-124">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="7d35f-125">Per i provider esterni, il valore viene fornito da tali provider.</span><span class="sxs-lookup"><span data-stu-id="7d35f-125">For external providers, the value is provided by them.</span></span> <span data-ttu-id="7d35f-126">Per ospitare un provider incorporato, il valore è:</span><span class="sxs-lookup"><span data-stu-id="7d35f-126">For host to host inbuilt provider, the value is:</span></span>

<span data-ttu-id="7d35f-127">"Provider di replica della macchina virtuale nell'host Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="7d35f-127">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="7d35f-128">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7d35f-128">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d35f-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d35f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d35f-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7d35f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d35f-131">Nome visualizzato per il provider di endpoint.</span><span class="sxs-lookup"><span data-stu-id="7d35f-131">A display name for the endpoint provider.</span></span> <span data-ttu-id="7d35f-132">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7d35f-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="7d35f-133">Per ospitare un provider incorporato, questa proprietà è sempre impostata su:</span><span class="sxs-lookup"><span data-stu-id="7d35f-133">For host to host inbuilt provider, this property is always set to:</span></span>

<span data-ttu-id="7d35f-134">"Provider di replica della macchina virtuale nell'host Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="7d35f-134">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="7d35f-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7d35f-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d35f-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d35f-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d35f-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7d35f-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d35f-138">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7d35f-138">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="7d35f-139">ID dell'istanza WMI, che identifica il provider.</span><span class="sxs-lookup"><span data-stu-id="7d35f-139">The WMI instance ID, which identifies the provider.</span></span> <span data-ttu-id="7d35f-140">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7d35f-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="7d35f-141">Il formato di questa proprietà è "Microsoft: <host-computer-name>\\ ReplicationProvider \\<provider-name>".</span><span class="sxs-lookup"><span data-stu-id="7d35f-141">The format of this property is "Microsoft:<host-machine-name>\\ReplicationProvider\\<provider-Name>."</span></span>

</dd> <dt>

<span data-ttu-id="7d35f-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7d35f-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d35f-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7d35f-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d35f-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7d35f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d35f-145">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7d35f-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7d35f-146">Identificatore univoco globale (GUID) del provider che identifica il provider dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="7d35f-146">The globally unique identifier (GUID) of the provider that identifies the endpoint provider.</span></span> <span data-ttu-id="7d35f-147">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7d35f-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="7d35f-148">Nel caso di un provider esterno, questa proprietà è il CLSID dell'oggetto classe COM del provider.</span><span class="sxs-lookup"><span data-stu-id="7d35f-148">In the case of an external provider, this property is the CLSID of the provider COM class object.</span></span> <span data-ttu-id="7d35f-149">Per ospitare un provider incorporato, questa proprietà viene fissata come segue:</span><span class="sxs-lookup"><span data-stu-id="7d35f-149">For host to host inbuilt provider, this property is fixed as:</span></span>

<span data-ttu-id="7d35f-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span><span class="sxs-lookup"><span data-stu-id="7d35f-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span></span>

</dd> <dt>

<span data-ttu-id="7d35f-151">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7d35f-151">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d35f-152">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d35f-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7d35f-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7d35f-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d35f-154">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7d35f-154">The current statuses of the object.</span></span> <span data-ttu-id="7d35f-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su:</span><span class="sxs-lookup"><span data-stu-id="7d35f-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to:</span></span>

<dl> <dt>

<span data-ttu-id="7d35f-156"><span id="S_OK"></span><span id="s_ok"></span>**S \_ OK** (2)</span><span class="sxs-lookup"><span data-stu-id="7d35f-156"><span id="S_OK"></span><span id="s_ok"></span>**S\_OK** (2)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d35f-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d35f-157">Remarks</span></span>

<span data-ttu-id="7d35f-158">Per abilitare una relazione di replica, è possibile usare uno dei provider disponibili e la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="7d35f-158">You can use any of available providers and the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to enable a replication relationship.</span></span> <span data-ttu-id="7d35f-159">Per impostazione predefinita, Hyper-V sceglie l'host incorporato nel provider host, che può essere modificato durante la creazione della replica.</span><span class="sxs-lookup"><span data-stu-id="7d35f-159">Hyper-V by default chooses the inbuilt host to host provider, which can be changed while creating the replication.</span></span> <span data-ttu-id="7d35f-160">Il servizio di gestione Hyper-V comunica con un provider esterno utilizzando COM.</span><span class="sxs-lookup"><span data-stu-id="7d35f-160">Hyper-V management service communicates with an external provider by using COM.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d35f-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d35f-161">Requirements</span></span>



| <span data-ttu-id="7d35f-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d35f-162">Requirement</span></span> | <span data-ttu-id="7d35f-163">Valore</span><span class="sxs-lookup"><span data-stu-id="7d35f-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d35f-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d35f-164">Minimum supported client</span></span><br/> | <span data-ttu-id="7d35f-165">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7d35f-165">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7d35f-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d35f-166">Minimum supported server</span></span><br/> | <span data-ttu-id="7d35f-167">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d35f-167">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7d35f-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7d35f-168">Namespace</span></span><br/>                | <span data-ttu-id="7d35f-169">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7d35f-169">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7d35f-170">MOF</span><span class="sxs-lookup"><span data-stu-id="7d35f-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d35f-171"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d35f-171"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d35f-172">DLL</span><span class="sxs-lookup"><span data-stu-id="7d35f-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d35f-173"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d35f-173"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7d35f-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d35f-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d35f-175">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="7d35f-175">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="7d35f-176">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="7d35f-176">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

