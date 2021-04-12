---
title: Proprietà SystemMonitor. DisplayType
description: Recupera o imposta il tipo di grafico utilizzato per rappresentare i dati del contatore delle prestazioni.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- Proprietà DisplayType SysMon
- Proprietà DisplayType SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà DisplayType
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119874"
---
# <a name="systemmonitordisplaytype-property"></a><span data-ttu-id="3abea-106">Proprietà SystemMonitor. DisplayType</span><span class="sxs-lookup"><span data-stu-id="3abea-106">SystemMonitor.DisplayType property</span></span>

<span data-ttu-id="3abea-107">Recupera o imposta il tipo di grafico utilizzato per rappresentare i dati del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="3abea-107">Retrieves or sets the type of graph used to graph the performance counter data.</span></span>

<span data-ttu-id="3abea-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3abea-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3abea-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3abea-109">Syntax</span></span>


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="3abea-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3abea-110">Property value</span></span>

<span data-ttu-id="3abea-111">Tipo di grafico utilizzato per rappresentare i dati del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="3abea-111">Type of graph used to graph the performance counter data.</span></span> <span data-ttu-id="3abea-112">Per i valori possibili, vedere [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span><span class="sxs-lookup"><span data-stu-id="3abea-112">For possible values, see [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="3abea-113">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="3abea-113">Exceptions</span></span>



| <span data-ttu-id="3abea-114">Tipo di eccezione</span><span class="sxs-lookup"><span data-stu-id="3abea-114">Exception type</span></span>               | <span data-ttu-id="3abea-115">Condizione</span><span class="sxs-lookup"><span data-stu-id="3abea-115">Condition</span></span>                                         |
|------------------------------|---------------------------------------------------|
| <span data-ttu-id="3abea-116">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="3abea-116">**System.ArgumentException**</span></span> | <span data-ttu-id="3abea-117">Il valore del grafico o del report specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="3abea-117">The specified graph or report value is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3abea-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3abea-118">Requirements</span></span>



| <span data-ttu-id="3abea-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3abea-119">Requirement</span></span> | <span data-ttu-id="3abea-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3abea-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3abea-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3abea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3abea-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3abea-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3abea-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3abea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3abea-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3abea-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3abea-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3abea-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3abea-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="3abea-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3abea-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3abea-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3abea-128">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="3abea-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





