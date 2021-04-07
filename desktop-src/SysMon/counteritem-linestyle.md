---
title: Proprietà CounterItem. LineStyle
description: Recupera o imposta lo stile di linea utilizzato per rappresentare il valore del contatore.
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- Proprietà LineStyle SysMon
- Proprietà LineStyle SysMon, classe CounterItem
- Classe CounterItem SysMon, proprietà LineStyle
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff1dd78c6fd65d72c28fe8f13f7bbf5603c75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964181"
---
# <a name="counteritemlinestyle-property"></a><span data-ttu-id="f5374-106">Proprietà CounterItem. LineStyle</span><span class="sxs-lookup"><span data-stu-id="f5374-106">CounterItem.LineStyle property</span></span>

<span data-ttu-id="f5374-107">Recupera o imposta lo stile di linea utilizzato per rappresentare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="f5374-107">Retrieves or sets the line style used to graph the counter value.</span></span>

<span data-ttu-id="f5374-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f5374-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5374-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5374-109">Syntax</span></span>


```VB
Property LineStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="f5374-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f5374-110">Property value</span></span>

<span data-ttu-id="f5374-111">Stile di linea utilizzato per rappresentare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="f5374-111">The line style used to graph the counter value.</span></span> <span data-ttu-id="f5374-112">I valori corrispondono alle costanti di sistema illustrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f5374-112">The values correspond to system constants shown in the following table.</span></span>



| <span data-ttu-id="f5374-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f5374-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="f5374-114">Significato</span><span class="sxs-lookup"><span data-stu-id="f5374-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <span data-ttu-id="f5374-115"><dt>**System. Drawing. Drawing2D. DashStyle. Solid**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5374-115"><dt>**System.Drawing.Drawing2D.DashStyle.Solid**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="f5374-116">Linea continua.</span><span class="sxs-lookup"><span data-stu-id="f5374-116">Solid line.</span></span> <span data-ttu-id="f5374-117">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f5374-117">This is the default value.</span></span><br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <span data-ttu-id="f5374-118"><dt>**System. Drawing. Drawing2D. DashStyle. Dash**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f5374-118"><dt>**System.Drawing.Drawing2D.DashStyle.Dash**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="f5374-119">Linea tratteggiata con segmenti lunghi e spazi stretti.</span><span class="sxs-lookup"><span data-stu-id="f5374-119">Dotted line with long segments and narrow spaces.</span></span><br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <span data-ttu-id="f5374-120"><dt>**System. Drawing. Drawing2D. DashStyle. dot**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f5374-120"><dt>**System.Drawing.Drawing2D.DashStyle.Dot**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="f5374-121">Linea tratteggiata con segmenti e spazi uniformi.</span><span class="sxs-lookup"><span data-stu-id="f5374-121">Dotted line with uniform segments and spaces.</span></span><br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <span data-ttu-id="f5374-122"><dt>**System. Drawing. Drawing2D. DashStyle. DashDot**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f5374-122"><dt>**System.Drawing.Drawing2D.DashStyle.DashDot**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="f5374-123">Linea tratteggiata con segmenti alternati brevi e lunghi.</span><span class="sxs-lookup"><span data-stu-id="f5374-123">Dotted line with alternating short and long segments.</span></span><br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <span data-ttu-id="f5374-124"><dt>**System. Drawing. Drawing2D. DashStyle. TrattoPuntoPunto**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f5374-124"><dt>**System.Drawing.Drawing2D.DashStyle.DashDotDot**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="f5374-125">Linea tratteggiata con trattini alternati e punti doppi.</span><span class="sxs-lookup"><span data-stu-id="f5374-125">Dotted line with alternating dashes and double dots.</span></span><br/>  |



 

## <a name="exceptions"></a><span data-ttu-id="f5374-126">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="f5374-126">Exceptions</span></span>



| <span data-ttu-id="f5374-127">Tipo di eccezione</span><span class="sxs-lookup"><span data-stu-id="f5374-127">Exception type</span></span>               | <span data-ttu-id="f5374-128">Condizione</span><span class="sxs-lookup"><span data-stu-id="f5374-128">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="f5374-129">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="f5374-129">**System.ArgumentException**</span></span> | <span data-ttu-id="f5374-130">Lo stile di linea specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="f5374-130">The specified line style is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f5374-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5374-131">Remarks</span></span>

<span data-ttu-id="f5374-132">Per specificare un valore diverso da DashStyle. Solid, [**CounterItem. Width**](counteritem-width.md) deve essere impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="f5374-132">To specify a value other than DashStyle.Solid, [**CounterItem.Width**](counteritem-width.md) must be set to 1.</span></span> <span data-ttu-id="f5374-133">Se la larghezza è maggiore di 1, SYSMON ignora lo stile di linea specificato e USA DashStyle. Solid.</span><span class="sxs-lookup"><span data-stu-id="f5374-133">If the width is greater than 1, SYSMON ignores the specified line style and uses DashStyle.Solid.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5374-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5374-134">Requirements</span></span>



| <span data-ttu-id="f5374-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5374-135">Requirement</span></span> | <span data-ttu-id="f5374-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f5374-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5374-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5374-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f5374-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f5374-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f5374-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5374-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f5374-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f5374-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5374-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f5374-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5374-142"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f5374-142"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5374-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5374-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5374-144">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="f5374-144">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





