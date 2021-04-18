---
title: Proprietà SystemMonitor. ShowTimeAxisLabels
description: Recupera o imposta un valore che determina se l'asse orizzontale (X) della visualizzazione grafico contiene etichette.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- Proprietà ShowTimeAxisLabels SysMon
- Proprietà ShowTimeAxisLabels SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà ShowTimeAxisLabels
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301254"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a><span data-ttu-id="5f25e-106">Proprietà SystemMonitor. ShowTimeAxisLabels</span><span class="sxs-lookup"><span data-stu-id="5f25e-106">SystemMonitor.ShowTimeAxisLabels property</span></span>

<span data-ttu-id="5f25e-107">Recupera o imposta un valore che determina se l'asse orizzontale (X) della visualizzazione grafico contiene etichette.</span><span class="sxs-lookup"><span data-stu-id="5f25e-107">Retrieves or sets a value that determines if the horizontal (X) axis of the graph view contains labels.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f25e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f25e-108">Syntax</span></span>


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a><span data-ttu-id="5f25e-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5f25e-109">Property value</span></span>

<span data-ttu-id="5f25e-110">Se il valore è true, le etichette verranno applicate all'asse x.</span><span class="sxs-lookup"><span data-stu-id="5f25e-110">A value of True will apply labels to the x-axis.</span></span> <span data-ttu-id="5f25e-111">Il valore false non lo è.</span><span class="sxs-lookup"><span data-stu-id="5f25e-111">A value of False will not.</span></span> <span data-ttu-id="5f25e-112">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="5f25e-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f25e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f25e-113">Remarks</span></span>

<span data-ttu-id="5f25e-114">SYSMON ignora questa proprietà per grafici a barre, report e istogrammi.</span><span class="sxs-lookup"><span data-stu-id="5f25e-114">SYSMON ignores this property for bar graphs, reports and histograms.</span></span>

<span data-ttu-id="5f25e-115">Per i grafici a linee, SYSMON usa l'ora in cui è stato campionato il valore del contatore come etichetta.</span><span class="sxs-lookup"><span data-stu-id="5f25e-115">For line graphs, SYSMON uses the time that the counter value was sampled as the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f25e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f25e-116">Requirements</span></span>



| <span data-ttu-id="5f25e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f25e-117">Requirement</span></span> | <span data-ttu-id="5f25e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5f25e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f25e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f25e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f25e-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f25e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f25e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f25e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f25e-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f25e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f25e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5f25e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f25e-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5f25e-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





