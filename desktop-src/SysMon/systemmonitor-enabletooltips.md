---
title: Proprietà SystemMonitor. EnableToolTips
description: Recupera o imposta un valore che determina se viene visualizzata una descrizione comandi quando il puntatore del mouse viene posizionato su un contatore in una delle visualizzazioni del grafico (non supportato per la visualizzazione report).
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- Proprietà EnableToolTips SysMon
- Proprietà EnableToolTips SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà EnableToolTips
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301695"
---
# <a name="systemmonitorenabletooltips-property"></a><span data-ttu-id="63eb0-106">Proprietà SystemMonitor. EnableToolTips</span><span class="sxs-lookup"><span data-stu-id="63eb0-106">SystemMonitor.EnableToolTips property</span></span>

<span data-ttu-id="63eb0-107">Recupera o imposta un valore che determina se viene visualizzata una descrizione comandi quando il puntatore del mouse viene posizionato su un contatore in una delle visualizzazioni del grafico (non supportato per la visualizzazione report).</span><span class="sxs-lookup"><span data-stu-id="63eb0-107">Retrieves or sets a value that determines if a tool tip is shown when the mouse hovers over a counter in one of the graph views (not supported for report view).</span></span>

## <a name="syntax"></a><span data-ttu-id="63eb0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63eb0-108">Syntax</span></span>


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a><span data-ttu-id="63eb0-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="63eb0-109">Property value</span></span>

<span data-ttu-id="63eb0-110">True Visualizza una descrizione comando contenente le informazioni sul contatore; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="63eb0-110">True displays a tool tip with the counter information in it; otherwise, False.</span></span>

## <a name="remarks"></a><span data-ttu-id="63eb0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="63eb0-111">Remarks</span></span>

<span data-ttu-id="63eb0-112">Per i grafici a linee, la descrizione comando è ancorata al punto dati più vicino al mouse.</span><span class="sxs-lookup"><span data-stu-id="63eb0-112">For line graphs, the tool tip is anchored to the data point that is closest to the mouse.</span></span> <span data-ttu-id="63eb0-113">Per i grafici a barre e gli istogrammi, la descrizione comando rappresenta il valore totale dei dati della barra, non un punto all'interno della barra.</span><span class="sxs-lookup"><span data-stu-id="63eb0-113">For bar charts and histograms, the tool tip represents the total data value of the bar, not a point within the bar.</span></span>

<span data-ttu-id="63eb0-114">La descrizione comando contiene informazioni diverse in base all'origine dati.</span><span class="sxs-lookup"><span data-stu-id="63eb0-114">The tool tip contains different information based upon the data source.</span></span> <span data-ttu-id="63eb0-115">Per i file di log, la descrizione comando contiene il percorso del contatore, il valore del contatore, il timestamp, il numero di campioni di dati inclusi nel punto dati e i valori di dati minimo e massimo.</span><span class="sxs-lookup"><span data-stu-id="63eb0-115">For log files, the tool tip contains the counter path, counter value, time stamp, number of data samples included in the data point, and the minimum and maximum data values.</span></span>

<span data-ttu-id="63eb0-116">Per l'attività in tempo reale, la descrizione comando contiene il percorso del contatore, il valore del contatore e il timestamp.</span><span class="sxs-lookup"><span data-stu-id="63eb0-116">For real time activity, the tool tip contains the counter path, counter value, and time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="63eb0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63eb0-117">Requirements</span></span>



| <span data-ttu-id="63eb0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="63eb0-118">Requirement</span></span> | <span data-ttu-id="63eb0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="63eb0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63eb0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63eb0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="63eb0-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63eb0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63eb0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63eb0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="63eb0-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63eb0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63eb0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="63eb0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63eb0-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="63eb0-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





