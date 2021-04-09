---
title: Proprietà SystemMonitor. UpdateInterval
description: Recupera o imposta il periodo di attesa di SYSMON prima della successiva raccolta dei dati del contatore e l'aggiornamento del grafico o del report.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Proprietà UpdateInterval SysMon
- Proprietà UpdateInterval SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà UpdateInterval
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964143"
---
# <a name="systemmonitorupdateinterval-property"></a><span data-ttu-id="6ee56-106">Proprietà SystemMonitor. UpdateInterval</span><span class="sxs-lookup"><span data-stu-id="6ee56-106">SystemMonitor.UpdateInterval property</span></span>

<span data-ttu-id="6ee56-107">Recupera o imposta il periodo di attesa di SYSMON prima della successiva raccolta dei dati del contatore e l'aggiornamento del grafico o del report.</span><span class="sxs-lookup"><span data-stu-id="6ee56-107">Retrieves or sets the length of time that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span>

<span data-ttu-id="6ee56-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6ee56-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee56-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ee56-109">Syntax</span></span>


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a><span data-ttu-id="6ee56-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6ee56-110">Property value</span></span>

<span data-ttu-id="6ee56-111">Tempo di attesa, in secondi, di SYSMON prima della successiva raccolta dei dati del contatore e aggiornamento del grafico o del report.</span><span class="sxs-lookup"><span data-stu-id="6ee56-111">Length of time, in seconds, that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span> <span data-ttu-id="6ee56-112">L'intervallo minimo è di 1 secondo (questo è anche il valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="6ee56-112">The minimum interval is 1 second (this is also the default value).</span></span> <span data-ttu-id="6ee56-113">Il valore massimo è 1 milione.</span><span class="sxs-lookup"><span data-stu-id="6ee56-113">The maximum value is 1,000,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ee56-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ee56-114">Remarks</span></span>

<span data-ttu-id="6ee56-115">Questa proprietà è pertinente solo quando [**SystemMonitor. ManualUpdate**](systemmonitor-manualupdate.md) è impostato su false.</span><span class="sxs-lookup"><span data-stu-id="6ee56-115">This property is relevant only when [**SystemMonitor.ManualUpdate**](systemmonitor-manualupdate.md) is set to False.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ee56-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ee56-116">Requirements</span></span>



| <span data-ttu-id="6ee56-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ee56-117">Requirement</span></span> | <span data-ttu-id="6ee56-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6ee56-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee56-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ee56-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee56-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ee56-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6ee56-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ee56-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee56-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ee56-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ee56-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6ee56-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ee56-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6ee56-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ee56-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ee56-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee56-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="6ee56-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





