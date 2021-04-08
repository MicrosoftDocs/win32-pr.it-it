---
title: Oggetto CounterItem (Isysmon. h)
description: Utilizzare questa classe per recuperare il percorso e il valore di un contatore e per specificare il colore utilizzato per il grafico del contatore. Per recuperare questo oggetto, chiamare Counters. Item.
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- Oggetto CounterItem SysMon
- Oggetto CounterItem SysMon, descritto
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741914"
---
# <a name="counteritem-object"></a><span data-ttu-id="bae99-106">Oggetto CounterItem</span><span class="sxs-lookup"><span data-stu-id="bae99-106">CounterItem object</span></span>

<span data-ttu-id="bae99-107">Utilizzare questa classe per recuperare il percorso e il valore di un contatore e per specificare il colore utilizzato per il grafico del contatore.</span><span class="sxs-lookup"><span data-stu-id="bae99-107">Use this class to retrieve the path and value of a counter and to specify the color used to graph the counter.</span></span>

<span data-ttu-id="bae99-108">Per recuperare questo oggetto, chiamare [**Counters. Item**](counters-item.md).</span><span class="sxs-lookup"><span data-stu-id="bae99-108">To retrieve this object, call [**Counters.Item**](counters-item.md).</span></span>

## <a name="members"></a><span data-ttu-id="bae99-109">Membri</span><span class="sxs-lookup"><span data-stu-id="bae99-109">Members</span></span>

<span data-ttu-id="bae99-110">L'oggetto **CounterItem** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bae99-110">The **CounterItem** object has these types of members:</span></span>

