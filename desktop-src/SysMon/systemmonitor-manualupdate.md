---
title: Proprietà SystemMonitor. ManualUpdate
description: Recupera o imposta un valore che indica se il contenuto del monitor di sistema verrà aggiornato manualmente o automaticamente a intervalli specificati.
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- Proprietà ManualUpdate SysMon
- Proprietà ManualUpdate SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà ManualUpdate
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301576"
---
# <a name="systemmonitormanualupdate-property"></a><span data-ttu-id="f7612-106">Proprietà SystemMonitor. ManualUpdate</span><span class="sxs-lookup"><span data-stu-id="f7612-106">SystemMonitor.ManualUpdate property</span></span>

<span data-ttu-id="f7612-107">Recupera o imposta un valore che indica se il contenuto del monitor di sistema verrà aggiornato manualmente o automaticamente a intervalli specificati.</span><span class="sxs-lookup"><span data-stu-id="f7612-107">Retrieves or sets a value indicating whether the contents of the System Monitor will be updated manually, or automatically at specified intervals.</span></span>

<span data-ttu-id="f7612-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f7612-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7612-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7612-109">Syntax</span></span>


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="f7612-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f7612-110">Property value</span></span>

<span data-ttu-id="f7612-111">True indica che il grafo è stato aggiornato manualmente.</span><span class="sxs-lookup"><span data-stu-id="f7612-111">True indicates that graph is updated manually.</span></span> <span data-ttu-id="f7612-112">False indica che il grafico viene aggiornato automaticamente in base all'intervallo di aggiornamento specificato in [**SystemMonitor. UpdateInterval**](systemmonitor-updateinterval.md).</span><span class="sxs-lookup"><span data-stu-id="f7612-112">False indicates that the graph is updated automatically based on the update interval specified in [**SystemMonitor.UpdateInterval**](systemmonitor-updateinterval.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7612-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7612-113">Remarks</span></span>

<span data-ttu-id="f7612-114">Per impostazione predefinita, il grafico viene aggiornato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f7612-114">By default, the graph is updated automatically.</span></span>

<span data-ttu-id="f7612-115">Per aggiornare il grafo manualmente, chiamare il metodo [**SystemMonitor. CollectSample**](systemmonitor-collectsample.md) .</span><span class="sxs-lookup"><span data-stu-id="f7612-115">To update the graph manually, call the [**SystemMonitor.CollectSample**](systemmonitor-collectsample.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7612-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7612-116">Requirements</span></span>



| <span data-ttu-id="f7612-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7612-117">Requirement</span></span> | <span data-ttu-id="f7612-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f7612-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7612-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7612-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f7612-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7612-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f7612-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7612-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f7612-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7612-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7612-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f7612-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7612-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f7612-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7612-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7612-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7612-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="f7612-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="f7612-127">**SystemMonitor. CollectSample**</span><span class="sxs-lookup"><span data-stu-id="f7612-127">**SystemMonitor.CollectSample**</span></span>](systemmonitor-collectsample.md)
</dt> <dt>

[<span data-ttu-id="f7612-128">**SystemMonitor. UpdateGraph**</span><span class="sxs-lookup"><span data-stu-id="f7612-128">**SystemMonitor.UpdateGraph**</span></span>](systemmonitor-updategraph.md)
</dt> </dl>

 

 





