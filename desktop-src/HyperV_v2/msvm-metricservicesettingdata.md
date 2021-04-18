---
description: Rappresenta le impostazioni per il servizio metrico. Non è possibile modificare direttamente le proprietà di questa classe. Il client deve chiamare il metodo ModifyServiceSettings per modificare una di queste proprietà.
ms.assetid: 578ddda7-4c8e-498e-8612-29c392390b73
title: Classe Msvm_MetricServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceSettingData
- Msvm_MetricServiceSettingData.InstanceID
- Msvm_MetricServiceSettingData.Caption
- Msvm_MetricServiceSettingData.Description
- Msvm_MetricServiceSettingData.ElementName
- Msvm_MetricServiceSettingData.MetricsFlushInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a1211b19692761dd8b92de69cf42e4ad55246f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310012"
---
# <a name="msvm_metricservicesettingdata-class"></a><span data-ttu-id="94ac4-105">\_Classe MSVM MetricServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="94ac4-105">Msvm\_MetricServiceSettingData class</span></span>

<span data-ttu-id="94ac4-106">Rappresenta le impostazioni per il servizio metrico.</span><span class="sxs-lookup"><span data-stu-id="94ac4-106">Represents the settings for the metric service.</span></span> <span data-ttu-id="94ac4-107">Non è possibile modificare direttamente le proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="94ac4-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="94ac4-108">Il client deve chiamare il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) per modificare una di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="94ac4-108">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="94ac4-109">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="94ac4-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94ac4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94ac4-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service Settings";
  string   Description = "Defines Hyper-V Metric Service Settings";
  string   ElementName = "Hyper-V Metric Service Settings";
  datetime MetricsFlushInterval;
};
```

## <a name="members"></a><span data-ttu-id="94ac4-111">Members</span><span class="sxs-lookup"><span data-stu-id="94ac4-111">Members</span></span>

<span data-ttu-id="94ac4-112">La **classe \_ MetricServiceSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="94ac4-112">The **Msvm\_MetricServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="94ac4-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94ac4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94ac4-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94ac4-114">Properties</span></span>

<span data-ttu-id="94ac4-115">La **classe \_ MetricServiceSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="94ac4-115">The **Msvm\_MetricServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94ac4-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="94ac4-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ac4-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94ac4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94ac4-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94ac4-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94ac4-119">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94ac4-119">A short description of the object.</span></span> <span data-ttu-id="94ac4-120">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "impostazioni del servizio metrica Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="94ac4-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="94ac4-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="94ac4-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ac4-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94ac4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94ac4-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94ac4-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94ac4-124">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="94ac4-124">A description of the object.</span></span> <span data-ttu-id="94ac4-125">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "definisce le impostazioni del servizio metrica Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="94ac4-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="94ac4-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="94ac4-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ac4-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94ac4-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94ac4-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94ac4-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94ac4-129">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94ac4-129">A display name for the object.</span></span> <span data-ttu-id="94ac4-130">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "impostazioni del servizio metrica Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="94ac4-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="94ac4-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="94ac4-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ac4-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="94ac4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94ac4-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94ac4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94ac4-134">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="94ac4-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="94ac4-135">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="94ac4-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="94ac4-136">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94ac4-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="94ac4-137">**MetricsFlushInterval**</span><span class="sxs-lookup"><span data-stu-id="94ac4-137">**MetricsFlushInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ac4-138">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94ac4-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94ac4-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="94ac4-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94ac4-140">Definisce l'intervallo in corrispondenza del quale le metriche devono essere scaricate su disco.</span><span class="sxs-lookup"><span data-stu-id="94ac4-140">Defines the interval at which metrics should be flushed to disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94ac4-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94ac4-141">Requirements</span></span>



| <span data-ttu-id="94ac4-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="94ac4-142">Requirement</span></span> | <span data-ttu-id="94ac4-143">Valore</span><span class="sxs-lookup"><span data-stu-id="94ac4-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94ac4-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94ac4-144">Minimum supported client</span></span><br/> | <span data-ttu-id="94ac4-145">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="94ac4-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="94ac4-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94ac4-146">Minimum supported server</span></span><br/> | <span data-ttu-id="94ac4-147">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="94ac4-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94ac4-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="94ac4-148">Namespace</span></span><br/>                | <span data-ttu-id="94ac4-149">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="94ac4-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="94ac4-150">MOF</span><span class="sxs-lookup"><span data-stu-id="94ac4-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94ac4-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94ac4-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94ac4-152">DLL</span><span class="sxs-lookup"><span data-stu-id="94ac4-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94ac4-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94ac4-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94ac4-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94ac4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ac4-155">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="94ac4-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="94ac4-156">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="94ac4-156">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md)
</dt> </dl>

 

