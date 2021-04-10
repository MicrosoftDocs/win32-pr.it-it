---
description: Imposta i tempi di campionamento del controllo.
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Metodo ControlSampleTimes della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1bb3797523153592610714406306035f59fc844c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227420"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="55056-103">Metodo ControlSampleTimes della classe MSVM \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="55056-103">ControlSampleTimes method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="55056-104">Imposta i tempi di campionamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="55056-104">Sets the control sample times.</span></span>

## <a name="syntax"></a><span data-ttu-id="55056-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55056-105">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="55056-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="55056-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55056-107">*StartSampleTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55056-107">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55056-108">Temporizzazione per l'avvio del campionamento per le metriche.</span><span class="sxs-lookup"><span data-stu-id="55056-108">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="55056-109">Il valore 99990101000000.000000 + 000 indicherà che il campionamento deve iniziare alla successiva sincronizzazione con l'ora completa.</span><span class="sxs-lookup"><span data-stu-id="55056-109">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="55056-110">Il campionamento viene sincronizzato con l'ora intera se i secondi dall'intervallo di campionamento del modulo mezzanotte in secondi è uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="55056-110">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="55056-111">*PreferredSampleInterval* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55056-111">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55056-112">Tempo di intervallo di campionamento preferito.</span><span class="sxs-lookup"><span data-stu-id="55056-112">Preferred sample interval time.</span></span> <span data-ttu-id="55056-113">Per ottenere metriche correlate, è consigliabile scegliere l'intervallo di campionamento in modo che l'intervallo di campionamento di esempio di 3600 modulo in secondi sia uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="55056-113">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="55056-114">È responsabilità dell'implementazione del servizio metrica CIM decidere se il tempo richiesto per l'intervallo di campionamento viene rispettato.</span><span class="sxs-lookup"><span data-stu-id="55056-114">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="55056-115">Il client CIM può verificare se i provider di metriche rispettano il tempo di intervallo di campionamento richiesto recuperando le istanze di BaseMetricDefinition correlate e controllando il contenuto della \_ Proprietà "CIM BaseMetricDefinition. SampleInterval".</span><span class="sxs-lookup"><span data-stu-id="55056-115">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the "CIM\_BaseMetricDefinition.SampleInterval" property.</span></span>

</dd> <dt>

<span data-ttu-id="55056-116">*RestartGathering* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55056-116">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55056-117">Valore booleano che, se impostato su TRUE, richiede che la raccolta di tutte le metriche associate al servizio della metrica venga riavviata con questa chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="55056-117">Boolean that when set to TRUE requests that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55056-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55056-118">Return value</span></span>

<span data-ttu-id="55056-119">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="55056-119">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="55056-120">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="55056-120">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="55056-121">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="55056-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="55056-122">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="55056-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="55056-123">**Metodo riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="55056-123">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="55056-124">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="55056-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="55056-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55056-125">Requirements</span></span>



| <span data-ttu-id="55056-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="55056-126">Requirement</span></span> | <span data-ttu-id="55056-127">Valore</span><span class="sxs-lookup"><span data-stu-id="55056-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55056-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55056-128">Minimum supported client</span></span><br/> | <span data-ttu-id="55056-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="55056-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="55056-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55056-130">Minimum supported server</span></span><br/> | <span data-ttu-id="55056-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="55056-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="55056-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="55056-132">Namespace</span></span><br/>                | <span data-ttu-id="55056-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="55056-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="55056-134">MOF</span><span class="sxs-lookup"><span data-stu-id="55056-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55056-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55056-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="55056-136">DLL</span><span class="sxs-lookup"><span data-stu-id="55056-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55056-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="55056-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="55056-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55056-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55056-139">**\_MetricService MSVM**</span><span class="sxs-lookup"><span data-stu-id="55056-139">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




