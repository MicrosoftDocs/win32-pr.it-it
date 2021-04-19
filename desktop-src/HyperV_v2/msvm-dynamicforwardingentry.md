---
description: Rappresenta una voce nel database di inoltri (filtro) associato al servizio bridging trasparente.
ms.assetid: 3C9FAE99-9543-4A6A-B578-3F4626598DB3
title: Classe Msvm_DynamicForwardingEntry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DynamicForwardingEntry
- Msvm_DynamicForwardingEntry.InstanceID
- Msvm_DynamicForwardingEntry.Caption
- Msvm_DynamicForwardingEntry.Description
- Msvm_DynamicForwardingEntry.ElementName
- Msvm_DynamicForwardingEntry.InstallDate
- Msvm_DynamicForwardingEntry.Name
- Msvm_DynamicForwardingEntry.OperationalStatus
- Msvm_DynamicForwardingEntry.StatusDescriptions
- Msvm_DynamicForwardingEntry.Status
- Msvm_DynamicForwardingEntry.HealthState
- Msvm_DynamicForwardingEntry.CommunicationStatus
- Msvm_DynamicForwardingEntry.DetailedStatus
- Msvm_DynamicForwardingEntry.OperatingStatus
- Msvm_DynamicForwardingEntry.PrimaryStatus
- Msvm_DynamicForwardingEntry.SystemCreationClassName
- Msvm_DynamicForwardingEntry.SystemName
- Msvm_DynamicForwardingEntry.ServiceCreationClassName
- Msvm_DynamicForwardingEntry.ServiceName
- Msvm_DynamicForwardingEntry.CreationClassName
- Msvm_DynamicForwardingEntry.MACAddress
- Msvm_DynamicForwardingEntry.DynamicStatus
- Msvm_DynamicForwardingEntry.VlanId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f14f8b3a8f5f62e1a474b3d7b7f832b6acd530f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314836"
---
# <a name="msvm_dynamicforwardingentry-class"></a><span data-ttu-id="a9562-103">\_Classe MSVM DynamicForwardingEntry</span><span class="sxs-lookup"><span data-stu-id="a9562-103">Msvm\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="a9562-104">Rappresenta una voce nel database di inoltri (filtro) associato al servizio bridging trasparente.</span><span class="sxs-lookup"><span data-stu-id="a9562-104">Represents an entry in the forwarding (filtering) database that is associated with the transparent bridging service.</span></span> <span data-ttu-id="a9562-105">La voce è debole per il servizio, come specificato da [**MSVM \_ TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md).</span><span class="sxs-lookup"><span data-stu-id="a9562-105">The entry is weak to the service, as specified by [**Msvm\_TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md).</span></span>

