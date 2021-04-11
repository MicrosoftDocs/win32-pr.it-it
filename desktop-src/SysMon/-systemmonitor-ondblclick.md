---
title: Evento SystemMonitor. OnDblClick
description: Invia una notifica quando un utente fa doppio clic sulla linea del grafico, sulla barra istogramma o sull'elemento del report con il pulsante sinistro del mouse.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- Evento OnDblClick SysMon
- Evento OnDblClick SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento OnDblClick
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119875"
---
# <a name="systemmonitorondblclick-event"></a><span data-ttu-id="fc1bd-106">Evento SystemMonitor. OnDblClick</span><span class="sxs-lookup"><span data-stu-id="fc1bd-106">SystemMonitor.OnDblClick event</span></span>

<span data-ttu-id="fc1bd-107">Invia una notifica quando un utente fa doppio clic sulla linea del grafico, sulla barra istogramma o sull'elemento del report con il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-107">Notifies you when a user double-clicks the graph line, histogram bar, or report item with the left mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc1bd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc1bd-108">Syntax</span></span>


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="fc1bd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc1bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc1bd-110">*Indice* \[ di in uscita\]</span><span class="sxs-lookup"><span data-stu-id="fc1bd-110">*index* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc1bd-111">Indice del contatore selezionato nell'oggetto raccolta dei [**contatori**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="fc1bd-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span> <span data-ttu-id="fc1bd-112">Se non è stato selezionato alcun contatore, viene restituito un valore di indice pari a 0. in caso contrario, viene restituito l'indice del contatore selezionato.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-112">An index value of 0 is returned if no counter was selected; otherwise, the index of the selected counter is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc1bd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc1bd-113">Return value</span></span>

<span data-ttu-id="fc1bd-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc1bd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc1bd-115">Remarks</span></span>

<span data-ttu-id="fc1bd-116">Quando viene generato questo evento, nel riquadro Legenda viene selezionato anche il contatore selezionato dall'utente nel grafico a linee e nell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-116">When this event is triggered, the counter that the user selected in the line graph and histogram is also selected in the Legend pane.</span></span> <span data-ttu-id="fc1bd-117">In questo modo è più semplice per l'utente del monitor di sistema verificare quale contatore è selezionato quando vengono visualizzati diversi valori dei contatori.</span><span class="sxs-lookup"><span data-stu-id="fc1bd-117">This makes it easier for the user of the System Monitor to see which counter is selected when several counter values are displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc1bd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc1bd-118">Requirements</span></span>



| <span data-ttu-id="fc1bd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc1bd-119">Requirement</span></span> | <span data-ttu-id="fc1bd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fc1bd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1bd-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc1bd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fc1bd-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fc1bd-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="fc1bd-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc1bd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fc1bd-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fc1bd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc1bd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fc1bd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc1bd-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="fc1bd-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





