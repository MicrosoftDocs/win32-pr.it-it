---
description: Ottiene i valori della metrica.
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: Metodo GetMetricValues della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe3e32b21ec0baa497fcef781e1b48fae37fbf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318334"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="ca5b0-103">Metodo GetMetricValues della classe MSVM \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="ca5b0-103">GetMetricValues method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="ca5b0-104">Ottiene i valori della metrica.</span><span class="sxs-lookup"><span data-stu-id="ca5b0-104">Gets metric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca5b0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca5b0-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="ca5b0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca5b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca5b0-107">*Definizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ca5b0-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca5b0-108">Identifica un [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) per cui verranno restituite le metriche.</span><span class="sxs-lookup"><span data-stu-id="ca5b0-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="ca5b0-109">*Intervallo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca5b0-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca5b0-110">Identifica la modalità di selezione delle istanze.</span><span class="sxs-lookup"><span data-stu-id="ca5b0-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="ca5b0-111">L'algoritmo per l'ordinamento delle istanze di valore è specifico della definizione della metrica.</span><span class="sxs-lookup"><span data-stu-id="ca5b0-111">The algorithm for ordering value instances is metric definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="ca5b0-112">**Minimo** (2)</span><span class="sxs-lookup"><span data-stu-id="ca5b0-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="ca5b0-113">**Massimo** (3)</span><span class="sxs-lookup"><span data-stu-id="ca5b0-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ca5b0-114">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="ca5b0-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="ca5b0-115">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ca5b0-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ca5b0-116">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ca5b0-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca5b0-117">Identifica il numero massimo di istanze che devono essere restituite dal metodo.</span><span class="sxs-lookup"><span data-stu-id="ca5b0-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="ca5b0-118">*Valori* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ca5b0-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca5b0-119">Al completamento del metodo, contiene riferimenti a istanze di [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md), filtrate in base ai valori dei parametri di input.</span><span class="sxs-lookup"><span data-stu-id="ca5b0-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca5b0-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca5b0-120">Return value</span></span>

<span data-ttu-id="ca5b0-121">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca5b0-121">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ca5b0-122">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="ca5b0-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ca5b0-123">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ca5b0-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ca5b0-124">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="ca5b0-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ca5b0-125">**Metodo riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="ca5b0-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ca5b0-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ca5b0-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ca5b0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca5b0-127">Requirements</span></span>



| <span data-ttu-id="ca5b0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca5b0-128">Requirement</span></span> | <span data-ttu-id="ca5b0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ca5b0-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca5b0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca5b0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ca5b0-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ca5b0-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ca5b0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca5b0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ca5b0-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ca5b0-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ca5b0-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca5b0-134">Namespace</span></span><br/>                | <span data-ttu-id="ca5b0-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ca5b0-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ca5b0-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ca5b0-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca5b0-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca5b0-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca5b0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ca5b0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca5b0-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca5b0-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ca5b0-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca5b0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5b0-141">**\_MetricService MSVM**</span><span class="sxs-lookup"><span data-stu-id="ca5b0-141">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




