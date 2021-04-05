---
description: Rappresenta un valore della metrica definito da un'istanza della \_ classe MSVM BaseMetricDefinition.
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Classe Msvm_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0e566de4822b271dcd4633c3dba35f7c88495bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884618"
---
# <a name="msvm_basemetricvalue-class"></a><span data-ttu-id="05eca-103">\_Classe MSVM BaseMetricValue</span><span class="sxs-lookup"><span data-stu-id="05eca-103">Msvm\_BaseMetricValue class</span></span>

<span data-ttu-id="05eca-104">Rappresenta un valore della metrica definito da un'istanza della classe [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="05eca-104">Represents a metric value defined by an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class.</span></span>

<span data-ttu-id="05eca-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="05eca-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="05eca-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05eca-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a><span data-ttu-id="05eca-107">Members</span><span class="sxs-lookup"><span data-stu-id="05eca-107">Members</span></span>

<span data-ttu-id="05eca-108">La **classe \_ BaseMetricValue di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="05eca-108">The **Msvm\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="05eca-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="05eca-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05eca-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="05eca-110">Properties</span></span>

<span data-ttu-id="05eca-111">La **classe \_ BaseMetricValue di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="05eca-111">The **Msvm\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05eca-112">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="05eca-112">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05eca-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05eca-115">Specifica una dimensione di suddivisione dalla matrice **BreakdownDimensions** definita nel [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md)associato.</span><span class="sxs-lookup"><span data-stu-id="05eca-115">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="05eca-116">Si tratta della dimensione in base alla quale questo set di valori di metrica viene suddiviso.</span><span class="sxs-lookup"><span data-stu-id="05eca-116">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="05eca-117">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-117">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05eca-118">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="05eca-118">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05eca-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05eca-121">Definisce un valore della proprietà **BreakdownDimension** definita per questa istanza del valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="05eca-121">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="05eca-122">Ad esempio, se **BreakdownDimension** è "transactionName", questa proprietà può assegnare un nome alla transazione effettiva a cui si applica questo particolare valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="05eca-122">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="05eca-123">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-123">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05eca-124">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="05eca-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05eca-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05eca-127">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="05eca-127">A short description of the object.</span></span> <span data-ttu-id="05eca-128">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05eca-129">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="05eca-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05eca-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05eca-132">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="05eca-132">A description of the object.</span></span> <span data-ttu-id="05eca-133">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05eca-134">**Duration**</span><span class="sxs-lookup"><span data-stu-id="05eca-134">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-135">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="05eca-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05eca-137">Specifica la durata del periodo di validità del valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="05eca-137">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="05eca-138">Questa proprietà non deve esistere per gli indicatori di tempo che si applicano solo a un punto nel tempo, ma deve essere specificata per i valori considerati validi per un determinato periodo di tempo, ad esempio il campionamento.</span><span class="sxs-lookup"><span data-stu-id="05eca-138">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="05eca-139">Se la proprietà **Duration** esiste e non è **null**, la proprietà **timestamp** specifica la fine dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="05eca-139">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="05eca-140">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-140">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05eca-141">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="05eca-141">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05eca-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05eca-144">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="05eca-144">A display name for the object.</span></span> <span data-ttu-id="05eca-145">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05eca-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="05eca-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05eca-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05eca-149">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="05eca-149">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="05eca-150">Stringa che identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="05eca-150">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="05eca-151">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05eca-152">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="05eca-152">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05eca-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05eca-155">Nome descrittivo per l'elemento a cui appartiene il valore della metrica, ovvero l'elemento misurato.</span><span class="sxs-lookup"><span data-stu-id="05eca-155">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="05eca-156">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-156">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05eca-157">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="05eca-157">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05eca-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05eca-160">Chiave dell'istanza di [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md) per questo valore.</span><span class="sxs-lookup"><span data-stu-id="05eca-160">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="05eca-161">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-161">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05eca-162">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="05eca-162">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="05eca-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05eca-165">Valore della metrica rappresentata come stringa.</span><span class="sxs-lookup"><span data-stu-id="05eca-165">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="05eca-166">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-166">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05eca-167">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="05eca-167">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-168">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="05eca-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05eca-170">Specifica l'ora in cui il valore della metrica è stato acquisito o calcolato.</span><span class="sxs-lookup"><span data-stu-id="05eca-170">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="05eca-171">Tenere presente che si tratta di una differenza rispetto all'ora di creazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="05eca-171">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="05eca-172">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-172">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05eca-173">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="05eca-173">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05eca-174">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="05eca-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="05eca-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="05eca-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05eca-176">**True** se il valore per il momento successivo utilizzerà la stessa istanza della classe e modificherà solo i valori delle proprietà, ad esempio il **valore** o il **timestamp**.</span><span class="sxs-lookup"><span data-stu-id="05eca-176">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="05eca-177">Se **true**, l'istanza viene riutilizzata.</span><span class="sxs-lookup"><span data-stu-id="05eca-177">If **True**, the instance is reused.</span></span> <span data-ttu-id="05eca-178">Se **false**, le istanze esistenti rimangono invariate e viene creata una nuova istanza per il nuovo punto nel tempo.</span><span class="sxs-lookup"><span data-stu-id="05eca-178">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="05eca-179">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="05eca-179">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05eca-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05eca-180">Requirements</span></span>



| <span data-ttu-id="05eca-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="05eca-181">Requirement</span></span> | <span data-ttu-id="05eca-182">Valore</span><span class="sxs-lookup"><span data-stu-id="05eca-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05eca-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05eca-183">Minimum supported client</span></span><br/> | <span data-ttu-id="05eca-184">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="05eca-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="05eca-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05eca-185">Minimum supported server</span></span><br/> | <span data-ttu-id="05eca-186">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="05eca-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05eca-187">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="05eca-187">Namespace</span></span><br/>                | <span data-ttu-id="05eca-188">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="05eca-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="05eca-189">MOF</span><span class="sxs-lookup"><span data-stu-id="05eca-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05eca-190"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05eca-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="05eca-191">DLL</span><span class="sxs-lookup"><span data-stu-id="05eca-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05eca-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="05eca-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

