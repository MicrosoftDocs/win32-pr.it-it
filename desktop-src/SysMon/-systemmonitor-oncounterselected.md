---
title: Evento SystemMonitor. OnCounterSelected
description: Notifica all'utente la selezione di un contatore.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- Evento OnCounterSelected SysMon
- Evento OnCounterSelected SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento OnCounterSelected
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0174ab2f896a27e44df592ec28b7cb12a03198f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301697"
---
# <a name="systemmonitoroncounterselected-event"></a><span data-ttu-id="2e0a9-106">Evento SystemMonitor. OnCounterSelected</span><span class="sxs-lookup"><span data-stu-id="2e0a9-106">SystemMonitor.OnCounterSelected event</span></span>

<span data-ttu-id="2e0a9-107">Notifica all'utente la selezione di un contatore.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-107">Notifies you when a counter is selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e0a9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e0a9-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="2e0a9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e0a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e0a9-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2e0a9-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e0a9-111">Indice del contatore selezionato nell'oggetto raccolta dei [**contatori**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="2e0a9-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e0a9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e0a9-112">Return value</span></span>

<span data-ttu-id="2e0a9-113">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2e0a9-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e0a9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e0a9-114">Remarks</span></span>

<span data-ttu-id="2e0a9-115">È possibile ricevere questo evento quando</span><span class="sxs-lookup"><span data-stu-id="2e0a9-115">You can receive this event when</span></span>

-   <span data-ttu-id="2e0a9-116">Impostare [**CounterItem. Selected**](counteritem-selected.md) su true</span><span class="sxs-lookup"><span data-stu-id="2e0a9-116">You set [**CounterItem.Selected**](counteritem-selected.md) to True</span></span>
-   <span data-ttu-id="2e0a9-117">L'utente seleziona un contatore nella legenda</span><span class="sxs-lookup"><span data-stu-id="2e0a9-117">The user selects a counter in the Legend</span></span>
-   <span data-ttu-id="2e0a9-118">L'utente fa doppio clic su un contatore nella legenda</span><span class="sxs-lookup"><span data-stu-id="2e0a9-118">The user double-clicks on a counter in the Legend</span></span>

## <a name="requirements"></a><span data-ttu-id="2e0a9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e0a9-119">Requirements</span></span>



| <span data-ttu-id="2e0a9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e0a9-120">Requirement</span></span> | <span data-ttu-id="2e0a9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2e0a9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0a9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e0a9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2e0a9-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2e0a9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2e0a9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e0a9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2e0a9-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2e0a9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e0a9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2e0a9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e0a9-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2e0a9-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e0a9-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e0a9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0a9-129">**SystemMonitor. OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="2e0a9-129">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="2e0a9-130">**SystemMonitor. OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="2e0a9-130">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