<span data-ttu-id="a9562-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a9562-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9562-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9562-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DynamicForwardingEntry : CIM_DynamicForwardingEntry
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   SystemCreationClassName;
  string   SystemName;
  string   ServiceCreationClassName;
  string   ServiceName;
  string   CreationClassName;
  string   MACAddress;
  uint16   DynamicStatus;
  uint16   VlanId;
};
```

## <a name="members"></a><span data-ttu-id="a9562-108">Members</span><span class="sxs-lookup"><span data-stu-id="a9562-108">Members</span></span>

<span data-ttu-id="a9562-109">La **classe \_ DynamicForwardingEntry di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a9562-109">The **Msvm\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="a9562-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a9562-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9562-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a9562-111">Properties</span></span>

<span data-ttu-id="a9562-112">La **classe \_ DynamicForwardingEntry di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a9562-112">The **Msvm\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9562-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a9562-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9562-116">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="a9562-116">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="a9562-117">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9562-117">A short description of the object.</span></span> <span data-ttu-id="a9562-118">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a9562-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-119">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a9562-119">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-120">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9562-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-122">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="a9562-122">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a9562-123">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="a9562-123">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9562-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9562-124">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a9562-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9562-128">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a9562-128">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9562-129">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a9562-129">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="a9562-130">Se utilizzata con le altre proprietà chiave di questa classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a9562-130">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="a9562-131">Questa proprietà viene ereditata da [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9562-131">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-132">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a9562-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-135">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="a9562-135">A description of the object.</span></span> <span data-ttu-id="a9562-136">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a9562-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-137">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a9562-137">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-138">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9562-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-140">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="a9562-140">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a9562-141">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="a9562-141">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9562-142">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9562-142">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-143">**DynamicStatus**</span><span class="sxs-lookup"><span data-stu-id="a9562-143">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9562-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-146">Stato della voce.</span><span class="sxs-lookup"><span data-stu-id="a9562-146">The status of the entry.</span></span> <span data-ttu-id="a9562-147">Questa proprietà viene ereditata da [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9562-147">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a9562-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a9562-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a9562-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Non valido** (2)</span><span class="sxs-lookup"><span data-stu-id="a9562-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a9562-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Appreso** (3)</span><span class="sxs-lookup"><span data-stu-id="a9562-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Learned** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a9562-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4)</span><span class="sxs-lookup"><span data-stu-id="a9562-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a9562-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**Mgmt** (5)</span><span class="sxs-lookup"><span data-stu-id="a9562-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**Mgmt** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a9562-153">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a9562-153">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-156">Nome visualizzato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a9562-156">A display name for the element.</span></span> <span data-ttu-id="a9562-157">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a9562-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-158">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a9562-158">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-159">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9562-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-161">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a9562-161">The current health of the element.</span></span> <span data-ttu-id="a9562-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 ("OK").</span><span class="sxs-lookup"><span data-stu-id="a9562-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="a9562-163">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a9562-163">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-164">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9562-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-166">Viene popolato automaticamente quando viene creata la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a9562-166">Automatically populated when the virtual machine is created.</span></span> <span data-ttu-id="a9562-167">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9562-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-168">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a9562-168">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9562-171">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="a9562-171">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a9562-172">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="a9562-172">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a9562-173">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a9562-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-174">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="a9562-174">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9562-177">Qualificatori: **Key**, **maxlen** (12)</span><span class="sxs-lookup"><span data-stu-id="a9562-177">Qualifiers: **Key**, **MaxLen** (12)</span></span>
</dt> </dl>

<span data-ttu-id="a9562-178">Indirizzo MAC unicast per il quale il servizio bridging trasparente presenta le informazioni di invio e filtro.</span><span class="sxs-lookup"><span data-stu-id="a9562-178">Unicast MAC address for which the transparent bridging service has forwarding and filtering information.</span></span> <span data-ttu-id="a9562-179">L'indirizzo MAC è formattato come dodici cifre esadecimali, ad esempio "010203040506", con ogni coppia che rappresenta uno dei sei ottetti dell'indirizzo MAC nell'ordine dei bit "canonical" in base a RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="a9562-179">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in "canonical" bit order according to RFC 2469.</span></span> <span data-ttu-id="a9562-180">Questa proprietà viene ereditata da [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9562-180">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-181">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a9562-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-184">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="a9562-184">The label by which the object is known.</span></span> <span data-ttu-id="a9562-185">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9562-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-186">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a9562-186">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-187">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9562-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-189">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="a9562-189">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a9562-190">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="a9562-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9562-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9562-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-192">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a9562-192">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-193">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9562-193">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9562-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-195">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a9562-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a9562-196">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a9562-196">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-197">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9562-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-199">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="a9562-199">Provides high level status information.</span></span> <span data-ttu-id="a9562-200">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="a9562-200">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="a9562-201">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="a9562-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9562-202">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9562-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-203">**ServiceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a9562-203">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9562-206">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a9562-206">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9562-207">**CreationClassName** del servizio di ambito.</span><span class="sxs-lookup"><span data-stu-id="a9562-207">The scoping service's **CreationClassName**.</span></span> <span data-ttu-id="a9562-208">Questa proprietà viene ereditata da [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9562-208">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-209">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="a9562-209">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9562-212">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a9562-212">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9562-213">Nome del servizio di ambito.</span><span class="sxs-lookup"><span data-stu-id="a9562-213">The scoping service's name.</span></span> <span data-ttu-id="a9562-214">Questa proprietà viene ereditata da [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9562-214">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-215">**Status**</span><span class="sxs-lookup"><span data-stu-id="a9562-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-218">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="a9562-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9562-219">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a9562-219">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-220">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a9562-220">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9562-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9562-222">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a9562-222">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a9562-223">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a9562-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-224">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9562-226">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a9562-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9562-227">**CreationClassName** del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a9562-227">The scoping system's **CreationClassName**.</span></span> <span data-ttu-id="a9562-228">Questa proprietà viene ereditata da [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9562-228">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a9562-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a9562-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a9562-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9562-232">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="a9562-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9562-233">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="a9562-233">The scoping system's name.</span></span> <span data-ttu-id="a9562-234">Questa proprietà viene ereditata da [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9562-234">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9562-235">**VlanId**</span><span class="sxs-lookup"><span data-stu-id="a9562-235">**VlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9562-236">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9562-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9562-237">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a9562-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a9562-238">Identificatore della LAN virtuale associato a questa voce.</span><span class="sxs-lookup"><span data-stu-id="a9562-238">The virtual LAN identifier associated with this entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9562-239">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9562-239">Remarks</span></span>

<span data-ttu-id="a9562-240">L'accesso alla **classe \_ DynamicForwardingEntry di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="a9562-240">Access to the **Msvm\_DynamicForwardingEntry** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a9562-241">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a9562-241">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="a9562-242">Esempio</span><span class="sxs-lookup"><span data-stu-id="a9562-242">Examples</span></span>

<span data-ttu-id="a9562-243">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a9562-243">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9562-244">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9562-244">Requirements</span></span>



| <span data-ttu-id="a9562-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9562-245">Requirement</span></span> | <span data-ttu-id="a9562-246">Valore</span><span class="sxs-lookup"><span data-stu-id="a9562-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9562-247">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9562-247">Minimum supported client</span></span><br/> | <span data-ttu-id="a9562-248">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a9562-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a9562-249">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9562-249">Minimum supported server</span></span><br/> | <span data-ttu-id="a9562-250">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a9562-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9562-251">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a9562-251">Namespace</span></span><br/>                | <span data-ttu-id="a9562-252">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a9562-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a9562-253">MOF</span><span class="sxs-lookup"><span data-stu-id="a9562-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9562-254"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9562-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9562-255">DLL</span><span class="sxs-lookup"><span data-stu-id="a9562-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9562-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9562-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9562-257">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9562-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9562-258">**\_DYNAMICFORWARDINGENTRY CIM**</span><span class="sxs-lookup"><span data-stu-id="a9562-258">**CIM\_DynamicForwardingEntry**</span></span>](cim-dynamicforwardingentry.md)
</dt> <dt>

<span data-ttu-id="a9562-259">[**\_DYNAMICFORWARDINGENTRY CIM**](/previous-versions//cc136814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a9562-259">[**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))</span></span>
</dt> </dl>

 

