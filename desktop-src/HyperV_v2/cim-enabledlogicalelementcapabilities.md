---
description: Descrive le restrizioni sulle proprietà di un \_ oggetto ENABLEDLOGICALELEMENT CIM associato.
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: Classe CIM_EnabledLogicalElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35f400643e01821667c999342603fd402a3ae419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312924"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a><span data-ttu-id="8e872-103">CIM \_ EnabledLogicalElementCapabilities (classe)</span><span class="sxs-lookup"><span data-stu-id="8e872-103">CIM\_EnabledLogicalElementCapabilities class</span></span>

<span data-ttu-id="8e872-104">Descrive le restrizioni sulle proprietà di un oggetto [**\_ EnabledLogicalElement CIM**](cim-enabledlogicalelement.md) associato.</span><span class="sxs-lookup"><span data-stu-id="8e872-104">Describes the restrictions on the properties of an associated [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e872-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e872-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="8e872-106">Members</span><span class="sxs-lookup"><span data-stu-id="8e872-106">Members</span></span>

<span data-ttu-id="8e872-107">La classe **CIM \_ EnabledLogicalElementCapabilities** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8e872-107">The **CIM\_EnabledLogicalElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="8e872-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e872-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e872-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e872-109">Properties</span></span>

<span data-ttu-id="8e872-110">La classe **CIM \_ EnabledLogicalElementCapabilities** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8e872-110">The **CIM\_EnabledLogicalElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e872-111">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="8e872-111">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e872-112">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8e872-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e872-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e872-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e872-114">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-swapi. Incis-T11 \| swapping \_ unità \_ config i \_ Caps \_ T \| EditName "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Managed**](cim-managedelement.md).**ElementName**")</span><span class="sxs-lookup"><span data-stu-id="8e872-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|EditName"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedElement**](cim-managedelement.md).**ElementName**")</span></span>
</dt> </dl>

<span data-ttu-id="8e872-115">**true** se la proprietà **ElementName** dell'elemento logico abilitato può essere modificata. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8e872-115">**true** if the **ElementName** property of the enabled logical element can be modified; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="8e872-116">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="8e872-116">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e872-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8e872-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e872-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e872-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e872-119">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElementCapabilities**.**MaxElementNameLen**")</span><span class="sxs-lookup"><span data-stu-id="8e872-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElementCapabilities**.**MaxElementNameLen**")</span></span>
</dt> </dl>

<span data-ttu-id="8e872-120">Espressione regolare che indica le restrizioni sulla proprietà **ElementName** dell'elemento logico Enable.</span><span class="sxs-lookup"><span data-stu-id="8e872-120">A regular expression that indicates the restrictions on the **ElementName** property of the enable logical element.</span></span> <span data-ttu-id="8e872-121">Vedere *DMTF standard ABNF con la Guida all'utilizzo della specifica del profilo di gestione*, Appendice C per la sintassi consentita.</span><span class="sxs-lookup"><span data-stu-id="8e872-121">See *DMTF standard ABNF with the Management Profile Specification Usage Guide*, appendix C for the permitted syntax.</span></span>

> [!Note]  
> <span data-ttu-id="8e872-122">Se questa proprietà e la proprietà **ElementNameMask** dell'elemento logico Enable descrivono la lunghezza massima di **ElementName**, viene usato il valore più piccolo.</span><span class="sxs-lookup"><span data-stu-id="8e872-122">If this property and the **ElementNameMask** property of the enable logical element describe the maximum length of **ElementName**, the smaller value is used.</span></span>

 

</dd> <dt>

<span data-ttu-id="8e872-123">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="8e872-123">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e872-124">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e872-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e872-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e872-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e872-126">Qualificatori: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-swapi. INCIs-T11 \| swapi \_ unit \_ config \_ Caps \_ T \| MaxNameChars "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ FCSwitchCapabilities. ElementNameEditSupported ","**CIM \_ EnabledLogicalElementCapabilities**.**ElementNameMask**")</span><span class="sxs-lookup"><span data-stu-id="8e872-126">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|MaxNameChars"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_FCSwitchCapabilities.ElementNameEditSupported", "**CIM\_EnabledLogicalElementCapabilities**.**ElementNameMask**")</span></span>
</dt> </dl>

<span data-ttu-id="8e872-127">Lunghezza massima supportata della proprietà **ElementName** dell'elemento logico abilitato.</span><span class="sxs-lookup"><span data-stu-id="8e872-127">The maximum supported length of the **ElementName** property of the enabled logical element.</span></span>

</dd> <dt>

<span data-ttu-id="8e872-128">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="8e872-128">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e872-129">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e872-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8e872-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e872-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e872-131">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")</span><span class="sxs-lookup"><span data-stu-id="8e872-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")</span></span>
</dt> </dl>

<span data-ttu-id="8e872-132">Gli stati possibili che possono essere richiesti sull'elemento logico abilitato tramite il metodo [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="8e872-132">The possible states that can be requested on the enabled logical element by the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8e872-133">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="8e872-133">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8e872-134">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="8e872-134">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="8e872-135">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="8e872-135">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="8e872-136">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="8e872-136">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="8e872-137">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="8e872-137">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="8e872-138">**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="8e872-138">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="8e872-139">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="8e872-139">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="8e872-140">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="8e872-140">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="8e872-141">**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="8e872-141">**Reset** (11)</span></span>


<span data-ttu-id="8e872-142"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8e872-142"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8e872-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e872-143">Requirements</span></span>



| <span data-ttu-id="8e872-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e872-144">Requirement</span></span> | <span data-ttu-id="8e872-145">Valore</span><span class="sxs-lookup"><span data-stu-id="8e872-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e872-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e872-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8e872-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8e872-147">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8e872-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e872-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8e872-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e872-149">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8e872-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8e872-150">Namespace</span></span><br/>                | <span data-ttu-id="8e872-151">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8e872-151">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8e872-152">MOF</span><span class="sxs-lookup"><span data-stu-id="8e872-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e872-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e872-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e872-154">DLL</span><span class="sxs-lookup"><span data-stu-id="8e872-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e872-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8e872-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8e872-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e872-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e872-157">**\_Funzionalità CIM**</span><span class="sxs-lookup"><span data-stu-id="8e872-157">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

