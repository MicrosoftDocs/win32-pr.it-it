---
description: Rappresenta i dati dell'impostazione della funzionalità di sicurezza.
ms.assetid: 98e0de24-ccdc-4fc7-86a5-b68d454fde9d
title: Classe Msvm_EthernetSwitchPortSecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortSecuritySettingData
- Msvm_EthernetSwitchPortSecuritySettingData.InstanceID
- Msvm_EthernetSwitchPortSecuritySettingData.Caption
- Msvm_EthernetSwitchPortSecuritySettingData.Description
- Msvm_EthernetSwitchPortSecuritySettingData.ElementName
- Msvm_EthernetSwitchPortSecuritySettingData.AllowMacSpoofing
- Msvm_EthernetSwitchPortSecuritySettingData.EnableDhcpGuard
- Msvm_EthernetSwitchPortSecuritySettingData.EnableRouterGuard
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorMode
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorSession
- Msvm_EthernetSwitchPortSecuritySettingData.AllowIeeePriorityTag
- Msvm_EthernetSwitchPortSecuritySettingData.VirtualSubnetId
- Msvm_EthernetSwitchPortSecuritySettingData.AllowTeaming
- Msvm_EthernetSwitchPortSecuritySettingData.TeamName
- Msvm_EthernetSwitchPortSecuritySettingData.TeamNumber
- Msvm_EthernetSwitchPortSecuritySettingData.EnableFixSpeed10G
- Msvm_EthernetSwitchPortSecuritySettingData.Reserved
- Msvm_EthernetSwitchPortSecuritySettingData.DynamicIPAddressLimit
- Msvm_EthernetSwitchPortSecuritySettingData.StormLimit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d37913f015a3ffbfaa751a7bbb10f79cea2fb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885862"
---
# <a name="msvm_ethernetswitchportsecuritysettingdata-class"></a><span data-ttu-id="f8a53-103">\_Classe MSVM EthernetSwitchPortSecuritySettingData</span><span class="sxs-lookup"><span data-stu-id="f8a53-103">Msvm\_EthernetSwitchPortSecuritySettingData class</span></span>

<span data-ttu-id="f8a53-104">Rappresenta i dati dell'impostazione della funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f8a53-104">Represents the security feature setting data.</span></span>

