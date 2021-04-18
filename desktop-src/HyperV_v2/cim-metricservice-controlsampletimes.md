---
description: Consente di specificare la raccolta di metriche temporizzate da avviare e di specificare il tempo di intervallo di campionamento preferito per la raccolta periodica di dati.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: Metodo ControlSampleTimes della classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e32d184199ff7ddc63be5d1fcfcd4ea376dad89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312921"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a><span data-ttu-id="2fb2b-103">Metodo ControlSampleTimes della classe CIM \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="2fb2b-103">ControlSampleTimes method of the CIM\_MetricService class</span></span>

<span data-ttu-id="2fb2b-104">Consente di specificare la raccolta di metriche temporizzate da avviare e di specificare il tempo di intervallo di campionamento preferito per la raccolta periodica di dati.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-104">Allows specification of the point in time metric gathering is to be started and to specify the preferred sample interval time for periodic data gathering.</span></span>

<span data-ttu-id="2fb2b-105">Ogni volta che viene avviato il campionamento per metriche aggiuntive, è possibile usare le impostazioni specificate da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-105">Whenever sampling for additional metrics is started, the settings specified by this method may be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb2b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fb2b-106">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="2fb2b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fb2b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fb2b-108">*StartSampleTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fb2b-108">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb2b-109">Temporizzazione per l'avvio del campionamento per le metriche.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-109">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="2fb2b-110">Il valore 99990101000000.000000 + 000 indicherà che il campionamento deve iniziare alla successiva sincronizzazione con l'ora completa.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-110">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="2fb2b-111">Il campionamento viene sincronizzato con l'ora intera se i secondi dall'intervallo di campionamento del modulo mezzanotte in secondi è uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-111">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2fb2b-112">*PreferredSampleInterval* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fb2b-112">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb2b-113">Tempo di intervallo di campionamento preferito.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-113">Preferred sample interval time.</span></span> <span data-ttu-id="2fb2b-114">Per ottenere metriche correlate, è consigliabile scegliere l'intervallo di campionamento in modo che l'intervallo di campionamento di esempio di 3600 modulo in secondi sia uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-114">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="2fb2b-115">È responsabilità dell'implementazione del servizio metrica CIM decidere se il tempo richiesto per l'intervallo di campionamento viene rispettato.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-115">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="2fb2b-116">Il client CIM può verificare se i provider di metriche rispettano il tempo di intervallo di campionamento richiesto recuperando le istanze di BaseMetricDefinition correlate e controllando il contenuto del [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).**Proprietà SampleInterval** .</span><span class="sxs-lookup"><span data-stu-id="2fb2b-116">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**SampleInterval** property.</span></span>

</dd> <dt>

<span data-ttu-id="2fb2b-117">*RestartGathering* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fb2b-117">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb2b-118">**True** per richiedere che la raccolta di tutte le metriche associate al servizio della metrica venga riavviata con questa chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-118">**TRUE** to request that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fb2b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fb2b-119">Return value</span></span>

<span data-ttu-id="2fb2b-120">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2fb2b-121">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="2fb2b-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2fb2b-122">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="2fb2b-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2fb2b-123">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="2fb2b-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2fb2b-124">**Metodo riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="2fb2b-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2fb2b-125">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2fb2b-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2fb2b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fb2b-126">Requirements</span></span>



| <span data-ttu-id="2fb2b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fb2b-127">Requirement</span></span> | <span data-ttu-id="2fb2b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2fb2b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb2b-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fb2b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb2b-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2fb2b-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2fb2b-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fb2b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb2b-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2fb2b-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2fb2b-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2fb2b-133">Namespace</span></span><br/>                | <span data-ttu-id="2fb2b-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2fb2b-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2fb2b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2fb2b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fb2b-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fb2b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fb2b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2fb2b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fb2b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2fb2b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2fb2b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fb2b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fb2b-140">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2fb2b-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




