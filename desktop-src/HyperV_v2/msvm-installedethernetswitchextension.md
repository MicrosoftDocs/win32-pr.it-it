---
description: Rappresenta un'istanza di un componente di estensione installato in un sistema host.
ms.assetid: ad24fb08-36af-42a8-a910-63eae54fa5b8
title: Classe Msvm_InstalledEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InstalledEthernetSwitchExtension
- Msvm_InstalledEthernetSwitchExtension.InstanceID
- Msvm_InstalledEthernetSwitchExtension.Caption
- Msvm_InstalledEthernetSwitchExtension.Description
- Msvm_InstalledEthernetSwitchExtension.ElementName
- Msvm_InstalledEthernetSwitchExtension.InstallDate
- Msvm_InstalledEthernetSwitchExtension.Name
- Msvm_InstalledEthernetSwitchExtension.OperationalStatus
- Msvm_InstalledEthernetSwitchExtension.StatusDescriptions
- Msvm_InstalledEthernetSwitchExtension.Status
- Msvm_InstalledEthernetSwitchExtension.HealthState
- Msvm_InstalledEthernetSwitchExtension.CommunicationStatus
- Msvm_InstalledEthernetSwitchExtension.DetailedStatus
- Msvm_InstalledEthernetSwitchExtension.OperatingStatus
- Msvm_InstalledEthernetSwitchExtension.PrimaryStatus
- Msvm_InstalledEthernetSwitchExtension.ExtensionType
- Msvm_InstalledEthernetSwitchExtension.Vendor
- Msvm_InstalledEthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfbe0b1996751613c31913447cb0d200d71b8168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307884"
---
# <a name="msvm_installedethernetswitchextension-class"></a><span data-ttu-id="092f6-103">\_Classe MSVM InstalledEthernetSwitchExtension</span><span class="sxs-lookup"><span data-stu-id="092f6-103">Msvm\_InstalledEthernetSwitchExtension class</span></span>

<span data-ttu-id="092f6-104">Rappresenta un'istanza di un componente di estensione installato in un sistema host.</span><span class="sxs-lookup"><span data-stu-id="092f6-104">Represents an instance of an extension component installed on a host system.</span></span>

