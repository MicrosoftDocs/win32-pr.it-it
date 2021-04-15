---
title: Proprietà SystemMonitor. MinimumScale
description: Recupera o imposta il valore minimo dell'asse verticale (Y) del grafico.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- Proprietà MinimumScale SysMon
- Proprietà MinimumScale SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà MinimumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476576"
---
# <a name="systemmonitorminimumscale-property"></a><span data-ttu-id="29de8-106">Proprietà SystemMonitor. MinimumScale</span><span class="sxs-lookup"><span data-stu-id="29de8-106">SystemMonitor.MinimumScale property</span></span>

<span data-ttu-id="29de8-107">Recupera o imposta il valore minimo dell'asse verticale (Y) del grafico.</span><span class="sxs-lookup"><span data-stu-id="29de8-107">Retrieves or sets the minimum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="29de8-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="29de8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="29de8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29de8-109">Syntax</span></span>


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="29de8-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="29de8-110">Property value</span></span>

<span data-ttu-id="29de8-111">Valore minimo positivo dell'asse verticale del grafico.</span><span class="sxs-lookup"><span data-stu-id="29de8-111">Positive minimum value of the vertical axis of the graph.</span></span> <span data-ttu-id="29de8-112">Il valore minimo predefinito della scala verticale è 0.</span><span class="sxs-lookup"><span data-stu-id="29de8-112">The default minimum value of the vertical scale is 0.</span></span> <span data-ttu-id="29de8-113">Il valore massimo in cui è possibile impostare il valore minimo è uno minore del valore [**MaximumScale**](systemmonitor-maximumscale.md) .</span><span class="sxs-lookup"><span data-stu-id="29de8-113">The highest value that you can set the minimum value to is one less than [**MaximumScale**](systemmonitor-maximumscale.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29de8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="29de8-114">Remarks</span></span>

<span data-ttu-id="29de8-115">Il controllo regola automaticamente la posizione dei numeri di scala visualizzati sulla scala verticale in base alle dimensioni del controllo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="29de8-115">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="29de8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29de8-116">Requirements</span></span>



| <span data-ttu-id="29de8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="29de8-117">Requirement</span></span> | <span data-ttu-id="29de8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="29de8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29de8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29de8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="29de8-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="29de8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="29de8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29de8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="29de8-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="29de8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29de8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="29de8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29de8-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="29de8-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29de8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29de8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29de8-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="29de8-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="29de8-127">**SystemMonitor. MaximumScale**</span><span class="sxs-lookup"><span data-stu-id="29de8-127">**SystemMonitor.MaximumScale**</span></span>](systemmonitor-maximumscale.md)
</dt> <dt>

[<span data-ttu-id="29de8-128">**SystemMonitor. ShowScaleLabels**</span><span class="sxs-lookup"><span data-stu-id="29de8-128">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





