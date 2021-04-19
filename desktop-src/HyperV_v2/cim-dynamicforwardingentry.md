---
description: Rappresenta una voce nel database di inoltri associato alla \_ classe TRANSPARENTBRIDGINGSERVICE CIM.
ms.assetid: 4c3afe7c-f7e5-4a83-8ba1-f0b1909cee52
title: Classe CIM_DynamicForwardingEntry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DynamicForwardingEntry
- CIM_DynamicForwardingEntry.SystemCreationClassName
- CIM_DynamicForwardingEntry.SystemName
- CIM_DynamicForwardingEntry.ServiceCreationClassName
- CIM_DynamicForwardingEntry.ServiceName
- CIM_DynamicForwardingEntry.CreationClassName
- CIM_DynamicForwardingEntry.MACAddress
- CIM_DynamicForwardingEntry.DynamicStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65cf4f1bc5e678089d54dd99a09a6d3b7aeb3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308347"
---
# <a name="cim_dynamicforwardingentry-class"></a><span data-ttu-id="8bcaa-103">CIM \_ DynamicForwardingEntry (classe)</span><span class="sxs-lookup"><span data-stu-id="8bcaa-103">CIM\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="8bcaa-104">Rappresenta una voce nel database di inoltri associato alla classe [**\_ TransparentBridgingService CIM**](cim-transparentbridgingservice.md) .</span><span class="sxs-lookup"><span data-stu-id="8bcaa-104">Represents an entry in the forwarding database associated with the [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bcaa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bcaa-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_DynamicForwardingEntry : CIM_LogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string ServiceCreationClassName;
  string ServiceName;
  string CreationClassName;
  string MACAddress;
  uint16 DynamicStatus;
};
```

## <a name="members"></a><span data-ttu-id="8bcaa-106">Members</span><span class="sxs-lookup"><span data-stu-id="8bcaa-106">Members</span></span>

<span data-ttu-id="8bcaa-107">La classe **CIM \_ DynamicForwardingEntry** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8bcaa-107">The **CIM\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="8bcaa-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8bcaa-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bcaa-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8bcaa-109">Properties</span></span>

<span data-ttu-id="8bcaa-110">La classe **CIM \_ DynamicForwardingEntry** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8bcaa-110">The **CIM\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bcaa-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcaa-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8bcaa-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-114">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8bcaa-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8bcaa-115">Nome della classe o della sottoclasse utilizzata per creare l'istanza.</span><span class="sxs-lookup"><span data-stu-id="8bcaa-115">The name of the class or the subclass used to create the instance.</span></span> <span data-ttu-id="8bcaa-116">Se utilizzata con le altre proprietà chiave di questa classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="8bcaa-116">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="8bcaa-117">**DynamicStatus**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-117">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcaa-118">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8bcaa-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-120">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbStatus ")</span><span class="sxs-lookup"><span data-stu-id="8bcaa-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8bcaa-121">Stato della voce.</span><span class="sxs-lookup"><span data-stu-id="8bcaa-121">The status of the entry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8bcaa-122">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="8bcaa-122">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>

<span data-ttu-id="8bcaa-123">**Non valido** (2)</span><span class="sxs-lookup"><span data-stu-id="8bcaa-123">**Invalid** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>

<span data-ttu-id="8bcaa-124">**Appreso** (3)</span><span class="sxs-lookup"><span data-stu-id="8bcaa-124">**Learned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>

<span data-ttu-id="8bcaa-125">**Self** (4)</span><span class="sxs-lookup"><span data-stu-id="8bcaa-125">**Self** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>

<span data-ttu-id="8bcaa-126">**Mgmt** (5)</span><span class="sxs-lookup"><span data-stu-id="8bcaa-126">**Mgmt** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8bcaa-127">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-127">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcaa-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8bcaa-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-130">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbAddress ")</span><span class="sxs-lookup"><span data-stu-id="8bcaa-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbAddress")</span></span>
</dt> </dl>

<span data-ttu-id="8bcaa-131">Indirizzo MAC unicast per il quale il servizio bridging filtra le informazioni.</span><span class="sxs-lookup"><span data-stu-id="8bcaa-131">The Unicast MAC address for which the bridging service filters information.</span></span> <span data-ttu-id="8bcaa-132">L'indirizzo MAC è formattato come dodici cifre esadecimali, ad esempio 010203040506, con ogni coppia che rappresenta uno dei sei ottetti dell'indirizzo MAC in un ordine di bit canonico in base a RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="8bcaa-132">The MAC address is formatted as twelve hexadecimal digits, such as 010203040506, with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="8bcaa-133">**ServiceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-133">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcaa-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8bcaa-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-136">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ servizio CIM**](cim-service.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="8bcaa-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="8bcaa-137">Valore **CreationClassName** dell'oggetto servizio di ambito.</span><span class="sxs-lookup"><span data-stu-id="8bcaa-137">The **CreationClassName** value of the scoping service object.</span></span>

</dd> <dt>

<span data-ttu-id="8bcaa-138">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-138">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcaa-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8bcaa-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-141">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ servizio CIM**](cim-service.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="8bcaa-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="8bcaa-142">Nome del servizio di ambito.</span><span class="sxs-lookup"><span data-stu-id="8bcaa-142">The name of the scoping service.</span></span>

</dd> <dt>

<span data-ttu-id="8bcaa-143">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcaa-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8bcaa-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-146">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="8bcaa-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="8bcaa-147">Valore **CreationClassName** dell'oggetto di sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="8bcaa-147">The **CreationClassName** value of the scoping system object.</span></span>

</dd> <dt>

<span data-ttu-id="8bcaa-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bcaa-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8bcaa-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bcaa-151">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="8bcaa-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="8bcaa-152">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="8bcaa-152">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bcaa-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bcaa-153">Requirements</span></span>



| <span data-ttu-id="8bcaa-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bcaa-154">Requirement</span></span> | <span data-ttu-id="8bcaa-155">Valore</span><span class="sxs-lookup"><span data-stu-id="8bcaa-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bcaa-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bcaa-156">Minimum supported client</span></span><br/> | <span data-ttu-id="8bcaa-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8bcaa-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8bcaa-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bcaa-158">Minimum supported server</span></span><br/> | <span data-ttu-id="8bcaa-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8bcaa-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8bcaa-160">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8bcaa-160">Namespace</span></span><br/>                | <span data-ttu-id="8bcaa-161">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8bcaa-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8bcaa-162">MOF</span><span class="sxs-lookup"><span data-stu-id="8bcaa-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bcaa-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bcaa-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bcaa-164">DLL</span><span class="sxs-lookup"><span data-stu-id="8bcaa-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bcaa-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8bcaa-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8bcaa-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bcaa-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bcaa-167">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="8bcaa-167">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