<span data-ttu-id="092f6-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="092f6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="092f6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="092f6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InstalledEthernetSwitchExtension : CIM_ManagedSystemElement
{
  string   InstanceID;
  string   Caption = " System Virtual Ethernet Switch Extension";
  string   Description = "Microsoft NDIS Packet Capture Filter Driver";
  string   ElementName = "Microsoft NDIS Capture";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="092f6-107">Members</span><span class="sxs-lookup"><span data-stu-id="092f6-107">Members</span></span>

<span data-ttu-id="092f6-108">La **classe \_ InstalledEthernetSwitchExtension di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="092f6-108">The **Msvm\_InstalledEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="092f6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="092f6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="092f6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="092f6-110">Properties</span></span>

<span data-ttu-id="092f6-111">La **classe \_ InstalledEthernetSwitchExtension di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="092f6-111">The **Msvm\_InstalledEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="092f6-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="092f6-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="092f6-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="092f6-115">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="092f6-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="092f6-116">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="092f6-116">A short description of the object.</span></span> <span data-ttu-id="092f6-117">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="092f6-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-118">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="092f6-118">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-119">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="092f6-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-121">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="092f6-121">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="092f6-122">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="092f6-122">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="092f6-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="092f6-123">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-124">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="092f6-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="092f6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-127">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="092f6-127">A description of the object.</span></span> <span data-ttu-id="092f6-128">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="092f6-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-129">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="092f6-129">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="092f6-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-132">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="092f6-132">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="092f6-133">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="092f6-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="092f6-134">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="092f6-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="092f6-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="092f6-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-138">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="092f6-138">A display name for the object.</span></span> <span data-ttu-id="092f6-139">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="092f6-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-140">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="092f6-140">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-141">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="092f6-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-143">Indica il tipo del componente di estensione.</span><span class="sxs-lookup"><span data-stu-id="092f6-143">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="092f6-144">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="092f6-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="092f6-145">**Acquisisci** (1)</span><span class="sxs-lookup"><span data-stu-id="092f6-145">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="092f6-146">**Filtro** (2)</span><span class="sxs-lookup"><span data-stu-id="092f6-146">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="092f6-147">**Inoltri** (3)</span><span class="sxs-lookup"><span data-stu-id="092f6-147">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="092f6-148">**Monitoraggio** (4)</span><span class="sxs-lookup"><span data-stu-id="092f6-148">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="092f6-149">**Nativo** (5)</span><span class="sxs-lookup"><span data-stu-id="092f6-149">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="092f6-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="092f6-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="092f6-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-153">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="092f6-153">The current health of the element.</span></span> <span data-ttu-id="092f6-154">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="092f6-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="092f6-155">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="092f6-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="092f6-156">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="092f6-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="092f6-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-158">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="092f6-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-160">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="092f6-160">The date and time when the object was installed.</span></span> <span data-ttu-id="092f6-161">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="092f6-161">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="092f6-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="092f6-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-163">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="092f6-163">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="092f6-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="092f6-166">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="092f6-166">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="092f6-167">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="092f6-167">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="092f6-168">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="092f6-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-169">**Nome**</span><span class="sxs-lookup"><span data-stu-id="092f6-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="092f6-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="092f6-172">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="092f6-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="092f6-173">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="092f6-173">The label by which the object is known.</span></span> <span data-ttu-id="092f6-174">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="092f6-174">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-175">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="092f6-175">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-176">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="092f6-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-178">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="092f6-178">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="092f6-179">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="092f6-179">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="092f6-180">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="092f6-180">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-181">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="092f6-181">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-182">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="092f6-182">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="092f6-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-184">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="092f6-184">The current statuses of the object.</span></span> <span data-ttu-id="092f6-185">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="092f6-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-186">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="092f6-186">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-187">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="092f6-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-189">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="092f6-189">Provides high level status information.</span></span> <span data-ttu-id="092f6-190">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="092f6-190">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="092f6-191">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="092f6-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="092f6-192">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="092f6-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="092f6-193">**Status**</span><span class="sxs-lookup"><span data-stu-id="092f6-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="092f6-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-196">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="092f6-196">The current status of the object.</span></span> <span data-ttu-id="092f6-197">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="092f6-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="092f6-198">OK</span><span class="sxs-lookup"><span data-stu-id="092f6-198">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="092f6-199"><span id="OK"></span><span id="ok"></span>**Ok**</span><span class="sxs-lookup"><span data-stu-id="092f6-199"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore**</span><span class="sxs-lookup"><span data-stu-id="092f6-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradato**</span><span class="sxs-lookup"><span data-stu-id="092f6-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="092f6-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Errore di prede**</span><span class="sxs-lookup"><span data-stu-id="092f6-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio**</span><span class="sxs-lookup"><span data-stu-id="092f6-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto**</span><span class="sxs-lookup"><span data-stu-id="092f6-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio**</span><span class="sxs-lookup"><span data-stu-id="092f6-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato**</span><span class="sxs-lookup"><span data-stu-id="092f6-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**Non ripristino**</span><span class="sxs-lookup"><span data-stu-id="092f6-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto**</span><span class="sxs-lookup"><span data-stu-id="092f6-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Comunicazione persa**</span><span class="sxs-lookup"><span data-stu-id="092f6-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="092f6-211">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="092f6-211">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-212">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="092f6-212">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="092f6-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-214">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="092f6-214">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="092f6-215">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="092f6-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="092f6-216">**Fornitore**</span><span class="sxs-lookup"><span data-stu-id="092f6-216">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="092f6-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-219">Indica il fornitore che fornisce l'estensione.</span><span class="sxs-lookup"><span data-stu-id="092f6-219">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="092f6-220">**Versione**</span><span class="sxs-lookup"><span data-stu-id="092f6-220">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="092f6-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="092f6-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="092f6-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="092f6-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="092f6-223">Versione dell'estensione in un formato "Major. minor", ad esempio "2,0".</span><span class="sxs-lookup"><span data-stu-id="092f6-223">The version of the extension in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="092f6-224">Requisiti</span><span class="sxs-lookup"><span data-stu-id="092f6-224">Requirements</span></span>



| <span data-ttu-id="092f6-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="092f6-225">Requirement</span></span> | <span data-ttu-id="092f6-226">Valore</span><span class="sxs-lookup"><span data-stu-id="092f6-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="092f6-227">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="092f6-227">Minimum supported client</span></span><br/> | <span data-ttu-id="092f6-228">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="092f6-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="092f6-229">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="092f6-229">Minimum supported server</span></span><br/> | <span data-ttu-id="092f6-230">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="092f6-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="092f6-231">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="092f6-231">Namespace</span></span><br/>                | <span data-ttu-id="092f6-232">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="092f6-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="092f6-233">MOF</span><span class="sxs-lookup"><span data-stu-id="092f6-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="092f6-234"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="092f6-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="092f6-235">DLL</span><span class="sxs-lookup"><span data-stu-id="092f6-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="092f6-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="092f6-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

