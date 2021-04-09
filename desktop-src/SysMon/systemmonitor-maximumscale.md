---
title: Proprietà SystemMonitor. MaximumScale
description: Recupera o imposta il valore massimo dell'asse verticale (Y) del grafico.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- Proprietà MaximumScale SysMon
- Proprietà MaximumScale SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà MaximumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37740802fac4d89bbcbe9d5c105e357b55ab481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964087"
---
# <a name="systemmonitormaximumscale-property"></a><span data-ttu-id="772a0-106">Proprietà SystemMonitor. MaximumScale</span><span class="sxs-lookup"><span data-stu-id="772a0-106">SystemMonitor.MaximumScale property</span></span>

<span data-ttu-id="772a0-107">Recupera o imposta il valore massimo dell'asse verticale (Y) del grafico.</span><span class="sxs-lookup"><span data-stu-id="772a0-107">Retrieves or sets the maximum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="772a0-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="772a0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="772a0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="772a0-109">Syntax</span></span>


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="772a0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="772a0-110">Property value</span></span>

<span data-ttu-id="772a0-111">Valore massimo positivo dell'asse verticale del grafico.</span><span class="sxs-lookup"><span data-stu-id="772a0-111">Positive maximum value of the vertical axis of the graph.</span></span> <span data-ttu-id="772a0-112">Il valore massimo predefinito della scala verticale è 100.</span><span class="sxs-lookup"><span data-stu-id="772a0-112">The default maximum value of the vertical scale is 100.</span></span> <span data-ttu-id="772a0-113">Il valore minimo in cui è possibile impostare il valore massimo è uno più del valore [**MinimumScale**](systemmonitor-minimumscale.md) .</span><span class="sxs-lookup"><span data-stu-id="772a0-113">The lowest value that you can set the maximum value to is one more than the [**MinimumScale**](systemmonitor-minimumscale.md) value.</span></span> <span data-ttu-id="772a0-114">Il valore massimo su cui è possibile impostare il valore massimo è 999.999.999.</span><span class="sxs-lookup"><span data-stu-id="772a0-114">The highest value that you can set the maximum value to is 999,999,999.</span></span>

## <a name="remarks"></a><span data-ttu-id="772a0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="772a0-115">Remarks</span></span>

<span data-ttu-id="772a0-116">Il controllo regola automaticamente la posizione dei numeri di scala visualizzati sulla scala verticale in base alle dimensioni del controllo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="772a0-116">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="772a0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="772a0-117">Requirements</span></span>



| <span data-ttu-id="772a0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="772a0-118">Requirement</span></span> | <span data-ttu-id="772a0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="772a0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="772a0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="772a0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="772a0-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="772a0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="772a0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="772a0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="772a0-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="772a0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="772a0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="772a0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="772a0-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="772a0-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="772a0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="772a0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772a0-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="772a0-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="772a0-128">**SystemMonitor. MinimumScale**</span><span class="sxs-lookup"><span data-stu-id="772a0-128">**SystemMonitor.MinimumScale**</span></span>](systemmonitor-minimumscale.md)
</dt> <dt>

[<span data-ttu-id="772a0-129">**SystemMonitor. ShowScaleLabels**</span><span class="sxs-lookup"><span data-stu-id="772a0-129">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





