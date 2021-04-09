---
title: Proprietà SystemMonitor. ChartScroll
description: Recupera o imposta un valore che determina se il grafico a linee scorre nella visualizzazione.
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Proprietà ChartScroll SysMon
- Proprietà ChartScroll SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà ChartScroll
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964322"
---
# <a name="systemmonitorchartscroll-property"></a><span data-ttu-id="29171-106">Proprietà SystemMonitor. ChartScroll</span><span class="sxs-lookup"><span data-stu-id="29171-106">SystemMonitor.ChartScroll property</span></span>

<span data-ttu-id="29171-107">Recupera o imposta un valore che determina se il grafico a linee scorre nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="29171-107">Retrieves or sets a value that determines if the line graph scrolls in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="29171-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29171-108">Syntax</span></span>


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a><span data-ttu-id="29171-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="29171-109">Property value</span></span>

<span data-ttu-id="29171-110">True se il grafico a linee scorre continuamente da destra a sinistra; in caso contrario, false se il grafico a linee viene disegnato da sinistra a destra e viene eseguito il wrapping su se stesso nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="29171-110">True if the line graph scrolls continuously from right to left; otherwise, False if the line graph is drawn from left to right and wraps around on itself in the view.</span></span> <span data-ttu-id="29171-111">False è l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="29171-111">False is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="29171-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="29171-112">Remarks</span></span>

<span data-ttu-id="29171-113">Questo valore viene ignorato se [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) non è [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span><span class="sxs-lookup"><span data-stu-id="29171-113">This value is ignored if the [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="requirements"></a><span data-ttu-id="29171-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29171-114">Requirements</span></span>



| <span data-ttu-id="29171-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="29171-115">Requirement</span></span> | <span data-ttu-id="29171-116">Valore</span><span class="sxs-lookup"><span data-stu-id="29171-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29171-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29171-117">Minimum supported client</span></span><br/> | <span data-ttu-id="29171-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29171-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29171-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29171-119">Minimum supported server</span></span><br/> | <span data-ttu-id="29171-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29171-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29171-121">DLL</span><span class="sxs-lookup"><span data-stu-id="29171-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29171-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="29171-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





