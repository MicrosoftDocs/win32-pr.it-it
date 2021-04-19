---
description: Rappresenta un'istanza di un componente di estensione associato a un comswitch Ethernet virtuale.
ms.assetid: 5b3e26e3-4cb9-47c9-865e-2f3232bbfc8e
title: Classe Msvm_EthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtension
- Msvm_EthernetSwitchExtension.InstanceID
- Msvm_EthernetSwitchExtension.Caption
- Msvm_EthernetSwitchExtension.Description
- Msvm_EthernetSwitchExtension.ElementName
- Msvm_EthernetSwitchExtension.InstallDate
- Msvm_EthernetSwitchExtension.OperationalStatus
- Msvm_EthernetSwitchExtension.StatusDescriptions
- Msvm_EthernetSwitchExtension.Status
- Msvm_EthernetSwitchExtension.HealthState
- Msvm_EthernetSwitchExtension.CommunicationStatus
- Msvm_EthernetSwitchExtension.DetailedStatus
- Msvm_EthernetSwitchExtension.OperatingStatus
- Msvm_EthernetSwitchExtension.PrimaryStatus
- Msvm_EthernetSwitchExtension.EnabledState
- Msvm_EthernetSwitchExtension.OtherEnabledState
- Msvm_EthernetSwitchExtension.RequestedState
- Msvm_EthernetSwitchExtension.EnabledDefault
- Msvm_EthernetSwitchExtension.TimeOfLastStateChange
- Msvm_EthernetSwitchExtension.AvailableRequestedStates
- Msvm_EthernetSwitchExtension.TransitioningToState
- Msvm_EthernetSwitchExtension.SystemCreationClassName
- Msvm_EthernetSwitchExtension.SystemName
- Msvm_EthernetSwitchExtension.CreationClassName
- Msvm_EthernetSwitchExtension.Name
- Msvm_EthernetSwitchExtension.ExtensionType
- Msvm_EthernetSwitchExtension.Vendor
- Msvm_EthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a6d760737ded1a12cf369ccb3a46595627d8e38e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320036"
---
# <a name="msvm_ethernetswitchextension-class"></a><span data-ttu-id="0e79b-103">\_Classe MSVM EthernetSwitchExtension</span><span class="sxs-lookup"><span data-stu-id="0e79b-103">Msvm\_EthernetSwitchExtension class</span></span>

<span data-ttu-id="0e79b-104">Rappresenta un'istanza di un componente di estensione associato a un comswitch Ethernet virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e79b-104">Represents an instance of an extension component bound to a virtual Ethernet switch.</span></span>

<span data-ttu-id="0e79b-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0e79b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e79b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e79b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtension : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption = "Virtual Switch Extension";
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchExtension";
  string   Name;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="0e79b-107">Members</span><span class="sxs-lookup"><span data-stu-id="0e79b-107">Members</span></span>

<span data-ttu-id="0e79b-108">La **classe \_ EthernetSwitchExtension di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0e79b-108">The **Msvm\_EthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="0e79b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="0e79b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0e79b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e79b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0e79b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="0e79b-111">Methods</span></span>

<span data-ttu-id="0e79b-112">La **classe \_ EthernetSwitchExtension di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0e79b-112">The **Msvm\_EthernetSwitchExtension** class has these methods.</span></span>



| <span data-ttu-id="0e79b-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="0e79b-113">Method</span></span>                                                                        | <span data-ttu-id="0e79b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e79b-114">Description</span></span>                         |
|:------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="0e79b-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0e79b-115">**RequestStateChange**</span></span>](msvm-ethernetswitchextension-requeststatechange.md) | <span data-ttu-id="0e79b-116">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="0e79b-116">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0e79b-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e79b-117">Properties</span></span>