-   [<span data-ttu-id="bae99-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="bae99-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="bae99-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bae99-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bae99-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="bae99-113">Methods</span></span>

<span data-ttu-id="bae99-114">L'oggetto **CounterItem** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bae99-114">The **CounterItem** object has these methods.</span></span>



| <span data-ttu-id="bae99-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="bae99-115">Method</span></span>                                             | <span data-ttu-id="bae99-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bae99-116">Description</span></span>                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="bae99-117">**GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="bae99-117">**GetDataAt**</span></span>](counteritem-getdataat.md)         | <span data-ttu-id="bae99-118">Recupera i dati del contatore da un punto specifico nel grafico a linee.</span><span class="sxs-lookup"><span data-stu-id="bae99-118">Retrieves the counter data from a specific point in the line graph.</span></span><br/> |
| [<span data-ttu-id="bae99-119">**GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="bae99-119">**GetStatistics**</span></span>](counteritem-getstatistics.md) | <span data-ttu-id="bae99-120">Recupera i valori medio, massimo e minimo per il contatore.</span><span class="sxs-lookup"><span data-stu-id="bae99-120">Retrieves the average, maximum, and minimum values for the counter.</span></span><br/> |
| [<span data-ttu-id="bae99-121">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="bae99-121">**GetValue**</span></span>](counteritem-getvalue.md)           | <span data-ttu-id="bae99-122">Recupera l'ultimo valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="bae99-122">Retrieves the last value of the counter.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="bae99-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bae99-123">Properties</span></span>

<span data-ttu-id="bae99-124">L'oggetto **CounterItem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bae99-124">The **CounterItem** object has these properties.</span></span>



| <span data-ttu-id="bae99-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bae99-125">Property</span></span>                                                  | <span data-ttu-id="bae99-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bae99-126">Description</span></span>                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="bae99-127">**Colore**</span><span class="sxs-lookup"><span data-stu-id="bae99-127">**Color**</span></span>](counteritem-color.md)<br/>             | <span data-ttu-id="bae99-128">Recupera o imposta il colore utilizzato per rappresentare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="bae99-128">Retrieves or sets the color used to graph the counter value.</span></span><br/>         |
| [<span data-ttu-id="bae99-129">**LineStyle**</span><span class="sxs-lookup"><span data-stu-id="bae99-129">**LineStyle**</span></span>](counteritem-linestyle.md)<br/>     | <span data-ttu-id="bae99-130">Recupera o imposta lo stile di linea utilizzato per rappresentare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="bae99-130">Retrieves or sets the line style used to graph the counter value.</span></span><br/>    |
| [<span data-ttu-id="bae99-131">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="bae99-131">**Path**</span></span>](counteritem-path.md)<br/>               | <span data-ttu-id="bae99-132">Recupera il percorso del contatore.</span><span class="sxs-lookup"><span data-stu-id="bae99-132">Retrieves the path of the counter.</span></span><br/>                                   |
| [<span data-ttu-id="bae99-133">**ScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="bae99-133">**ScaleFactor**</span></span>](counteritem-scalefactor.md)<br/> | <span data-ttu-id="bae99-134">Recupera o imposta il fattore di scala utilizzato per rappresentare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="bae99-134">Retrieves or sets the scale factor used to graph the counter value.</span></span><br/>  |
| [<span data-ttu-id="bae99-135">**Selezionato**</span><span class="sxs-lookup"><span data-stu-id="bae99-135">**Selected**</span></span>](counteritem-selected.md)<br/>       | <span data-ttu-id="bae99-136">Recupera o imposta un valore che indica se il contatore è selezionato.</span><span class="sxs-lookup"><span data-stu-id="bae99-136">Retrieves or sets a value that indicates if the counter is selected.</span></span><br/> |
| [<span data-ttu-id="bae99-137">**Valore**</span><span class="sxs-lookup"><span data-stu-id="bae99-137">**Value**</span></span>](counteritem-value.md)<br/>             | <span data-ttu-id="bae99-138">Recupera il valore corrente del contatore.</span><span class="sxs-lookup"><span data-stu-id="bae99-138">Retrieves the current value of the counter.</span></span><br/>                          |
| [<span data-ttu-id="bae99-139">**Visible**</span><span class="sxs-lookup"><span data-stu-id="bae99-139">**Visible**</span></span>](counteritem-visible.md)<br/>         | <span data-ttu-id="bae99-140">Recupera o imposta un valore che indica se il contatore è associato a un grafico.</span><span class="sxs-lookup"><span data-stu-id="bae99-140">Retrieves or sets a value that indicates if the counter is graphed.</span></span><br/>  |
| [<span data-ttu-id="bae99-141">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="bae99-141">**Width**</span></span>](counteritem-width.md)<br/>             | <span data-ttu-id="bae99-142">Recupera o imposta la lunghezza riga utilizzata per rappresentare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="bae99-142">Retrieves or sets the line width used to graph the counter value.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="bae99-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="bae99-143">Remarks</span></span>

<span data-ttu-id="bae99-144">[**Value**](counteritem-value.md) è la proprietà predefinita di **CounterItem**.</span><span class="sxs-lookup"><span data-stu-id="bae99-144">[**Value**](counteritem-value.md) is the default property of **CounterItem**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bae99-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bae99-145">Requirements</span></span>



| <span data-ttu-id="bae99-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="bae99-146">Requirement</span></span> | <span data-ttu-id="bae99-147">Valore</span><span class="sxs-lookup"><span data-stu-id="bae99-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bae99-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bae99-148">Minimum supported client</span></span><br/> | <span data-ttu-id="bae99-149">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bae99-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bae99-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bae99-150">Minimum supported server</span></span><br/> | <span data-ttu-id="bae99-151">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bae99-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bae99-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bae99-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="bae99-153"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bae99-153"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="bae99-154">DLL</span><span class="sxs-lookup"><span data-stu-id="bae99-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bae99-155"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="bae99-155"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bae99-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bae99-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae99-157">Classi SYSMON</span><span class="sxs-lookup"><span data-stu-id="bae99-157">SYSMON Classes</span></span>](sysmon-classes.md)
</dt> </dl>

 

 





