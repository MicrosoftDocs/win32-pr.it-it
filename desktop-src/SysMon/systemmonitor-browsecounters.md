---
title: Metodo SystemMonitor BrowseCounters
description: Consente di visualizzare la finestra di dialogo Aggiungi contatori.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Metodo BrowseCounters SysMon
- Metodo BrowseCounters SysMon, interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon, metodo BrowseCounters
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047820"
---
# <a name="systemmonitorbrowsecounters-method"></a><span data-ttu-id="cb92f-106">Metodo SystemMonitor:: BrowseCounters</span><span class="sxs-lookup"><span data-stu-id="cb92f-106">SystemMonitor::BrowseCounters method</span></span>

<span data-ttu-id="cb92f-107">Consente di visualizzare la finestra di dialogo **Aggiungi contatori** .</span><span class="sxs-lookup"><span data-stu-id="cb92f-107">Displays the **Add Counters** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb92f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb92f-108">Syntax</span></span>


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a><span data-ttu-id="cb92f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb92f-109">Parameters</span></span>

<span data-ttu-id="cb92f-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cb92f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb92f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb92f-111">Return value</span></span>

<span data-ttu-id="cb92f-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cb92f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb92f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb92f-113">Remarks</span></span>

<span data-ttu-id="cb92f-114">Questa finestra di dialogo consente all'utente di selezionare i contatori delle prestazioni locali o remoti da un elenco di oggetti prestazioni.</span><span class="sxs-lookup"><span data-stu-id="cb92f-114">This dialog box lets the user select local or remote performance counters from a list of performance objects.</span></span> <span data-ttu-id="cb92f-115">I contatori selezionati vengono aggiunti alla raccolta dei [**contatori**](counters.md) e visualizzati nel grafico o nel report.</span><span class="sxs-lookup"><span data-stu-id="cb92f-115">The selected counters are added to the [**Counters**](counters.md) collection and displayed in the graph or report.</span></span>

<span data-ttu-id="cb92f-116">Per ricevere una notifica quando viene aggiunto un contatore, implementare l'evento [**OnCounterAdded**](systemmonitor-oncounteradded.md) .</span><span class="sxs-lookup"><span data-stu-id="cb92f-116">To receive notification when a counter is added, implement the [**OnCounterAdded**](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb92f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb92f-117">Requirements</span></span>



| <span data-ttu-id="cb92f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb92f-118">Requirement</span></span> | <span data-ttu-id="cb92f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="cb92f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb92f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb92f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cb92f-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cb92f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cb92f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb92f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cb92f-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cb92f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb92f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cb92f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb92f-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cb92f-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb92f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb92f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb92f-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="cb92f-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="cb92f-128">**Contatori. Aggiungi**</span><span class="sxs-lookup"><span data-stu-id="cb92f-128">**Counters.Add**</span></span>](counters-add.md)
</dt> </dl>

 

 





