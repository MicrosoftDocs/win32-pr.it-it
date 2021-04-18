---
title: Proprietà SystemMonitor. Appearance
description: Recupera o imposta l'aspetto del controllo in modo da includere o omettere gli effetti di visualizzazione tridimensionali.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Proprietà Appearance SysMon
- Proprietà Appearance SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà Appearance
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200c66f83a47f15421480967e8ea1ae9509b13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301064"
---
# <a name="systemmonitorappearance-property"></a><span data-ttu-id="43acb-106">Proprietà SystemMonitor. Appearance</span><span class="sxs-lookup"><span data-stu-id="43acb-106">SystemMonitor.Appearance property</span></span>

<span data-ttu-id="43acb-107">Recupera o imposta l'aspetto del controllo in modo da includere o omettere gli effetti di visualizzazione tridimensionali.</span><span class="sxs-lookup"><span data-stu-id="43acb-107">Retrieves or sets the control's appearance to include or omit three-dimensional display effects.</span></span>

<span data-ttu-id="43acb-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="43acb-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="43acb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43acb-109">Syntax</span></span>


```VB
Property Appearance As Long
```



## <a name="property-value"></a><span data-ttu-id="43acb-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="43acb-110">Property value</span></span>

<span data-ttu-id="43acb-111">Valore di aspetto che determina se il controllo viene disegnato con effetti tridimensionali.</span><span class="sxs-lookup"><span data-stu-id="43acb-111">Appearance value that determines if the control is painted with three-dimensional effects.</span></span>

<span data-ttu-id="43acb-112">È possibile impostare questa proprietà su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="43acb-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="43acb-113">Valore</span><span class="sxs-lookup"><span data-stu-id="43acb-113">Value</span></span>                                                                        | <span data-ttu-id="43acb-114">Significato</span><span class="sxs-lookup"><span data-stu-id="43acb-114">Meaning</span></span>                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43acb-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="43acb-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="43acb-116">Disegna il controllo senza effetti visivi.</span><span class="sxs-lookup"><span data-stu-id="43acb-116">Paints the control without visual effects.</span></span><br/>                                    |
| <dl> <span data-ttu-id="43acb-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="43acb-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="43acb-118">Disegna il controllo con effetti tridimensionali.</span><span class="sxs-lookup"><span data-stu-id="43acb-118">Paints the control with three-dimensional effects.</span></span> <span data-ttu-id="43acb-119">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="43acb-119">This is the default value.</span></span><br/> |



 

## <a name="exceptions"></a><span data-ttu-id="43acb-120">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="43acb-120">Exceptions</span></span>



| <span data-ttu-id="43acb-121">Tipo di eccezione</span><span class="sxs-lookup"><span data-stu-id="43acb-121">Exception type</span></span>               | <span data-ttu-id="43acb-122">Condizione</span><span class="sxs-lookup"><span data-stu-id="43acb-122">Condition</span></span>                                    |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="43acb-123">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="43acb-123">**System.ArgumentException**</span></span> | <span data-ttu-id="43acb-124">Il valore dell'aspetto specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="43acb-124">The specified appearance value is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="43acb-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="43acb-125">Remarks</span></span>

<span data-ttu-id="43acb-126">Si tratta di una proprietà di ambiente.</span><span class="sxs-lookup"><span data-stu-id="43acb-126">This is an ambient property.</span></span> <span data-ttu-id="43acb-127">Il valore di questa proprietà è determinato dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="43acb-127">The value of this property is determined by the container.</span></span> <span data-ttu-id="43acb-128">L'impostazione del valore di questa proprietà potrebbe influire sull'illusione del controllo e del contenitore come una singola applicazione.</span><span class="sxs-lookup"><span data-stu-id="43acb-128">Setting the value of this property could affect the illusion of the control and container being a single application.</span></span>

## <a name="requirements"></a><span data-ttu-id="43acb-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43acb-129">Requirements</span></span>



| <span data-ttu-id="43acb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="43acb-130">Requirement</span></span> | <span data-ttu-id="43acb-131">Valore</span><span class="sxs-lookup"><span data-stu-id="43acb-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43acb-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43acb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="43acb-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="43acb-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="43acb-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43acb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="43acb-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="43acb-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43acb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="43acb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43acb-137"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="43acb-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43acb-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43acb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43acb-139">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="43acb-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





