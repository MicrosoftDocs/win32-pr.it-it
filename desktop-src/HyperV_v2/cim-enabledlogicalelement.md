---
description: Rappresenta un elemento logico che può essere abilitato e disabilitato.
ms.assetid: 52eed77e-f3f1-4489-8eff-a8ebebd5e1a8
title: Classe CIM_EnabledLogicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement
- CIM_EnabledLogicalElement.EnabledState
- CIM_EnabledLogicalElement.OtherEnabledState
- CIM_EnabledLogicalElement.RequestedState
- CIM_EnabledLogicalElement.EnabledDefault
- CIM_EnabledLogicalElement.TimeOfLastStateChange
- CIM_EnabledLogicalElement.AvailableRequestedStates
- CIM_EnabledLogicalElement.TransitioningToState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e2d7043653b219bc0d54ac7bee3393275dab673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312926"
---
# <a name="cim_enabledlogicalelement-class"></a><span data-ttu-id="6b99e-103">CIM \_ EnabledLogicalElement (classe)</span><span class="sxs-lookup"><span data-stu-id="6b99e-103">CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="6b99e-104">Rappresenta un elemento logico che può essere abilitato e disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6b99e-104">Represents a logical element that can be enabled and disabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b99e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b99e-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_EnabledLogicalElement : CIM_LogicalElement
{
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
};
```

## <a name="members"></a><span data-ttu-id="6b99e-106">Members</span><span class="sxs-lookup"><span data-stu-id="6b99e-106">Members</span></span>

<span data-ttu-id="6b99e-107">La classe **CIM \_ EnabledLogicalElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6b99e-107">The **CIM\_EnabledLogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="6b99e-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="6b99e-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="6b99e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6b99e-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6b99e-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6b99e-110">Methods</span></span>

<span data-ttu-id="6b99e-111">La classe **CIM \_ EnabledLogicalElement** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6b99e-111">The **CIM\_EnabledLogicalElement** class has these methods.</span></span>



| <span data-ttu-id="6b99e-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="6b99e-112">Method</span></span>                                                                     | <span data-ttu-id="6b99e-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b99e-113">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b99e-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="6b99e-114">**RequestStateChange**</span></span>](cim-enabledlogicalelement-requeststatechange.md) | <span data-ttu-id="6b99e-115">Richiede che lo stato dell'elemento venga modificato nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="6b99e-115">Requests that the state of the element be changed to the specified value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6b99e-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6b99e-116">Properties</span></span>

<span data-ttu-id="6b99e-117">La classe **CIM \_ EnabledLogicalElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6b99e-117">The **CIM\_EnabledLogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b99e-118">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="6b99e-118">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b99e-119">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b99e-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b99e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-121">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**RequestStateChange**","[**CIM \_ EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md).**RequestedStatesSupported**")</span><span class="sxs-lookup"><span data-stu-id="6b99e-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "[**CIM\_EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md).**RequestedStatesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="6b99e-122">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="6b99e-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<span data-ttu-id="6b99e-123">I valori elencati devono essere un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza **\_ EnabledLogicalElementCapabilities CIM** associata.</span><span class="sxs-lookup"><span data-stu-id="6b99e-123">The listed values must be a subset of the values that are contained in the **RequestedStatesSupported** property of the associated **CIM\_EnabledLogicalElementCapabilities** instance.</span></span> <span data-ttu-id="6b99e-124">Questa proprietà è **null** se l'implementazione non è in grado di determinare il set di valori possibili per lo stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6b99e-124">This property is **NULL** if the implementation cannot determine the set of possible values for the current state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6b99e-125">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="6b99e-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6b99e-126">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="6b99e-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="6b99e-127">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="6b99e-127">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="6b99e-128">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="6b99e-128">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="6b99e-129">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="6b99e-129">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="6b99e-130">**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="6b99e-130">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="6b99e-131">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="6b99e-131">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="6b99e-132">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="6b99e-132">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="6b99e-133">**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="6b99e-133">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6b99e-134">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6b99e-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b99e-135">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="6b99e-135">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b99e-136">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b99e-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6b99e-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b99e-138">Indica la configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="6b99e-138">Indicates an administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="6b99e-139">Il valore predefinito è **abilitato** (2).</span><span class="sxs-lookup"><span data-stu-id="6b99e-139">The default value **Enabled** (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6b99e-140">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="6b99e-140">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6b99e-141">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="6b99e-141">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6b99e-142">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="6b99e-142">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="6b99e-143">**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="6b99e-143">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Default"></span><span id="no_default"></span><span id="NO_DEFAULT"></span>

<span data-ttu-id="6b99e-144">**Nessun valore predefinito** (7)</span><span class="sxs-lookup"><span data-stu-id="6b99e-144">**No Default** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="6b99e-145">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="6b99e-145">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6b99e-146">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6b99e-146">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6b99e-147">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6b99e-147">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b99e-148">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="6b99e-148">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b99e-149">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b99e-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b99e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-151">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**OtherEnabledState**")</span><span class="sxs-lookup"><span data-stu-id="6b99e-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**OtherEnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="6b99e-152">Indica lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="6b99e-152">Indicates the enabled state of an element.</span></span> <span data-ttu-id="6b99e-153">I valori possibili includono le transizioni tra gli Stati.</span><span class="sxs-lookup"><span data-stu-id="6b99e-153">Possible values include the transitions between states.</span></span> <span data-ttu-id="6b99e-154">Ad esempio, l' **arresto** (4) e l' **avvio** di (10) sono stati temporanei tra l' **Abilitazione** e la **disabilitazione**.</span><span class="sxs-lookup"><span data-stu-id="6b99e-154">For example, **Shutting Down** (4) and **Starting** (10) are transient states between **Enabled** and **Disabled**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b99e-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6b99e-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6b99e-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6b99e-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6b99e-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="6b99e-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-158">L'elemento è o potrebbe eseguire comandi, elaborerà tutti i comandi in coda e accoda le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="6b99e-158">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6b99e-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="6b99e-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-160">l'elemento non esegue i comandi e rilascia tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="6b99e-160">the element will not execute commands and will drop any new requests.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="6b99e-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="6b99e-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-162">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6b99e-162">The element is in the process of going to a Disabled state.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6b99e-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="6b99e-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-164">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="6b99e-164">The element does not support being enabled or disabled.</span></span>

</dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="6b99e-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="6b99e-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-166">È possibile che l'elemento stia completando i comandi e eliminerà tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="6b99e-166">The element might be completing commands, and will drop any new requests.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6b99e-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (7)</span><span class="sxs-lookup"><span data-stu-id="6b99e-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-168">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="6b99e-168">The element is in a test state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="6b99e-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Posticipato** (8)</span><span class="sxs-lookup"><span data-stu-id="6b99e-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-170">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="6b99e-170">The element might be completing commands, but will queue any new requests.</span></span>

</dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="6b99e-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="6b99e-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-172">Indica che l'elemento è abilitato ma in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="6b99e-172">That the element is enabled but in a restricted mode.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6b99e-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** in corso (10)</span><span class="sxs-lookup"><span data-stu-id="6b99e-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-174">L'elemento sta per passare a uno stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="6b99e-174">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="6b99e-175">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="6b99e-175">New requests are queued.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6b99e-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (11.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6b99e-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (11..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6b99e-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6b99e-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b99e-178">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="6b99e-178">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b99e-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6b99e-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b99e-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-181">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="6b99e-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="6b99e-182">Descrive lo stato dell'elemento quando il valore della proprietà **EnabledState** è **other**.</span><span class="sxs-lookup"><span data-stu-id="6b99e-182">Describes the state of the element when the value of the **EnabledState** property is **Other**.</span></span> <span data-ttu-id="6b99e-183">Questa proprietà deve essere impostata su **null** se **EnabledState** non è **diverso**.</span><span class="sxs-lookup"><span data-stu-id="6b99e-183">This property must be set to **NULL** when **EnabledState** is not **Other**.</span></span>

</dd> <dt>

<span data-ttu-id="6b99e-184">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="6b99e-184">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b99e-185">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b99e-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b99e-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-187">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="6b99e-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="6b99e-188">Indica l'ultimo stato richiesto per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="6b99e-188">Indicates the last requested state for the element.</span></span> <span data-ttu-id="6b99e-189">Lo stato corrente è indicato dalla proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="6b99e-189">The current state is indicated by the **EnabledState** property.</span></span> <span data-ttu-id="6b99e-190">Questa proprietà consente di confrontare gli ultimi stati richiesti e correnti.</span><span class="sxs-lookup"><span data-stu-id="6b99e-190">This property enables you to compare the last requested and current states.</span></span>

> [!Note]  
> <span data-ttu-id="6b99e-191">Se il valore della proprietà **EnabledState** non è **applicabile**, questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="6b99e-191">When the value of the **EnabledState** property is **Not Applicable**, this property has no meaning.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b99e-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6b99e-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-193">L'ultimo stato richiesto per l'elemento è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6b99e-193">The last requested state for the element is unknown.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6b99e-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="6b99e-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6b99e-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="6b99e-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-196">Richiede una disabilitazione immediata dell'elemento, in modo che non esegua né accetti comandi o richieste di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="6b99e-196">Requests an immediate disabling of the element, such that it will not execute or accept any commands or processing requests.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="6b99e-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="6b99e-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-198">Richiede una transizione ordinata allo stato disabilitato e potrebbe comportare la rimozione dell'alimentazione, per cancellare completamente qualsiasi stato esistente.</span><span class="sxs-lookup"><span data-stu-id="6b99e-198">Requests an orderly transition to the Disabled state, and might involve removing power, to completely erase any existing state.</span></span>

</dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="6b99e-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Nessuna modifica** (5)</span><span class="sxs-lookup"><span data-stu-id="6b99e-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-200">Deprecato anziché indicare che l'ultimo stato richiesto è "Unknown" (0).</span><span class="sxs-lookup"><span data-stu-id="6b99e-200">Deprecated in lieu of indicating the last requested state is "Unknown" (0).</span></span> <span data-ttu-id="6b99e-201">Se lo stato ultimo richiesto o desiderato è sconosciuto, **RequestedState** deve avere il valore "Unknown" (0), ma può avere il valore "No Change" (5).</span><span class="sxs-lookup"><span data-stu-id="6b99e-201">If the last requested or desired state is unknown, **RequestedState** should have the value "Unknown" (0), but may have the value "No Change" (5).</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="6b99e-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="6b99e-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-203">All'elemento è stata richiesta la transizione al **EnabledState** abilitato ma offline.</span><span class="sxs-lookup"><span data-stu-id="6b99e-203">The element has been requested to transition to the Enabled but Offline **EnabledState**.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="6b99e-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="6b99e-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="6b99e-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Posticipato** (8)</span><span class="sxs-lookup"><span data-stu-id="6b99e-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="6b99e-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="6b99e-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="6b99e-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="6b99e-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-208">Si riferisce all'operazione "arresta" e quindi allo stato "Enabled".</span><span class="sxs-lookup"><span data-stu-id="6b99e-208">Refers to doing a "Shut Down" and then moving to an "Enabled" state.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="6b99e-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="6b99e-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="6b99e-210">Indica che l'elemento viene innanzitutto "disabilitato" e quindi "Enabled".</span><span class="sxs-lookup"><span data-stu-id="6b99e-210">Indicates that the element is first "Disabled" and then "Enabled".</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6b99e-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (12)</span><span class="sxs-lookup"><span data-stu-id="6b99e-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6b99e-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6b99e-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6b99e-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6b99e-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b99e-214">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="6b99e-214">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b99e-215">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b99e-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b99e-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b99e-217">Indica quando l'elemento è stato modificato per ultimo.</span><span class="sxs-lookup"><span data-stu-id="6b99e-217">Indicates when the element last changed state.</span></span> <span data-ttu-id="6b99e-218">Se lo stato dell'elemento non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo zero.</span><span class="sxs-lookup"><span data-stu-id="6b99e-218">If the state of the element has not changed and this property is populated, then it must be set to a zero interval value.</span></span> <span data-ttu-id="6b99e-219">Se è stata richiesta una modifica di stato, ma è stata rifiutata o non è ancora stata elaborata, la proprietà non deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="6b99e-219">If a state change was requested, but was rejected or is not yet processed, the property must not be updated.</span></span>

</dd> <dt>

<span data-ttu-id="6b99e-220">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="6b99e-220">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b99e-221">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b99e-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b99e-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b99e-223">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**RequestStateChange**","**CIM \_ EnabledLogicalElement**.**RequestedState**","**CIM \_ EnabledLogicalElement**.**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="6b99e-223">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "**CIM\_EnabledLogicalElement**.**RequestedState**", "**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="6b99e-224">Indica lo stato di destinazione in cui l'istanza è in corso di modifica.</span><span class="sxs-lookup"><span data-stu-id="6b99e-224">Indicates the target state to which the instance is changing.</span></span>

<span data-ttu-id="6b99e-225">Il valore **Nessuna modifica** indica che non è in corso alcuna transizione.</span><span class="sxs-lookup"><span data-stu-id="6b99e-225">A value of **No Change** indicates that no transition is in progress.</span></span> <span data-ttu-id="6b99e-226">Il valore **non applicabile** indica che l'implementazione non riporta le transizioni in corso.</span><span class="sxs-lookup"><span data-stu-id="6b99e-226">A value of **Not Applicable** indicates that the implementation does not report ongoing transitions.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6b99e-227">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6b99e-227">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6b99e-228">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="6b99e-228">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6b99e-229">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="6b99e-229">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="6b99e-230">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="6b99e-230">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="6b99e-231">**Nessuna modifica** (5)</span><span class="sxs-lookup"><span data-stu-id="6b99e-231">**No Change** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="6b99e-232">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="6b99e-232">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="6b99e-233">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="6b99e-233">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="6b99e-234">**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="6b99e-234">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="6b99e-235">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="6b99e-235">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="6b99e-236">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="6b99e-236">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="6b99e-237">**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="6b99e-237">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6b99e-238">**Non applicabile** (12)</span><span class="sxs-lookup"><span data-stu-id="6b99e-238">**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6b99e-239">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6b99e-239">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="6b99e-240"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6b99e-240"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6b99e-241">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b99e-241">Requirements</span></span>



| <span data-ttu-id="6b99e-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b99e-242">Requirement</span></span> | <span data-ttu-id="6b99e-243">Valore</span><span class="sxs-lookup"><span data-stu-id="6b99e-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b99e-244">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b99e-244">Minimum supported client</span></span><br/> | <span data-ttu-id="6b99e-245">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6b99e-245">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6b99e-246">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b99e-246">Minimum supported server</span></span><br/> | <span data-ttu-id="6b99e-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6b99e-247">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6b99e-248">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6b99e-248">Namespace</span></span><br/>                | <span data-ttu-id="6b99e-249">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6b99e-249">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6b99e-250">MOF</span><span class="sxs-lookup"><span data-stu-id="6b99e-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b99e-251"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b99e-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b99e-252">DLL</span><span class="sxs-lookup"><span data-stu-id="6b99e-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b99e-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6b99e-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6b99e-254">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b99e-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b99e-255">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="6b99e-255">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

