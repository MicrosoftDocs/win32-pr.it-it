---
title: SystemMonitor. ScaleToFit, metodo
description: Ridimensionare i valori dei contatori per adattarli al grafico.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Metodo ScaleToFit SysMon
- Metodo ScaleToFit SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo ScaleToFit
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741111"
---
# <a name="systemmonitorscaletofit-method"></a><span data-ttu-id="58cc7-106">SystemMonitor. ScaleToFit, metodo</span><span class="sxs-lookup"><span data-stu-id="58cc7-106">SystemMonitor.ScaleToFit method</span></span>

<span data-ttu-id="58cc7-107">Ridimensionare i valori dei contatori per adattarli al grafico.</span><span class="sxs-lookup"><span data-stu-id="58cc7-107">Scale counter values to fit in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="58cc7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58cc7-108">Syntax</span></span>


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a><span data-ttu-id="58cc7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="58cc7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58cc7-110">*selectedCountersOnly* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58cc7-110">*selectedCountersOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58cc7-111">True per ridimensionare solo i contatori selezionati; in caso contrario, false per ridimensionare tutti i contatori.</span><span class="sxs-lookup"><span data-stu-id="58cc7-111">True to scale only the selected counters; otherwise, false to scale all counters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58cc7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58cc7-112">Return value</span></span>

<span data-ttu-id="58cc7-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="58cc7-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58cc7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="58cc7-114">Remarks</span></span>

<span data-ttu-id="58cc7-115">Questo metodo cancellerà la visualizzazione grafico.</span><span class="sxs-lookup"><span data-stu-id="58cc7-115">This method will clear the graph view.</span></span> <span data-ttu-id="58cc7-116">SYSMON usa quindi il fattore di scala specificato per ogni contatore per ridisegnare il grafico se l'origine dati è un file di log oppure iniziare a rappresentare i nuovi valori dei contatori se l'origine dati è un'attività in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="58cc7-116">SYSMON then uses the scale factor specified for each counter to redraw the graph if the data source is a log file, or begin graphing new counter values if the data source is real time activity.</span></span>

## <a name="requirements"></a><span data-ttu-id="58cc7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58cc7-117">Requirements</span></span>



| <span data-ttu-id="58cc7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="58cc7-118">Requirement</span></span> | <span data-ttu-id="58cc7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="58cc7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58cc7-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58cc7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="58cc7-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58cc7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58cc7-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58cc7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="58cc7-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58cc7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58cc7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="58cc7-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58cc7-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="58cc7-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58cc7-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58cc7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58cc7-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="58cc7-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="58cc7-128">**CounterItem. ScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="58cc7-128">**CounterItem.ScaleFactor**</span></span>](counteritem-scalefactor.md)
</dt> <dt>

[<span data-ttu-id="58cc7-129">**CounterItem. Selected**</span><span class="sxs-lookup"><span data-stu-id="58cc7-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





