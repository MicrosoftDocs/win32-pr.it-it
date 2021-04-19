---
description: Rappresenta l'elenco di controllo di accesso (ACL) per le impostazioni della porta di commutazione.
ms.assetid: c0d6dfa1-017c-4e66-9ee3-425182d84231
title: Classe Msvm_EthernetSwitchPortAclSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortAclSettingData
- Msvm_EthernetSwitchPortAclSettingData.InstanceID
- Msvm_EthernetSwitchPortAclSettingData.Caption
- Msvm_EthernetSwitchPortAclSettingData.Description
- Msvm_EthernetSwitchPortAclSettingData.ElementName
- Msvm_EthernetSwitchPortAclSettingData.Name
- Msvm_EthernetSwitchPortAclSettingData.Direction
- Msvm_EthernetSwitchPortAclSettingData.Applicability
- Msvm_EthernetSwitchPortAclSettingData.AclType
- Msvm_EthernetSwitchPortAclSettingData.Action
- Msvm_EthernetSwitchPortAclSettingData.LocalAddress
- Msvm_EthernetSwitchPortAclSettingData.LocalAddressPrefixLength
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddress
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddressPrefixLength
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 92735718e339a0caf33910dec703276aea946a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320022"
---
# <a name="msvm_ethernetswitchportaclsettingdata-class"></a><span data-ttu-id="0ef7a-103">\_Classe MSVM EthernetSwitchPortAclSettingData</span><span class="sxs-lookup"><span data-stu-id="0ef7a-103">Msvm\_EthernetSwitchPortAclSettingData class</span></span>

<span data-ttu-id="0ef7a-104">Rappresenta l'elenco di controllo di accesso (ACL) per le impostazioni della porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-104">Represents the access control list (ACL) for switch port settings.</span></span>

