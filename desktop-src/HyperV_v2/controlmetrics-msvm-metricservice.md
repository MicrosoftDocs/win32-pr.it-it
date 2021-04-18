---
description: Usato per controllare la raccolta di metriche per un elemento o elementi gestiti.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Metodo ControlMetrics della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314356"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="2a039-103">Metodo ControlMetrics della classe MSVM \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="2a039-103">ControlMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="2a039-104">Usato per controllare la raccolta di metriche per un elemento o elementi gestiti.</span><span class="sxs-lookup"><span data-stu-id="2a039-104">Used to control the collection of metrics for a managed element or elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a039-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a039-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="2a039-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a039-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a039-107">*Oggetto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a039-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a039-108">Istanza di [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che identifica gli elementi gestiti per i quali verranno raccolte le metriche.</span><span class="sxs-lookup"><span data-stu-id="2a039-108">A [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) instance that identifies the managed elements for which metrics will be collected.</span></span> <span data-ttu-id="2a039-109">Se questo parametro è **null**, verranno raccolte le metriche per tutti gli elementi gestiti associati al parametro *Definition* .</span><span class="sxs-lookup"><span data-stu-id="2a039-109">If this parameter is **Null**, the metrics for all the managed elements associated with the *Definition* parameter will be collected.</span></span>

</dd> <dt>

<span data-ttu-id="2a039-110">*Definizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2a039-110">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a039-111">Istanza di [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) che specifica le metriche che verranno raccolte.</span><span class="sxs-lookup"><span data-stu-id="2a039-111">An [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance that specifies which metrics will be collected.</span></span> <span data-ttu-id="2a039-112">Se questo parametro è **null**, vengono raccolte le metriche per tutte le definizioni associate all'elemento gestito identificato dal parametro *Subject*</span><span class="sxs-lookup"><span data-stu-id="2a039-112">If this parameter is **Null**, the metrics for all the definitions associated with the managed element identified by the *Subject* parameter will be collected</span></span>

</dd> <dt>

<span data-ttu-id="2a039-113">*MetricCollectionEnabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a039-113">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a039-114">Specifica l'operazione da eseguire sulla raccolta di metriche.</span><span class="sxs-lookup"><span data-stu-id="2a039-114">Specifies the operation to perform on the metrics collection.</span></span> <span data-ttu-id="2a039-115">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a039-115">This must be one of the following values.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="2a039-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Abilita** (2)</span><span class="sxs-lookup"><span data-stu-id="2a039-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2a039-117">Abilitare la raccolta di metriche.</span><span class="sxs-lookup"><span data-stu-id="2a039-117">Enable metrics collection.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="2a039-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disabilita** (3)</span><span class="sxs-lookup"><span data-stu-id="2a039-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2a039-119">Disabilitare la raccolta di metriche.</span><span class="sxs-lookup"><span data-stu-id="2a039-119">Disable metrics collection.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="2a039-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (4)</span><span class="sxs-lookup"><span data-stu-id="2a039-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2a039-121">Reimposta i valori delle metriche.</span><span class="sxs-lookup"><span data-stu-id="2a039-121">Reset metrics values.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2a039-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="2a039-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2a039-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2a039-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="2a039-124"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2a039-124"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="2a039-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a039-125">Return value</span></span>

<span data-ttu-id="2a039-126">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a039-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2a039-127">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="2a039-127">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2a039-128">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="2a039-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2a039-129">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="2a039-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2a039-130">**Metodo riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="2a039-130">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2a039-131">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2a039-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2a039-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a039-132">Remarks</span></span>

<span data-ttu-id="2a039-133">Questo metodo avrà esito negativo nelle istanze seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a039-133">This method will fail in the following instances:</span></span>

-   <span data-ttu-id="2a039-134">I parametri *Subject* e *Definition* sono entrambi **null**.</span><span class="sxs-lookup"><span data-stu-id="2a039-134">The *Subject* and *Definition* parameters are both **Null**.</span></span>
-   <span data-ttu-id="2a039-135">I parametri *Subject* e *Definition* sono entrambi non **null** e non è disponibile un'istanza di [**MSVM \_ MetricDefForME**](msvm-metricdefforme.md) che associ le due istanze.</span><span class="sxs-lookup"><span data-stu-id="2a039-135">The *Subject* and *Definition* parameters are both non-**Null** and there is not an instance of [**Msvm\_MetricDefForME**](msvm-metricdefforme.md) that associates the two instances.</span></span>
-   <span data-ttu-id="2a039-136">Il parametro della *definizione* è un riferimento a un'istanza di [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) che non è associata a [**MSVM \_ MetricService**](msvm-metricservice.md) tramite [**MSVM \_ ServiceAffectsElement**](msvm-serviceaffectselement.md).</span><span class="sxs-lookup"><span data-stu-id="2a039-136">The *Definition* parameter is a reference to an instance of [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) that is not associated with the [**Msvm\_MetricService**](msvm-metricservice.md) through [**Msvm\_ServiceAffectsElement**](msvm-serviceaffectselement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a039-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a039-137">Requirements</span></span>



| <span data-ttu-id="2a039-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a039-138">Requirement</span></span> | <span data-ttu-id="2a039-139">Valore</span><span class="sxs-lookup"><span data-stu-id="2a039-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a039-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a039-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2a039-141">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2a039-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2a039-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a039-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2a039-143">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2a039-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a039-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2a039-144">Namespace</span></span><br/>                | <span data-ttu-id="2a039-145">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2a039-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2a039-146">MOF</span><span class="sxs-lookup"><span data-stu-id="2a039-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a039-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a039-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a039-148">DLL</span><span class="sxs-lookup"><span data-stu-id="2a039-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a039-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a039-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2a039-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a039-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a039-151">**\_MetricService MSVM**</span><span class="sxs-lookup"><span data-stu-id="2a039-151">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

