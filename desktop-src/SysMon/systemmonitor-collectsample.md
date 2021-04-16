---
title: Metodo SystemMonitor CollectSample
description: Campiona un valore per ogni contatore nell'oggetto contatori.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Metodo CollectSample SysMon
- Metodo CollectSample SysMon, interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon, metodo CollectSample
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477098"
---
# <a name="systemmonitorcollectsample-method"></a><span data-ttu-id="aecdf-106">Metodo SystemMonitor:: CollectSample</span><span class="sxs-lookup"><span data-stu-id="aecdf-106">SystemMonitor::CollectSample method</span></span>

<span data-ttu-id="aecdf-107">Campiona un valore per ogni contatore nell'oggetto [**contatori**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="aecdf-107">Samples a value for each counter in the [**Counters**](counters.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aecdf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aecdf-108">Syntax</span></span>


```VB
Sub CollectSample()
```



## <a name="parameters"></a><span data-ttu-id="aecdf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="aecdf-109">Parameters</span></span>

<span data-ttu-id="aecdf-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="aecdf-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aecdf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aecdf-111">Return value</span></span>

<span data-ttu-id="aecdf-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="aecdf-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aecdf-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="aecdf-113">Remarks</span></span>

<span data-ttu-id="aecdf-114">Chiamare **CollectSample** solo se [**ManualUpdate**](systemmonitor-manualupdate.md) è true e i valori del contatore di campionamento dall'attività corrente del computer non utilizzano questo metodo durante il campionamento da un file di log.</span><span class="sxs-lookup"><span data-stu-id="aecdf-114">Call **CollectSample** only if [**ManualUpdate**](systemmonitor-manualupdate.md) is True and you are sampling counter values from the current activity of the computer do not use this method when sampling from a log file.</span></span> <span data-ttu-id="aecdf-115">Il grafico o il report viene aggiornato con il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="aecdf-115">The graph or report is updated with the new value.</span></span> <span data-ttu-id="aecdf-116">Si noti che alcuni tipi di grafici richiedono due esempi per rappresentare i dati, ad esempio il grafico a linee.</span><span class="sxs-lookup"><span data-stu-id="aecdf-116">Note that some types of graphs need two samples in order to graph the data, for example, the line graph.</span></span>

<span data-ttu-id="aecdf-117">Per ricevere una notifica quando l'esempio è stato raccolto, implementare l'evento [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) .</span><span class="sxs-lookup"><span data-stu-id="aecdf-117">To receive notification when the sample has been collected, implement the [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="aecdf-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aecdf-118">Requirements</span></span>



| <span data-ttu-id="aecdf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aecdf-119">Requirement</span></span> | <span data-ttu-id="aecdf-120">Valore</span><span class="sxs-lookup"><span data-stu-id="aecdf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aecdf-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aecdf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aecdf-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aecdf-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="aecdf-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aecdf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aecdf-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aecdf-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aecdf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="aecdf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aecdf-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="aecdf-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aecdf-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aecdf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aecdf-128">**Contatori**</span><span class="sxs-lookup"><span data-stu-id="aecdf-128">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="aecdf-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="aecdf-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





