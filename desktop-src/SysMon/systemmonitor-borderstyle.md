---
title: Proprietà SystemMonitor. BorderStyle
description: Recupera o imposta lo stile del bordo del controllo.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- Proprietà BorderStyle SysMon
- Proprietà BorderStyle SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà BorderStyle
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873701"
---
# <a name="systemmonitorborderstyle-property"></a><span data-ttu-id="9d2d6-106">Proprietà SystemMonitor. BorderStyle</span><span class="sxs-lookup"><span data-stu-id="9d2d6-106">SystemMonitor.BorderStyle property</span></span>

<span data-ttu-id="9d2d6-107">Recupera o imposta lo stile del bordo del controllo.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-107">Retrieves or sets the border style of the control.</span></span>

<span data-ttu-id="9d2d6-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d2d6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d2d6-109">Syntax</span></span>


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="9d2d6-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9d2d6-110">Property value</span></span>

<span data-ttu-id="9d2d6-111">Stile del bordo del controllo.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-111">Border style of the control.</span></span>

<span data-ttu-id="9d2d6-112">È possibile impostare questa proprietà su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="9d2d6-113">Valore</span><span class="sxs-lookup"><span data-stu-id="9d2d6-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="9d2d6-114">Significato</span><span class="sxs-lookup"><span data-stu-id="9d2d6-114">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <span data-ttu-id="9d2d6-115"><dt>**System. Windows. Forms. FormBorderStyle. VbBSNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9d2d6-115"><dt>**System.Windows.Forms.FormBorderStyle.VbBSNone**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="9d2d6-116">Nessun bordo.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-116">No border.</span></span> <span data-ttu-id="9d2d6-117">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-117">This is the default value.</span></span><br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <span data-ttu-id="9d2d6-118"><dt>**System. Windows. Forms. FormBorderStyle. VbFixedSingle**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9d2d6-118"><dt>**System.Windows.Forms.FormBorderStyle.VbFixedSingle**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="9d2d6-119">Fisso, singolo bordo.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-119">Fixed, single border.</span></span><br/>                 |



 

## <a name="exceptions"></a><span data-ttu-id="9d2d6-120">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="9d2d6-120">Exceptions</span></span>



| <span data-ttu-id="9d2d6-121">Tipo di eccezione</span><span class="sxs-lookup"><span data-stu-id="9d2d6-121">Exception type</span></span>               | <span data-ttu-id="9d2d6-122">Condizione</span><span class="sxs-lookup"><span data-stu-id="9d2d6-122">Condition</span></span>                                |
|------------------------------|------------------------------------------|
| <span data-ttu-id="9d2d6-123">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="9d2d6-123">**System.ArgumentException**</span></span> | <span data-ttu-id="9d2d6-124">Lo stile del bordo specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-124">The specified border style is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9d2d6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d2d6-125">Requirements</span></span>



| <span data-ttu-id="9d2d6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d2d6-126">Requirement</span></span> | <span data-ttu-id="9d2d6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="9d2d6-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d2d6-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d2d6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9d2d6-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9d2d6-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9d2d6-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d2d6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9d2d6-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9d2d6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d2d6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9d2d6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d2d6-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="9d2d6-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d2d6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d2d6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d2d6-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="9d2d6-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





