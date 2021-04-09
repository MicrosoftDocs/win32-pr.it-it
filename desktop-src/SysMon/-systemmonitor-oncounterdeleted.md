---
title: Evento SystemMonitor. OnCounterDeleted
description: Notifica all'utente prima dell'eliminazione di un contatore dalla raccolta dei contatori.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- Evento OnCounterDeleted SysMon
- Evento OnCounterDeleted SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento OnCounterDeleted
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964273"
---
# <a name="systemmonitoroncounterdeleted-event"></a><span data-ttu-id="793a1-106">Evento SystemMonitor. OnCounterDeleted</span><span class="sxs-lookup"><span data-stu-id="793a1-106">SystemMonitor.OnCounterDeleted event</span></span>

<span data-ttu-id="793a1-107">Notifica all'utente prima dell'eliminazione di un contatore dalla raccolta dei [**contatori**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="793a1-107">Notifies you before a counter is deleted from the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="793a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="793a1-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="793a1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="793a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="793a1-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="793a1-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="793a1-111">Indice del contatore da eliminare dall'oggetto raccolta dei [**contatori**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="793a1-111">Index of the counter to be deleted from the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="793a1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="793a1-112">Return value</span></span>

<span data-ttu-id="793a1-113">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="793a1-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="793a1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="793a1-114">Requirements</span></span>



| <span data-ttu-id="793a1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="793a1-115">Requirement</span></span> | <span data-ttu-id="793a1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="793a1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="793a1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="793a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="793a1-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="793a1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="793a1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="793a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="793a1-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="793a1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="793a1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="793a1-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="793a1-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="793a1-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="793a1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="793a1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="793a1-124">**SystemMonitor. OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="793a1-124">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="793a1-125">**SystemMonitor. OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="793a1-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





