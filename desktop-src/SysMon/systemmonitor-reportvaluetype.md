---
title: Proprietà SystemMonitor. ReportValueType
description: Recupera o imposta un valore che determina se l'istogramma e le visualizzazioni del rapporto disegnano l'ultimo valore campionato durante l'intervallo di campionamento o un valore calcolato dal campionamento, ad esempio il valore medio o minimo del contatore.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Proprietà ReportValueType SysMon
- Proprietà ReportValueType SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà ReportValueType
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964178"
---
# <a name="systemmonitorreportvaluetype-property"></a><span data-ttu-id="0ea9c-106">Proprietà SystemMonitor. ReportValueType</span><span class="sxs-lookup"><span data-stu-id="0ea9c-106">SystemMonitor.ReportValueType property</span></span>

<span data-ttu-id="0ea9c-107">Recupera o imposta un valore che determina se l'istogramma e le visualizzazioni del rapporto disegnano l'ultimo valore campionato durante l'intervallo di campionamento o un valore calcolato dal campionamento, ad esempio il valore medio o minimo del contatore.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-107">Retrieves or sets a value that determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling, such as the average or minimum counter value.</span></span>

<span data-ttu-id="0ea9c-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea9c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ea9c-109">Syntax</span></span>


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="0ea9c-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0ea9c-110">Property value</span></span>

<span data-ttu-id="0ea9c-111">Determina se l'istogramma e le visualizzazioni del report disegnano l'ultimo valore campionato durante l'intervallo di campionamento o un valore calcolato dall'intervallo di campionamento.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-111">Determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling interval.</span></span> <span data-ttu-id="0ea9c-112">Per i valori possibili, vedere [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="0ea9c-112">For possible values, see [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ea9c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ea9c-113">Remarks</span></span>

<span data-ttu-id="0ea9c-114">SYSMON ignora questo valore e USA [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) se [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) non è [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) o **DisplayTypeConstants.sysmonReport**.</span><span class="sxs-lookup"><span data-stu-id="0ea9c-114">SYSMON ignores this value and uses [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) if [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) or **DisplayTypeConstants.sysmonReport**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ea9c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ea9c-115">Requirements</span></span>



| <span data-ttu-id="0ea9c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ea9c-116">Requirement</span></span> | <span data-ttu-id="0ea9c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0ea9c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea9c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ea9c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0ea9c-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0ea9c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0ea9c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ea9c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0ea9c-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0ea9c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ea9c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0ea9c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ea9c-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="0ea9c-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ea9c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ea9c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea9c-125">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="0ea9c-125">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





