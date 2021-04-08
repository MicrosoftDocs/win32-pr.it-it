---
title: Proprietà SystemMonitor. ShowValueBar
description: Recupera o imposta un valore che determina se la barra del valore (il set di valori statistici sotto il grafo) viene visualizzata nel controllo.
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- Proprietà ShowValueBar SysMon
- Proprietà ShowValueBar SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà ShowValueBar
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740623"
---
# <a name="systemmonitorshowvaluebar-property"></a><span data-ttu-id="6b8d0-106">Proprietà SystemMonitor. ShowValueBar</span><span class="sxs-lookup"><span data-stu-id="6b8d0-106">SystemMonitor.ShowValueBar property</span></span>

<span data-ttu-id="6b8d0-107">Recupera o imposta un valore che determina se la barra del valore (il set di valori statistici sotto il grafo) viene visualizzata nel controllo.</span><span class="sxs-lookup"><span data-stu-id="6b8d0-107">Retrieves or sets a value that determines whether the value bar (the set of statistical values below the graph) is displayed on the control.</span></span>

<span data-ttu-id="6b8d0-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6b8d0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b8d0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b8d0-109">Syntax</span></span>


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6b8d0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6b8d0-110">Property value</span></span>

<span data-ttu-id="6b8d0-111">True indica che la barra dei valori è visualizzata sul controllo; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="6b8d0-111">True indicates that the value bar is displayed on the control; otherwise false.</span></span> <span data-ttu-id="6b8d0-112">Il valore predefinito di questa proprietà è True.</span><span class="sxs-lookup"><span data-stu-id="6b8d0-112">The default value for this property is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b8d0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b8d0-113">Remarks</span></span>

<span data-ttu-id="6b8d0-114">Le statistiche visualizzate includono l'ultimo valore, il valore medio e i valori minimo e massimo del contatore attualmente selezionato sull'intervallo di tempo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="6b8d0-114">The displayed statistics include the last value, the average value, and the minimum and maximum values of the currently selected counter over the displayed time interval.</span></span> <span data-ttu-id="6b8d0-115">Per selezionare i valori dei contatori da visualizzare, l'utente deve selezionare il contatore nel riquadro Legenda del controllo.</span><span class="sxs-lookup"><span data-stu-id="6b8d0-115">To select the counter values to display, the user must select the counter in the Legend pane of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8d0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b8d0-116">Requirements</span></span>



| <span data-ttu-id="6b8d0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b8d0-117">Requirement</span></span> | <span data-ttu-id="6b8d0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8d0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8d0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8d0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6b8d0-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b8d0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6b8d0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8d0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6b8d0-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b8d0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b8d0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6b8d0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b8d0-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6b8d0-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b8d0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b8d0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8d0-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="6b8d0-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