<span data-ttu-id="f8a53-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f8a53-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a53-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8a53-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("776E0BA7-94A1-41C8-8F28-951F524251B5"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Security Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortSecuritySettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Security Settings";
  string  Description = "Represents the security feature setting data.";
  string  ElementName = "Ethernet Switch Port Security Settings";
  boolean AllowMacSpoofing = FALSE;
  boolean EnableDhcpGuard = FALSE;
  boolean EnableRouterGuard = FALSE;
  uint8   MonitorMode = 0;
  uint8   MonitorSession = 0;
  boolean AllowIeeePriorityTag = FALSE;
  uint32  VirtualSubnetId = 0;
  boolean AllowTeaming = FALSE;
  string  TeamName = ;
  uint32  TeamNumber = 0;
  boolean EnableFixSpeed10G = FALSE;
  boolean Reserved = FALSE;
  uint32  DynamicIPAddressLimit = 0;
  uint32  StormLimit = 0;
};
```

## <a name="members"></a><span data-ttu-id="f8a53-107">Members</span><span class="sxs-lookup"><span data-stu-id="f8a53-107">Members</span></span>

<span data-ttu-id="f8a53-108">La **classe \_ EthernetSwitchPortSecuritySettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f8a53-108">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f8a53-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8a53-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8a53-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8a53-110">Properties</span></span>

<span data-ttu-id="f8a53-111">La **classe \_ EthernetSwitchPortSecuritySettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8a53-111">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8a53-112">**AllowIeeePriorityTag**</span><span class="sxs-lookup"><span data-stu-id="f8a53-112">**AllowIeeePriorityTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8a53-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-115">Qualificatori: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-115">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-116">Specifica se il traffico verso/dalla porta mantiene le informazioni 802.1 P.</span><span class="sxs-lookup"><span data-stu-id="f8a53-116">Specifies whether traffic to/from the port retains 802.1P information.</span></span> <span data-ttu-id="f8a53-117">Contiene **true** se il traffico verso/dalla porta mantiene le informazioni 802.1 p o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f8a53-117">Contains **True** if traffic to/from the port retains 802.1P information or **False** otherwise.</span></span> <span data-ttu-id="f8a53-118">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="f8a53-118">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-119">**AllowMacSpoofing**</span><span class="sxs-lookup"><span data-stu-id="f8a53-119">**AllowMacSpoofing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-120">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8a53-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-122">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-122">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-123">Indica se la porta consentirà lo spoofing degli indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="f8a53-123">Indicates whether the port will allow MAC spoofing.</span></span> <span data-ttu-id="f8a53-124">Se questa proprietà è **true**, la porta consentirà lo spoofing degli indirizzi Mac.</span><span class="sxs-lookup"><span data-stu-id="f8a53-124">If this property is **True**, the port will allow MAC addresses to be spoofed.</span></span> <span data-ttu-id="f8a53-125">Sono consentiti tutti i valori di indirizzi MAC unicast validi.</span><span class="sxs-lookup"><span data-stu-id="f8a53-125">All valid unicast MAC address values are allowed.</span></span> <span data-ttu-id="f8a53-126">Se questa proprietà è **false**, la porta consentirà l'utilizzo solo degli indirizzi MAC configurati all'interno della gestione di Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="f8a53-126">If this property is **False**, the port will only allow MAC addresses that are configured within Hyper-V management to be used.</span></span> <span data-ttu-id="f8a53-127">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="f8a53-127">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-128">**AllowTeaming**</span><span class="sxs-lookup"><span data-stu-id="f8a53-128">**AllowTeaming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8a53-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-131">Qualificatori: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-131">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-132">Indica se le schede di rete connesse alla porta possono far parte di un team.</span><span class="sxs-lookup"><span data-stu-id="f8a53-132">Indicates whether the NICs connected to the port can be part of a team.</span></span> <span data-ttu-id="f8a53-133">Questo vale solo per le schede di rete connesse alle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="f8a53-133">This applies only to NICs connected to virtual machines.</span></span> <span data-ttu-id="f8a53-134">Contiene **true** se gruppo NIC è consentito o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f8a53-134">Contains **True** if NIC teaming is allowed or **False** otherwise.</span></span> <span data-ttu-id="f8a53-135">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="f8a53-135">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-136">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f8a53-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8a53-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8a53-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-139">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8a53-139">A short description of the object.</span></span> <span data-ttu-id="f8a53-140">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "impostazioni di sicurezza della porta del commutere Ethernet".</span><span class="sxs-lookup"><span data-stu-id="f8a53-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-141">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f8a53-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8a53-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8a53-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-144">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="f8a53-144">A description of the object.</span></span> <span data-ttu-id="f8a53-145">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "rappresenta i dati dell'impostazione della funzionalità di sicurezza".</span><span class="sxs-lookup"><span data-stu-id="f8a53-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the security feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-146">**DynamicIPAddressLimit**</span><span class="sxs-lookup"><span data-stu-id="f8a53-146">**DynamicIPAddressLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-147">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8a53-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-149">Qualificatori: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-149">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-150">Definisce il limite per il numero di indirizzi IP dinamici appresi.</span><span class="sxs-lookup"><span data-stu-id="f8a53-150">Defines the limit for number of Dynamic IP addresses learned.</span></span> <span data-ttu-id="f8a53-151">L'impostazione predefinita è none.</span><span class="sxs-lookup"><span data-stu-id="f8a53-151">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-152">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f8a53-152">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8a53-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8a53-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-155">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8a53-155">A display name for the object.</span></span> <span data-ttu-id="f8a53-156">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "impostazioni di sicurezza della porta del commutere Ethernet".</span><span class="sxs-lookup"><span data-stu-id="f8a53-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-157">**EnableDhcpGuard**</span><span class="sxs-lookup"><span data-stu-id="f8a53-157">**EnableDhcpGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-158">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8a53-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-159">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-160">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-161">Specifica se le offerte DHCP sono bloccate dalla porta.</span><span class="sxs-lookup"><span data-stu-id="f8a53-161">Specifies whether DHCP offers are blocked from the port.</span></span> <span data-ttu-id="f8a53-162">Contiene **true** se le offerte DHCP sono bloccate dalla porta o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f8a53-162">Contains **True** if DHCP offers are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="f8a53-163">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="f8a53-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-164">**EnableFixSpeed10G**</span><span class="sxs-lookup"><span data-stu-id="f8a53-164">**EnableFixSpeed10G**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-165">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8a53-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-167">Qualificatori: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-167">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-168">Impostare su TRUE se la velocità a dimensione fissa 10G è abilitata altrimenti FALSE.</span><span class="sxs-lookup"><span data-stu-id="f8a53-168">Set to TRUE if Fixed Speed 10G is enabled else FALSE.</span></span> <span data-ttu-id="f8a53-169">Il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="f8a53-169">Default value is FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="f8a53-170">Proprietà aggiunta in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f8a53-170">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="f8a53-171">**EnableRouterGuard**</span><span class="sxs-lookup"><span data-stu-id="f8a53-171">**EnableRouterGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-172">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8a53-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-174">Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-174">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-175">Specifica se gli annunci router e i reindirizzamenti router sono bloccati dalla porta.</span><span class="sxs-lookup"><span data-stu-id="f8a53-175">Specifies whether router advertisements and router redirects are blocked from the port.</span></span> <span data-ttu-id="f8a53-176">Contiene **true** se gli annunci router e i reindirizzamenti router sono bloccati dalla porta o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f8a53-176">Contains **True** if router advertisements and router redirects are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="f8a53-177">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="f8a53-177">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-178">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f8a53-178">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8a53-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8a53-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-181">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="f8a53-181">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-182">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="f8a53-182">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f8a53-183">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f8a53-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-184">**MonitorMode**</span><span class="sxs-lookup"><span data-stu-id="f8a53-184">**MonitorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-185">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f8a53-185">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-186">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-186">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-187">Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-187">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-188">Indica la modalità di monitoraggio della porta.</span><span class="sxs-lookup"><span data-stu-id="f8a53-188">This indicates the monitor mode of the port.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="f8a53-189">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-189">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination"></span><span id="destination"></span><span id="DESTINATION"></span>

<span data-ttu-id="f8a53-190">**Destinazione** (1)</span><span class="sxs-lookup"><span data-stu-id="f8a53-190">**Destination** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>

<span data-ttu-id="f8a53-191">**Origine** (2)</span><span class="sxs-lookup"><span data-stu-id="f8a53-191">**Source** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f8a53-192">**MonitorSession**</span><span class="sxs-lookup"><span data-stu-id="f8a53-192">**MonitorSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-193">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f8a53-193">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-194">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-195">Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-195">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-196">Specifica l'identificatore della sessione di monitoraggio a cui appartiene questa porta.</span><span class="sxs-lookup"><span data-stu-id="f8a53-196">Specifies the identifier of the monitor session this port belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-197">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f8a53-197">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-198">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8a53-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-199">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-200">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-200">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-201">Riservato</span><span class="sxs-lookup"><span data-stu-id="f8a53-201">Reserved</span></span>

> [!Note]  
> <span data-ttu-id="f8a53-202">Proprietà aggiunta in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f8a53-202">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="f8a53-203">**StormLimit**</span><span class="sxs-lookup"><span data-stu-id="f8a53-203">**StormLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-204">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8a53-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-205">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-206">Qualificatori: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-206">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-207">Definisce il limite di pacchetti al secondo per il traffico broadcast e multicast.</span><span class="sxs-lookup"><span data-stu-id="f8a53-207">Defines the packets per second limit for broadcast and multicast traffic.</span></span> <span data-ttu-id="f8a53-208">L'impostazione predefinita è none.</span><span class="sxs-lookup"><span data-stu-id="f8a53-208">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-209">**TeamName**</span><span class="sxs-lookup"><span data-stu-id="f8a53-209">**TeamName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8a53-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-211">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-212">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-213">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="f8a53-213">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-214">**TeamNumber**</span><span class="sxs-lookup"><span data-stu-id="f8a53-214">**TeamNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-215">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8a53-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-216">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-216">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-217">Qualificatori: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a53-217">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-218">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="f8a53-218">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="f8a53-219">**VirtualSubnetId**</span><span class="sxs-lookup"><span data-stu-id="f8a53-219">**VirtualSubnetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a53-220">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8a53-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-221">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f8a53-221">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f8a53-222">Qualificatori: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span><span class="sxs-lookup"><span data-stu-id="f8a53-222">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span></span>
</dt> </dl>

<span data-ttu-id="f8a53-223">Specifica l'identificatore della subnet virtuale di cui la porta è membro.</span><span class="sxs-lookup"><span data-stu-id="f8a53-223">Specifies the identifier of the virtual subnet that the port is a member of.</span></span> <span data-ttu-id="f8a53-224">Il valore predefinito è none.</span><span class="sxs-lookup"><span data-stu-id="f8a53-224">The default is none.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8a53-225">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8a53-225">Requirements</span></span>



| <span data-ttu-id="f8a53-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8a53-226">Requirement</span></span> | <span data-ttu-id="f8a53-227">Valore</span><span class="sxs-lookup"><span data-stu-id="f8a53-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a53-228">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8a53-228">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a53-229">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f8a53-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f8a53-230">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8a53-230">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a53-231">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f8a53-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8a53-232">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8a53-232">Namespace</span></span><br/>                | <span data-ttu-id="f8a53-233">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f8a53-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f8a53-234">MOF</span><span class="sxs-lookup"><span data-stu-id="f8a53-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8a53-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8a53-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8a53-236">DLL</span><span class="sxs-lookup"><span data-stu-id="f8a53-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8a53-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f8a53-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

