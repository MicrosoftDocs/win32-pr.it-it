---
title: Raccolta dei contatori (Isysmon. h)
description: Utilizzare questa classe per gestire la raccolta di oggetti CounterItem. Per recuperare l'oggetto, chiamare SystemMonitor. Counters.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- SysMon raccolta contatori
- Raccolta di contatori SysMon, descritti
topic_type:
- apiref
api_name:
- Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbf8da93f13dce2ce2a290adeab9394ee8addb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302249"
---
# <a name="counters-collection"></a><span data-ttu-id="68847-106">Raccolta di contatori</span><span class="sxs-lookup"><span data-stu-id="68847-106">Counters collection</span></span>

<span data-ttu-id="68847-107">Utilizzare questa classe per gestire la raccolta di oggetti [**CounterItem**](counteritem.md) .</span><span class="sxs-lookup"><span data-stu-id="68847-107">Use this class to manage the collection of [**CounterItem**](counteritem.md) objects.</span></span>

<span data-ttu-id="68847-108">Per recuperare l'oggetto, chiamare [**SystemMonitor. Counters**](systemmonitor-counters.md).</span><span class="sxs-lookup"><span data-stu-id="68847-108">To retrieve this object, call [**SystemMonitor.Counters**](systemmonitor-counters.md).</span></span>

## <a name="members"></a><span data-ttu-id="68847-109">Membri</span><span class="sxs-lookup"><span data-stu-id="68847-109">Members</span></span>

<span data-ttu-id="68847-110">La raccolta di **contatori** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="68847-110">The **Counters** collection has these types of members:</span></span>

-   [<span data-ttu-id="68847-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="68847-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="68847-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68847-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="68847-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="68847-113">Methods</span></span>

<span data-ttu-id="68847-114">La raccolta di **contatori** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="68847-114">The **Counters** collection has these methods.</span></span>



| <span data-ttu-id="68847-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="68847-115">Method</span></span>                            | <span data-ttu-id="68847-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68847-116">Description</span></span>                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="68847-117">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="68847-117">**Add**</span></span>](counters-add.md)       | <span data-ttu-id="68847-118">Aggiunge un'istanza di [**CounterItem**](counteritem.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="68847-118">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="68847-119">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="68847-119">**Remove**</span></span>](counters-remove.md) | <span data-ttu-id="68847-120">Rimuove un'istanza di [**CounterItem**](counteritem.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="68847-120">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="68847-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68847-121">Properties</span></span>

<span data-ttu-id="68847-122">La raccolta di **contatori** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="68847-122">The **Counters** collection has these properties.</span></span>



| <span data-ttu-id="68847-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68847-123">Property</span></span>                                   | <span data-ttu-id="68847-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68847-124">Description</span></span>                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68847-125">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="68847-125">**Count**</span></span>](counters-count.md)<br/> | <span data-ttu-id="68847-126">Recupera il numero di istanze di [**CounterItem**](counteritem.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="68847-126">Retrieves the number of [**CounterItem**](counteritem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="68847-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="68847-127">**Item**</span></span>](counters-item.md)<br/>   | <span data-ttu-id="68847-128">Recupera l'istanza di [**CounterItem**](counteritem.md) specificata dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="68847-128">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="68847-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="68847-129">Remarks</span></span>

<span data-ttu-id="68847-130">L'oggetto **contatori** è la proprietà predefinita dell'oggetto [**SystemMonitor**](systemmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="68847-130">The **Counters** object is the default property of the [**SystemMonitor**](systemmonitor.md) object.</span></span>

<span data-ttu-id="68847-131">Aggiungere a questa raccolta i contatori che si desidera rappresentare nel grafico.</span><span class="sxs-lookup"><span data-stu-id="68847-131">Add to this collection those counters that you want to graph.</span></span> <span data-ttu-id="68847-132">SYSMON recupera i valori del contatore dal sistema o da un file di log a seconda dell' [**origine dati**](systemmonitor-datasourcetype.md) specificata.</span><span class="sxs-lookup"><span data-stu-id="68847-132">SYSMON retrieves the counter values either from the system or from a log file depending on the [**data source**](systemmonitor-datasourcetype.md) that you specify.</span></span>

## <a name="requirements"></a><span data-ttu-id="68847-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68847-133">Requirements</span></span>



| <span data-ttu-id="68847-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="68847-134">Requirement</span></span> | <span data-ttu-id="68847-135">Valore</span><span class="sxs-lookup"><span data-stu-id="68847-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68847-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68847-136">Minimum supported client</span></span><br/> | <span data-ttu-id="68847-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="68847-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="68847-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68847-138">Minimum supported server</span></span><br/> | <span data-ttu-id="68847-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="68847-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68847-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68847-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="68847-141"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="68847-141"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="68847-142">DLL</span><span class="sxs-lookup"><span data-stu-id="68847-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68847-143"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="68847-143"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





