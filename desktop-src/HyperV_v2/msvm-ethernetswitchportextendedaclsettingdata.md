---
description: Rappresenta le impostazioni ACL della porta estesa.
ms.assetid: 357dd891-6692-4ffc-b8a8-4ece40d4af28
title: Classe Msvm_EthernetSwitchPortExtendedAclSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortExtendedAclSettingData
- Msvm_EthernetSwitchPortExtendedAclSettingData.Name
- Msvm_EthernetSwitchPortExtendedAclSettingData.Direction
- Msvm_EthernetSwitchPortExtendedAclSettingData.Action
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemoteIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalPort
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemotePort
- Msvm_EthernetSwitchPortExtendedAclSettingData.Protocol
- Msvm_EthernetSwitchPortExtendedAclSettingData.Weight
- Msvm_EthernetSwitchPortExtendedAclSettingData.Stateful
- Msvm_EthernetSwitchPortExtendedAclSettingData.IdleSessionTimeout
- Msvm_EthernetSwitchPortExtendedAclSettingData.IsolationID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25ae81e4f00e87e41170ac5713ced0d9b523c844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313858"
---
# <a name="msvm_ethernetswitchportextendedaclsettingdata-class"></a><span data-ttu-id="afdd6-103">\_Classe MSVM EthernetSwitchPortExtendedAclSettingData</span><span class="sxs-lookup"><span data-stu-id="afdd6-103">Msvm\_EthernetSwitchPortExtendedAclSettingData class</span></span>

<span data-ttu-id="afdd6-104">Rappresenta le impostazioni ACL della porta estesa.</span><span class="sxs-lookup"><span data-stu-id="afdd6-104">Represents the extended port ACL settings.</span></span>

