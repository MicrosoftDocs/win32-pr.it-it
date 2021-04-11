---
title: Proprietà SystemMonitor. DataPointCount
description: Recupera o imposta il numero di punti dati visualizzati in un grafico a linee.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Proprietà DataPointCount SysMon
- Proprietà DataPointCount SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà DataPointCount
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963991"
---
# <a name="systemmonitordatapointcount-property"></a><span data-ttu-id="595c9-106">Proprietà SystemMonitor. DataPointCount</span><span class="sxs-lookup"><span data-stu-id="595c9-106">SystemMonitor.DataPointCount property</span></span>

<span data-ttu-id="595c9-107">Recupera o imposta il numero di punti dati visualizzati in un grafico a linee.</span><span class="sxs-lookup"><span data-stu-id="595c9-107">Retrieves or sets the number of data points displayed in a line graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="595c9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="595c9-108">Syntax</span></span>


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a><span data-ttu-id="595c9-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="595c9-109">Property value</span></span>

<span data-ttu-id="595c9-110">Numero di punti dati visualizzati nella visualizzazione per un grafico a linee.</span><span class="sxs-lookup"><span data-stu-id="595c9-110">Number of data points displayed in the view for a line graph.</span></span> <span data-ttu-id="595c9-111">Il valore predefinito è 100 punti dati.</span><span class="sxs-lookup"><span data-stu-id="595c9-111">The default value is 100 data points.</span></span> <span data-ttu-id="595c9-112">L'intervallo valido di valori è compreso tra 2 e 1.000.</span><span class="sxs-lookup"><span data-stu-id="595c9-112">The valid range of values is 2 to 1,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="595c9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="595c9-113">Remarks</span></span>

<span data-ttu-id="595c9-114">Questa proprietà viene utilizzata solo se [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è **sysmonCurrentActivity**.</span><span class="sxs-lookup"><span data-stu-id="595c9-114">This property is used only if [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is **sysmonCurrentActivity**.</span></span>

## <a name="requirements"></a><span data-ttu-id="595c9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="595c9-115">Requirements</span></span>



| <span data-ttu-id="595c9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="595c9-116">Requirement</span></span> | <span data-ttu-id="595c9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="595c9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="595c9-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="595c9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="595c9-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="595c9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="595c9-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="595c9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="595c9-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="595c9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="595c9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="595c9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="595c9-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="595c9-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





