---
title: Proprietà CounterItem. Width
description: Recupera o imposta la lunghezza riga utilizzata per rappresentare il valore del contatore.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Proprietà Width SysMon
- Proprietà Width SysMon, classe CounterItem
- Classe CounterItem SysMon, proprietà Width
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741786"
---
# <a name="counteritemwidth-property"></a><span data-ttu-id="1dc44-106">Proprietà CounterItem. Width</span><span class="sxs-lookup"><span data-stu-id="1dc44-106">CounterItem.Width property</span></span>

<span data-ttu-id="1dc44-107">Recupera o imposta la lunghezza riga utilizzata per rappresentare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="1dc44-107">Retrieves or sets the line width used to graph the counter value.</span></span>

<span data-ttu-id="1dc44-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1dc44-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc44-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1dc44-109">Syntax</span></span>


```VB
Property Width As Long
```



## <a name="property-value"></a><span data-ttu-id="1dc44-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1dc44-110">Property value</span></span>

<span data-ttu-id="1dc44-111">Spessore riga utilizzato in un grafico a linee.</span><span class="sxs-lookup"><span data-stu-id="1dc44-111">Line width used in a line graph.</span></span> <span data-ttu-id="1dc44-112">I valori validi sono compresi tra 1 e 3, dove 1 (il valore predefinito) è la larghezza più stretta.</span><span class="sxs-lookup"><span data-stu-id="1dc44-112">Valid values range from 1 to 3, where 1 (the default value) is the narrowest width.</span></span>

<span data-ttu-id="1dc44-113">**Prima di Windows Vista:** I valori validi sono compresi tra 1 e 9.</span><span class="sxs-lookup"><span data-stu-id="1dc44-113">**Prior to Windows Vista:** Valid values range from 1 to 9.</span></span> <span data-ttu-id="1dc44-114">Se l'applicazione verrà eseguita in Windows Vista, non utilizzare un valore di larghezza maggiore di 3.</span><span class="sxs-lookup"><span data-stu-id="1dc44-114">Do not use a width value greater than 3 if your application will be run on Windows Vista.</span></span>

## <a name="exceptions"></a><span data-ttu-id="1dc44-115">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="1dc44-115">Exceptions</span></span>



| <span data-ttu-id="1dc44-116">Tipo di eccezione</span><span class="sxs-lookup"><span data-stu-id="1dc44-116">Exception type</span></span>               | <span data-ttu-id="1dc44-117">Condizione</span><span class="sxs-lookup"><span data-stu-id="1dc44-117">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="1dc44-118">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="1dc44-118">**System.ArgumentException**</span></span> | <span data-ttu-id="1dc44-119">Lunghezza riga specificata non valida.</span><span class="sxs-lookup"><span data-stu-id="1dc44-119">The specified line width is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1dc44-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="1dc44-120">Remarks</span></span>

<span data-ttu-id="1dc44-121">La lunghezza di riga predefinita per i primi sedici contatori aggiunti è 1.</span><span class="sxs-lookup"><span data-stu-id="1dc44-121">The default line width for the first sixteen counters that you add is 1.</span></span> <span data-ttu-id="1dc44-122">La lunghezza di riga predefinita per i successivi sedici contatori (contatori 17-32) aggiunti è 2.</span><span class="sxs-lookup"><span data-stu-id="1dc44-122">The default line width for the next sixteen counters (counters 17 - 32) that you add is 2.</span></span> <span data-ttu-id="1dc44-123">La lunghezza di riga predefinita per i successivi sedici contatori (contatori 33-48) aggiunta è 3.</span><span class="sxs-lookup"><span data-stu-id="1dc44-123">The default line width for the next sixteen counters (counters 33 - 48) that you add is 3.</span></span> <span data-ttu-id="1dc44-124">Successivamente, SYSMON sceglie in modo casuale la lunghezza della linea.</span><span class="sxs-lookup"><span data-stu-id="1dc44-124">After that, SYSMON randomly chooses the line width.</span></span> <span data-ttu-id="1dc44-125">Per informazioni dettagliate, vedere [**CounterItem. Color**](counteritem-color.md).</span><span class="sxs-lookup"><span data-stu-id="1dc44-125">For details, see [**CounterItem.Color**](counteritem-color.md).</span></span>

<span data-ttu-id="1dc44-126">Per specificare uno [**stile di linea**](counteritem-linestyle.md) diverso da Solid, la larghezza deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="1dc44-126">To specify a [**line style**](counteritem-linestyle.md) other than solid, the width must be 1.</span></span> <span data-ttu-id="1dc44-127">Se si specifica un valore maggiore di 1 e si specifica uno stile di linea non a tinta unita, SYSMON ignora la lunghezza di riga specificata.</span><span class="sxs-lookup"><span data-stu-id="1dc44-127">If you specify a value greater than 1 and specify a non-solid line style, SYSMON ignores the specified line width.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dc44-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dc44-128">Requirements</span></span>



| <span data-ttu-id="1dc44-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc44-129">Requirement</span></span> | <span data-ttu-id="1dc44-130">Valore</span><span class="sxs-lookup"><span data-stu-id="1dc44-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc44-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dc44-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc44-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1dc44-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1dc44-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dc44-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc44-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1dc44-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1dc44-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1dc44-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dc44-136"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1dc44-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dc44-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1dc44-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc44-138">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="1dc44-138">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