<span data-ttu-id="afdd6-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="afdd6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="afdd6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afdd6-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("CD168FF0-A16D-4514-B7B5-8BBBA791A928"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Extended ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortExtendedAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  Name = "";
  uint8   Direction = 0;
  uint8   Action = 0;
  string  LocalIPAddress = "ANY";
  string  RemoteIPAddress = "ANY";
  string  LocalPort = "ANY";
  string  RemotePort = "ANY";
  string  Protocol = "ANY";
  Uint16  Weight = 0;
  Boolean Stateful = FALSE;
  Uint16  IdleSessionTimeout = 255;
  Uint32  IsolationID = 0;
};
```

## <a name="members"></a><span data-ttu-id="afdd6-107">Members</span><span class="sxs-lookup"><span data-stu-id="afdd6-107">Members</span></span>

<span data-ttu-id="afdd6-108">La **classe \_ EthernetSwitchPortExtendedAclSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="afdd6-108">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="afdd6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="afdd6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afdd6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="afdd6-110">Properties</span></span>

<span data-ttu-id="afdd6-111">La **classe \_ EthernetSwitchPortExtendedAclSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="afdd6-111">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afdd6-112">**Azione**</span><span class="sxs-lookup"><span data-stu-id="afdd6-112">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-113">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="afdd6-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-115">Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-115">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-116">Azione dell'ACL esteso.</span><span class="sxs-lookup"><span data-stu-id="afdd6-116">The action of the extended ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="afdd6-117">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="afdd6-118">**Consenti** (1)</span><span class="sxs-lookup"><span data-stu-id="afdd6-118">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="afdd6-119">**Nega** (2)</span><span class="sxs-lookup"><span data-stu-id="afdd6-119">**Deny** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="afdd6-120">**Direzione**</span><span class="sxs-lookup"><span data-stu-id="afdd6-120">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-121">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="afdd6-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-123">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-123">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-124">Indica se l'ACL esteso si applica alla direzione in ingresso o in uscita.</span><span class="sxs-lookup"><span data-stu-id="afdd6-124">Indicates if the extended ACL applies to incoming or outgoing direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="afdd6-125">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="afdd6-126">**In ingresso** (1)</span><span class="sxs-lookup"><span data-stu-id="afdd6-126">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="afdd6-127">**In uscita** (2)</span><span class="sxs-lookup"><span data-stu-id="afdd6-127">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="afdd6-128">**IdleSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="afdd6-128">**IdleSessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afdd6-129">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-131">Qualificatori: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-131">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-132">Valore di timeout della sessione inattiva (in secondi) per l'ACL con stato.</span><span class="sxs-lookup"><span data-stu-id="afdd6-132">Idle session timeout value (in seconds) for stateful ACL.</span></span>

</dd> <dt>

<span data-ttu-id="afdd6-133">**IsolationID**</span><span class="sxs-lookup"><span data-stu-id="afdd6-133">**IsolationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afdd6-134">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-136">Qualificatori: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="afdd6-136">Qualifiers: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-137">ID di isolamento per cui deve essere applicato l'ACL esteso.</span><span class="sxs-lookup"><span data-stu-id="afdd6-137">Isolation ID for which the extended ACL should be applied.</span></span>

</dd> <dt>

<span data-ttu-id="afdd6-138">**LocalIPAddress**</span><span class="sxs-lookup"><span data-stu-id="afdd6-138">**LocalIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="afdd6-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-141">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-142">Indirizzo IP locale.</span><span class="sxs-lookup"><span data-stu-id="afdd6-142">The local IP address.</span></span>

</dd> <dt>

<span data-ttu-id="afdd6-143">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="afdd6-143">**LocalPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="afdd6-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-146">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-147">Intervallo di porte locali.</span><span class="sxs-lookup"><span data-stu-id="afdd6-147">The local port range.</span></span>

</dd> <dt>

<span data-ttu-id="afdd6-148">**Nome**</span><span class="sxs-lookup"><span data-stu-id="afdd6-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="afdd6-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-151">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-152">Nome descrittivo dell'ACL esteso.</span><span class="sxs-lookup"><span data-stu-id="afdd6-152">The friendly name of the Extended ACL.</span></span>

</dd> <dt>

<span data-ttu-id="afdd6-153">**Protocollo**</span><span class="sxs-lookup"><span data-stu-id="afdd6-153">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="afdd6-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-156">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-157">Stringa del protocollo.</span><span class="sxs-lookup"><span data-stu-id="afdd6-157">The protocol string.</span></span>

</dd> <dt>

<span data-ttu-id="afdd6-158">**RemoteIPAddress**</span><span class="sxs-lookup"><span data-stu-id="afdd6-158">**RemoteIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="afdd6-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-161">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-162">Indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="afdd6-162">The remote IP address.</span></span>

</dd> <dt>

<span data-ttu-id="afdd6-163">**RemotePort**</span><span class="sxs-lookup"><span data-stu-id="afdd6-163">**RemotePort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="afdd6-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-166">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-167">Intervallo di porte remote.</span><span class="sxs-lookup"><span data-stu-id="afdd6-167">The remote port range.</span></span>

</dd> <dt>

<span data-ttu-id="afdd6-168">**Con stato**</span><span class="sxs-lookup"><span data-stu-id="afdd6-168">**Stateful**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-169">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="afdd6-169">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-171">Qualificatori: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-171">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-172">Indica se l'ACL esteso è con stato o senza stato.</span><span class="sxs-lookup"><span data-stu-id="afdd6-172">Indicates if the extended ACL is stateful or stateless.</span></span>

</dd> <dt>

<span data-ttu-id="afdd6-173">**Weight**</span><span class="sxs-lookup"><span data-stu-id="afdd6-173">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afdd6-174">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="afdd6-174">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="afdd6-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="afdd6-176">Qualificatori: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="afdd6-176">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="afdd6-177">Spessore applicato all'ACL esteso.</span><span class="sxs-lookup"><span data-stu-id="afdd6-177">The weight applied to the extended ACL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afdd6-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afdd6-178">Requirements</span></span>



| <span data-ttu-id="afdd6-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="afdd6-179">Requirement</span></span> | <span data-ttu-id="afdd6-180">Valore</span><span class="sxs-lookup"><span data-stu-id="afdd6-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afdd6-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afdd6-181">Minimum supported client</span></span><br/> | <span data-ttu-id="afdd6-182">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="afdd6-182">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="afdd6-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afdd6-183">Minimum supported server</span></span><br/> | <span data-ttu-id="afdd6-184">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="afdd6-184">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="afdd6-185">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="afdd6-185">Namespace</span></span><br/>                | <span data-ttu-id="afdd6-186">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="afdd6-186">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="afdd6-187">MOF</span><span class="sxs-lookup"><span data-stu-id="afdd6-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afdd6-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afdd6-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="afdd6-189">DLL</span><span class="sxs-lookup"><span data-stu-id="afdd6-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afdd6-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="afdd6-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="afdd6-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afdd6-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afdd6-192">**\_EthernetSwitchPortFeatureSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="afdd6-192">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

