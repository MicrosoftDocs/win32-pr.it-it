---
title: Proprietà CounterItem. ScaleFactor
description: Recupera o imposta il fattore di scala utilizzato per rappresentare il valore del contatore.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Proprietà ScaleFactor SysMon
- Proprietà ScaleFactor SysMon, classe CounterItem
- Classe CounterItem SysMon, proprietà ScaleFactor
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301750"
---
# <a name="counteritemscalefactor-property"></a><span data-ttu-id="11b16-106">Proprietà CounterItem. ScaleFactor</span><span class="sxs-lookup"><span data-stu-id="11b16-106">CounterItem.ScaleFactor property</span></span>

<span data-ttu-id="11b16-107">Recupera o imposta il fattore di scala utilizzato per rappresentare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="11b16-107">Retrieves or sets the scale factor used to graph the counter value.</span></span>

<span data-ttu-id="11b16-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="11b16-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="11b16-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11b16-109">Syntax</span></span>


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a><span data-ttu-id="11b16-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="11b16-110">Property value</span></span>

<span data-ttu-id="11b16-111">Fattore di scala utilizzato per visualizzare i valori dei contatori grafici.</span><span class="sxs-lookup"><span data-stu-id="11b16-111">Scale factor used in displaying the graphed counter values.</span></span> <span data-ttu-id="11b16-112">I valori validi sono compresi tra-9 e 9 (i valori corrispondono a 0,000000001-100000000,0).</span><span class="sxs-lookup"><span data-stu-id="11b16-112">Valid values range from -9 to 9 (the values correspond to 0.000000001 - 100000000.0).</span></span>

<span data-ttu-id="11b16-113">**Prima di Windows Vista:** I valori validi sono compresi tra-7 e 7 (i valori corrispondono a 0,0000001-1000000,0).</span><span class="sxs-lookup"><span data-stu-id="11b16-113">**Prior to Windows Vista:** Valid values range from -7 to 7 (the values correspond to 0.0000001 - 1000000.0).</span></span>

## <a name="remarks"></a><span data-ttu-id="11b16-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="11b16-114">Remarks</span></span>

<span data-ttu-id="11b16-115">Impostare questa proprietà solo se si desidera modificare il fattore di scala predefinito del contatore. ogni contatore definisce il proprio fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="11b16-115">Only set this property if you want to change the counter's default scale factor (each counter defines its own scale factor).</span></span> <span data-ttu-id="11b16-116">Il valore di questa proprietà è impostato su Integer. MaxValue se il contatore usa il fattore di scala predefinito per rappresentare i valori.</span><span class="sxs-lookup"><span data-stu-id="11b16-116">The value of this property is set to Integer.MaxValue if the counter is using its default scale factor to graph the values.</span></span>

## <a name="requirements"></a><span data-ttu-id="11b16-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11b16-117">Requirements</span></span>



| <span data-ttu-id="11b16-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="11b16-118">Requirement</span></span> | <span data-ttu-id="11b16-119">Valore</span><span class="sxs-lookup"><span data-stu-id="11b16-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11b16-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11b16-120">Minimum supported client</span></span><br/> | <span data-ttu-id="11b16-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11b16-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="11b16-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11b16-122">Minimum supported server</span></span><br/> | <span data-ttu-id="11b16-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11b16-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11b16-124">DLL</span><span class="sxs-lookup"><span data-stu-id="11b16-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11b16-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="11b16-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11b16-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11b16-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11b16-127">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="11b16-127">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="11b16-128">**SystemMonitor. ScaleToFit**</span><span class="sxs-lookup"><span data-stu-id="11b16-128">**SystemMonitor.ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