<span data-ttu-id="0ef7a-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef7a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ef7a-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("998BEF4A-5D55-492A-9C43-8B2F5EAE9F2B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port ACL Settings";
  string Description = "Represents the base class for switch port settings.";
  string ElementName = "Ethernet Switch Port ACL Settings";
  string Name = "";
  uint8  Direction = 0;
  uint8  Applicability = 0;
  uint8  AclType = 0;
  uint8  Action = 0;
  string LocalAddress = "";
  uint8  LocalAddressPrefixLength = 0;
  string RemoteAddress = length = 0;
  uint8  RemoteAddressPrefixLength = 0;
};
```

## <a name="members"></a><span data-ttu-id="0ef7a-107">Members</span><span class="sxs-lookup"><span data-stu-id="0ef7a-107">Members</span></span>

<span data-ttu-id="0ef7a-108">La **classe \_ EthernetSwitchPortAclSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0ef7a-108">The **Msvm\_EthernetSwitchPortAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0ef7a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0ef7a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ef7a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0ef7a-110">Properties</span></span>

<span data-ttu-id="0ef7a-111">La **classe \_ EthernetSwitchPortAclSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-111">The **Msvm\_EthernetSwitchPortAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ef7a-112">**AclType**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-112">**AclType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-113">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-115">Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-116">Indica il tipo di endpoint ACL.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-116">This indicates the type of ACL endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ef7a-117">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC_Acl"></span><span id="mac_acl"></span><span id="MAC_ACL"></span>

<span data-ttu-id="0ef7a-118">**ACL Mac** (1)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-118">**MAC Acl** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_Acl"></span><span id="ipv4_acl"></span><span id="IPV4_ACL"></span>

<span data-ttu-id="0ef7a-119">**ACL IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-119">**IPv4 Acl** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6_Acl"></span><span id="ipv6_acl"></span><span id="IPV6_ACL"></span>

<span data-ttu-id="0ef7a-120">**ACL IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-120">**IPv6 Acl** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ef7a-121">**Azione**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-121">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-122">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-122">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-124">Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-124">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-125">Indica l'azione dell'ACL.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-125">This indicates the action of the ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ef7a-126">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="0ef7a-127">**Consenti** (1)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-127">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="0ef7a-128">**Nega** (2)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-128">**Deny** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Meter"></span><span id="meter"></span><span id="METER"></span>

<span data-ttu-id="0ef7a-129">**Contatore** (3)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-129">**Meter** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ef7a-130">**Applicabilità**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-130">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-131">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-133">Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-133">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-134">Indica se l'ACL viene applicato all'endpoint locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-134">This indicates whether the ACL applies to the local or remote endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ef7a-135">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>

<span data-ttu-id="0ef7a-136">**Locale** (1)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-136">**Local** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote"></span><span id="remote"></span><span id="REMOTE"></span>

<span data-ttu-id="0ef7a-137">**Remoto** (2)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-137">**Remote** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ef7a-138">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-141">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-141">A short description of the object.</span></span> <span data-ttu-id="0ef7a-142">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port ACL Settings".</span><span class="sxs-lookup"><span data-stu-id="0ef7a-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="0ef7a-143">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-146">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="0ef7a-146">A description of the object.</span></span> <span data-ttu-id="0ef7a-147">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "rappresenta la classe di base per le impostazioni della porta di commutazione".</span><span class="sxs-lookup"><span data-stu-id="0ef7a-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the base class for switch port settings.".</span></span>

</dd> <dt>

<span data-ttu-id="0ef7a-148">**Direzione**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-148">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-149">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-151">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-151">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-152">Indica se l'ACL si applica alla direzione in ingresso o in uscita.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-152">This indicates whether the ACL applies to ingress or egress direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ef7a-153">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="0ef7a-154">**In ingresso** (1)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-154">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="0ef7a-155">**In uscita** (2)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-155">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ef7a-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-159">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-159">A display name for the object.</span></span> <span data-ttu-id="0ef7a-160">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port ACL Settings".</span><span class="sxs-lookup"><span data-stu-id="0ef7a-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="0ef7a-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-164">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-165">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-165">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0ef7a-166">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0ef7a-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ef7a-167">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-167">**LocalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-170">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-171">Indirizzo locale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-171">The local address of the virtual machine.</span></span> <span data-ttu-id="0ef7a-172">Può trattarsi di un indirizzo IPv4, IPv6 o MAC.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-172">This can be an IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="0ef7a-173">**LocalAddressPrefixLength**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-173">**LocalAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-174">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-176">Qualificatori: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-176">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-177">Lunghezza del prefisso dell'indirizzo locale.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-177">The local address prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="0ef7a-178">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-180">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-181">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-182">Nome visualizzato dell'ACL.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-182">The display name of the ACL.</span></span>

</dd> <dt>

<span data-ttu-id="0ef7a-183">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-183">**RemoteAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-185">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-186">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-187">Indirizzo remoto della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-187">The remote address of the virtual machine.</span></span> <span data-ttu-id="0ef7a-188">Può essere IPv4, IPv6 o un indirizzo MAC.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-188">This can be IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="0ef7a-189">**RemoteAddressPrefixLength**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-189">**RemoteAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ef7a-190">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0ef7a-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-191">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ef7a-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0ef7a-192">Qualificatori: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0ef7a-192">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0ef7a-193">Lunghezza del prefisso dell'indirizzo remoto.</span><span class="sxs-lookup"><span data-stu-id="0ef7a-193">The remote address prefix length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ef7a-194">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ef7a-194">Requirements</span></span>



| <span data-ttu-id="0ef7a-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ef7a-195">Requirement</span></span> | <span data-ttu-id="0ef7a-196">Valore</span><span class="sxs-lookup"><span data-stu-id="0ef7a-196">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef7a-197">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ef7a-197">Minimum supported client</span></span><br/> | <span data-ttu-id="0ef7a-198">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0ef7a-198">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0ef7a-199">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ef7a-199">Minimum supported server</span></span><br/> | <span data-ttu-id="0ef7a-200">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0ef7a-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ef7a-201">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0ef7a-201">Namespace</span></span><br/>                | <span data-ttu-id="0ef7a-202">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0ef7a-202">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0ef7a-203">MOF</span><span class="sxs-lookup"><span data-stu-id="0ef7a-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ef7a-204"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ef7a-204"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ef7a-205">DLL</span><span class="sxs-lookup"><span data-stu-id="0ef7a-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ef7a-206"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ef7a-206"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