<span data-ttu-id="0e79b-118">La **classe \_ EthernetSwitchExtension di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0e79b-118">The **Msvm\_EthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e79b-119">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0e79b-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-120">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e79b-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-122">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="0e79b-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="0e79b-123">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente del [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e79b-123">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="0e79b-124">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="0e79b-124">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="0e79b-125">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="0e79b-125">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="0e79b-126">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e79b-126">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="0e79b-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="0e79b-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="0e79b-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="0e79b-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="0e79b-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="0e79b-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="0e79b-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="0e79b-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="0e79b-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="0e79b-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="0e79b-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="0e79b-137">)</span><span class="sxs-lookup"><span data-stu-id="0e79b-137">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0e79b-138">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0e79b-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-141">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e79b-141">A short description of the object.</span></span> <span data-ttu-id="0e79b-142">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Virtual Switch Extension".</span><span class="sxs-lookup"><span data-stu-id="0e79b-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch Extension".</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-143">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0e79b-143">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e79b-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-146">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="0e79b-146">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0e79b-147">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0e79b-147">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0e79b-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-148">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-149">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e79b-149">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-152">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0e79b-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-153">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="0e79b-153">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="0e79b-154">Questa proprietà è sempre impostata su "MSVM \_ EthernetSwitchExtension".</span><span class="sxs-lookup"><span data-stu-id="0e79b-154">This property is always set to "Msvm\_EthernetSwitchExtension".</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-155">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0e79b-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-158">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="0e79b-158">A description of the object.</span></span> <span data-ttu-id="0e79b-159">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-160">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0e79b-160">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-161">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e79b-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-163">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="0e79b-163">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0e79b-164">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0e79b-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0e79b-165">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-166">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0e79b-166">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-169">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e79b-169">A display name for the object.</span></span> <span data-ttu-id="0e79b-170">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-171">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0e79b-171">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-172">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e79b-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-174">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="0e79b-174">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0e79b-175">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0e79b-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0e79b-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="0e79b-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="0e79b-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="0e79b-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0e79b-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0e79b-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-180">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e79b-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-182">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="0e79b-182">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0e79b-183">Questa proprietà può anche indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="0e79b-183">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0e79b-184">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e79b-184">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="0e79b-185">Valore</span><span class="sxs-lookup"><span data-stu-id="0e79b-185">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="0e79b-186">Significato</span><span class="sxs-lookup"><span data-stu-id="0e79b-186">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="0e79b-187"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-187"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="0e79b-188"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="0e79b-189"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-189"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="0e79b-190">L'elemento è o potrebbe eseguire comandi, elaborerà tutti i comandi in coda e accoda le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="0e79b-190">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="0e79b-191"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-191"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="0e79b-192">L'elemento non esegue i comandi e rilascia tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="0e79b-192">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="0e79b-193"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-193"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="0e79b-194">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0e79b-194">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="0e79b-195"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-195"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="0e79b-196">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="0e79b-196">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="0e79b-197"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-197"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="0e79b-198">L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="0e79b-198">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="0e79b-199"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-199"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="0e79b-200">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="0e79b-200">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="0e79b-201"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-201"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="0e79b-202">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="0e79b-202">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="0e79b-203"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-203"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="0e79b-204">L'elemento è abilitato ma in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="0e79b-204">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="0e79b-205">Il comportamento dell'elemento è simile allo stato Enabled, ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="0e79b-205">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="0e79b-206">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="0e79b-206">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="0e79b-207"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-207"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="0e79b-208">L'elemento sta per passare a uno stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="0e79b-208">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="0e79b-209">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="0e79b-209">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="0e79b-210"><dt>**DMTF riservato**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-210"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="0e79b-211">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0e79b-211">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="0e79b-212"><dt>**Fornitore riservato**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-212"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="0e79b-213">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0e79b-213">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="0e79b-214">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="0e79b-214">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-215">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0e79b-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-217">Indica il tipo del componente di estensione.</span><span class="sxs-lookup"><span data-stu-id="0e79b-217">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e79b-218">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0e79b-218">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="0e79b-219">**Acquisisci** (1)</span><span class="sxs-lookup"><span data-stu-id="0e79b-219">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="0e79b-220">**Filtro** (2)</span><span class="sxs-lookup"><span data-stu-id="0e79b-220">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="0e79b-221">**Inoltri** (3)</span><span class="sxs-lookup"><span data-stu-id="0e79b-221">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="0e79b-222">**Monitoraggio** (4)</span><span class="sxs-lookup"><span data-stu-id="0e79b-222">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="0e79b-223">**Nativo** (5)</span><span class="sxs-lookup"><span data-stu-id="0e79b-223">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e79b-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0e79b-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-225">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e79b-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-227">Specifica lo stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0e79b-227">Specifies the current health of the element.</span></span> <span data-ttu-id="0e79b-228">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="0e79b-228">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="0e79b-229">Quando si verifica un errore critico, controllare il registro eventi per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="0e79b-229">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="0e79b-230">La proprietà **EnabledState** può inoltre contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="0e79b-230">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="0e79b-231">Ad esempio, quando lo spazio su disco è insufficiente, **HealthState** è impostato su 25, la macchina virtuale viene sospesa e **EnabledState** è impostato su 32768 (in pausa).</span><span class="sxs-lookup"><span data-stu-id="0e79b-231">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="0e79b-232">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-232">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="0e79b-233">Valore</span><span class="sxs-lookup"><span data-stu-id="0e79b-233">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="0e79b-234">Significato</span><span class="sxs-lookup"><span data-stu-id="0e79b-234">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="0e79b-235"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-235"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="0e79b-236">L'elemento è completamente funzionante e funziona entro i normali parametri operativi e senza errori.</span><span class="sxs-lookup"><span data-stu-id="0e79b-236">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="0e79b-237"><dt>**Errore principale**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-237"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="0e79b-238">Si è verificato un errore grave nell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0e79b-238">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="0e79b-239"><dt>**Errore critico**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-239"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="0e79b-240">L'elemento è non funzionale e il ripristino potrebbe non essere possibile.</span><span class="sxs-lookup"><span data-stu-id="0e79b-240">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="0e79b-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0e79b-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-242">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e79b-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-244">Data e ora di creazione della configurazione della macchina virtuale per una macchina virtuale, o **null**, per un sistema operativo di gestione.</span><span class="sxs-lookup"><span data-stu-id="0e79b-244">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="0e79b-245">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0e79b-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-249">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="0e79b-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-250">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="0e79b-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0e79b-251">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-252">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0e79b-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-253">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-255">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0e79b-255">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-256">Nome univoco del componente di estensione.</span><span class="sxs-lookup"><span data-stu-id="0e79b-256">The unique name of the extension component.</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-257">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0e79b-257">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-258">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e79b-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-260">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="0e79b-260">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0e79b-261">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0e79b-261">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0e79b-262">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-262">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-263">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0e79b-263">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-264">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e79b-264">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-266">Matrice che contiene gli stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e79b-266">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="0e79b-267">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-268">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0e79b-268">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-269">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-271">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="0e79b-271">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0e79b-272">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="0e79b-272">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0e79b-273">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="0e79b-273">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-274">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0e79b-274">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-275">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e79b-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-277">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="0e79b-277">Provides high level status information.</span></span> <span data-ttu-id="0e79b-278">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="0e79b-278">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="0e79b-279">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0e79b-279">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0e79b-280">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-281">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0e79b-281">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-282">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e79b-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-284">Ultimo stato richiesto o desiderato per l'elemento passato al metodo **RequestStateChange** oppure 12 (non applicabile) se non è in corso alcuna modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="0e79b-284">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="0e79b-285">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="0e79b-285">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0e79b-286">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0e79b-286">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="0e79b-287">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e79b-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-288">**Status**</span><span class="sxs-lookup"><span data-stu-id="0e79b-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-291">Stringa che specifica lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0e79b-291">A string that specifies the status of the element.</span></span> <span data-ttu-id="0e79b-292">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-293">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0e79b-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-294">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0e79b-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-296">Qualificatori: **arrayType** ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="0e79b-296">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-297">Matrice contenente stringhe che descrivono i valori corrispondenti della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0e79b-297">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="0e79b-298">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e79b-298">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-299">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e79b-299">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-302">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**propagata**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0e79b-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-303">Nome della classe di creazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="0e79b-303">The system creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-304">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0e79b-304">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-305">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-307">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**propagata**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Nome**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0e79b-307">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-308">Nome del commutire virtuale a cui è associata l'istanza di estensione.</span><span class="sxs-lookup"><span data-stu-id="0e79b-308">The name of the virtual switch to which the extension instance is bound to.</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-309">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0e79b-309">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-310">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e79b-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-312">Data e ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0e79b-312">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0e79b-313">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e79b-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-314">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0e79b-314">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-315">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e79b-315">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-317">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0e79b-317">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0e79b-318">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0e79b-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-319">**Fornitore**</span><span class="sxs-lookup"><span data-stu-id="0e79b-319">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-320">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-322">Indica il fornitore che fornisce l'estensione.</span><span class="sxs-lookup"><span data-stu-id="0e79b-322">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="0e79b-323">**Versione**</span><span class="sxs-lookup"><span data-stu-id="0e79b-323">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e79b-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e79b-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e79b-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e79b-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e79b-326">Versione dell'estensione in formato "*principale*". *minor*", ad esempio" 2,0 ".</span><span class="sxs-lookup"><span data-stu-id="0e79b-326">The version of the extension in a format of "*major*.*minor*", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e79b-327">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e79b-327">Requirements</span></span>



| <span data-ttu-id="0e79b-328">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e79b-328">Requirement</span></span> | <span data-ttu-id="0e79b-329">Valore</span><span class="sxs-lookup"><span data-stu-id="0e79b-329">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e79b-330">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e79b-330">Minimum supported client</span></span><br/> | <span data-ttu-id="0e79b-331">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0e79b-331">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0e79b-332">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e79b-332">Minimum supported server</span></span><br/> | <span data-ttu-id="0e79b-333">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0e79b-333">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0e79b-334">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0e79b-334">Namespace</span></span><br/>                | <span data-ttu-id="0e79b-335">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0e79b-335">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0e79b-336">MOF</span><span class="sxs-lookup"><span data-stu-id="0e79b-336">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e79b-337"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-337"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e79b-338">DLL</span><span class="sxs-lookup"><span data-stu-id="0e79b-338">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e79b-339"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e79b-339"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

