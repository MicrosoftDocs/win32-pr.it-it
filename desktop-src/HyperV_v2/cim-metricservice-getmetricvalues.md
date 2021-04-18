---
description: Fornisce la possibilità di restituire un elenco filtrato di \_ istanze di BASEMETRICVALUE CIM.
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: Metodo GetMetricValues della classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3c84ae9f5128edecfd3dd4cb591f811fdbd86010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312922"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a><span data-ttu-id="ed672-103">Metodo GetMetricValues della classe CIM \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="ed672-103">GetMetricValues method of the CIM\_MetricService class</span></span>

<span data-ttu-id="ed672-104">Fornisce la possibilità di restituire un elenco filtrato di istanze di [**\_ BaseMetricValue CIM**](cim-basemetricvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="ed672-104">Provides the ability to return a filtered list of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed672-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed672-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="ed672-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed672-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed672-107">*Definizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ed672-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed672-108">Identifica un [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) per cui verranno restituite le metriche.</span><span class="sxs-lookup"><span data-stu-id="ed672-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="ed672-109">*Intervallo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed672-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed672-110">Identifica la modalità di selezione delle istanze.</span><span class="sxs-lookup"><span data-stu-id="ed672-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="ed672-111">L'algoritmo per l'ordinamento delle istanze di valore è specifico della definizione metrica.</span><span class="sxs-lookup"><span data-stu-id="ed672-111">The algorithm for ordering value instances is metric-definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="ed672-112">**Minimo** (2)</span><span class="sxs-lookup"><span data-stu-id="ed672-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="ed672-113">**Massimo** (3)</span><span class="sxs-lookup"><span data-stu-id="ed672-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ed672-114">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="ed672-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="ed672-115">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ed672-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ed672-116">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ed672-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed672-117">Identifica il numero massimo di istanze che devono essere restituite dal metodo.</span><span class="sxs-lookup"><span data-stu-id="ed672-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="ed672-118">*Valori* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ed672-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed672-119">Al completamento del metodo, contiene riferimenti a istanze di [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md), filtrate in base ai valori dei parametri di input.</span><span class="sxs-lookup"><span data-stu-id="ed672-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed672-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed672-120">Return value</span></span>

<span data-ttu-id="ed672-121">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ed672-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ed672-122">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="ed672-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ed672-123">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ed672-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ed672-124">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="ed672-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ed672-125">**Metodo riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="ed672-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ed672-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ed672-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ed672-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed672-127">Requirements</span></span>



| <span data-ttu-id="ed672-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed672-128">Requirement</span></span> | <span data-ttu-id="ed672-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ed672-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed672-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed672-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ed672-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ed672-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ed672-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed672-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ed672-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ed672-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ed672-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed672-134">Namespace</span></span><br/>                | <span data-ttu-id="ed672-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ed672-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ed672-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ed672-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed672-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed672-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed672-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ed672-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed672-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ed672-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ed672-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed672-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed672-141">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ed672-141">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




