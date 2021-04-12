---
title: CounterItem. GetDataAt, metodo
description: Recupera il valore del contatore specificato da un punto specifico nel grafico.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Metodo GetDataAt SysMon
- Metodo GetDataAt SysMon, oggetto CounterItem
- Oggetto CounterItem SysMon, metodo GetDataAt
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517920"
---
# <a name="counteritemgetdataat-method"></a><span data-ttu-id="d2645-106">CounterItem. GetDataAt, metodo</span><span class="sxs-lookup"><span data-stu-id="d2645-106">CounterItem.GetDataAt method</span></span>

<span data-ttu-id="d2645-107">Recupera il valore del contatore specificato da un punto specifico nel grafico.</span><span class="sxs-lookup"><span data-stu-id="d2645-107">Retrieves the specified counter value from a specific point in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2645-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2645-108">Syntax</span></span>


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="d2645-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2645-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2645-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d2645-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2645-111">Indice in base zero del punto grafico di cui si desidera recuperare il valore.</span><span class="sxs-lookup"><span data-stu-id="d2645-111">Zero-based index of the graph point whose value you want to retrieve.</span></span> <span data-ttu-id="d2645-112">I valori validi sono compresi tra 0 e ([**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md) -1).</span><span class="sxs-lookup"><span data-stu-id="d2645-112">Valid values range from 0 to ([**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md) - 1).</span></span>

</dd> <dt>

<span data-ttu-id="d2645-113">*che* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2645-113">*which* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2645-114">Tipo di valore del contatore da recuperare, ad esempio il valore medio del contatore visualizzato nella finestra Graph.</span><span class="sxs-lookup"><span data-stu-id="d2645-114">Type of counter value to retrieve, for example, the average value of the counter as displayed in the graph window.</span></span> <span data-ttu-id="d2645-115">Per i valori possibili, vedere [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span><span class="sxs-lookup"><span data-stu-id="d2645-115">For possible values, see [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span></span>

</dd> <dt>

<span data-ttu-id="d2645-116">*variante* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d2645-116">*variant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2645-117">Valore del contatore recuperato.</span><span class="sxs-lookup"><span data-stu-id="d2645-117">Counter value that was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2645-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2645-118">Return value</span></span>

<span data-ttu-id="d2645-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d2645-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2645-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2645-120">Remarks</span></span>

<span data-ttu-id="d2645-121">Usare questo metodo solo se</span><span class="sxs-lookup"><span data-stu-id="d2645-121">Use this method only if</span></span>

-   <span data-ttu-id="d2645-122">[**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) è impostato su sysmonLineGraph</span><span class="sxs-lookup"><span data-stu-id="d2645-122">[**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is set to sysmonLineGraph</span></span>
-   <span data-ttu-id="d2645-123">[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su SysmonLogFiles o sysmonSqlLog</span><span class="sxs-lookup"><span data-stu-id="d2645-123">[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles or sysmonSqlLog</span></span>

## <a name="requirements"></a><span data-ttu-id="d2645-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2645-124">Requirements</span></span>



| <span data-ttu-id="d2645-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2645-125">Requirement</span></span> | <span data-ttu-id="d2645-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d2645-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2645-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2645-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d2645-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2645-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2645-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2645-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d2645-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d2645-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2645-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d2645-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2645-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="d2645-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2645-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2645-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2645-134">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="d2645-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="d2645-135">**CounterItem. GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="d2645-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="d2645-136">**CounterItem. GetValue**</span><span class="sxs-lookup"><span data-stu-id="d2645-136">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





