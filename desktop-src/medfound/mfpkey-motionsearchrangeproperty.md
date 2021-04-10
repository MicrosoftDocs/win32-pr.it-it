---
description: Specifica l'intervallo usato nelle ricerche di movimento.
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: Proprietà MFPKEY_MOTIONSEARCHRANGE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227003"
---
# <a name="mfpkey_motionsearchrange-property"></a><span data-ttu-id="4f164-103">\_Proprietà MOTIONSEARCHRANGE di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="4f164-103">MFPKEY\_MOTIONSEARCHRANGE Property</span></span>

<span data-ttu-id="4f164-104">Specifica l'intervallo usato nelle ricerche di movimento.</span><span class="sxs-lookup"><span data-stu-id="4f164-104">Specifies the range used in motion searches.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4f164-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4f164-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4f164-106">g \_ wszWMVCMotionSearchRange</span><span class="sxs-lookup"><span data-stu-id="4f164-106">g\_wszWMVCMotionSearchRange</span></span>

## <a name="data-type"></a><span data-ttu-id="4f164-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4f164-107">Data Type</span></span>

<span data-ttu-id="4f164-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="4f164-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="4f164-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="4f164-109">Default Value</span></span>

<span data-ttu-id="4f164-110">0</span><span class="sxs-lookup"><span data-stu-id="4f164-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="4f164-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f164-111">Remarks</span></span>

<span data-ttu-id="4f164-112">Questa proprietà può essere impostata su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4f164-112">This property may be set to one of the following values.</span></span> <span data-ttu-id="4f164-113">H indica l'intervallo orizzontale e V indica l'intervallo verticale.</span><span class="sxs-lookup"><span data-stu-id="4f164-113">H denotes horizontal range and V denotes vertical range.</span></span> <span data-ttu-id="4f164-114">Tutti gli intervalli sono specificati in pixel.</span><span class="sxs-lookup"><span data-stu-id="4f164-114">All ranges are given in pixels.</span></span>



| <span data-ttu-id="4f164-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4f164-115">Value</span></span> | <span data-ttu-id="4f164-116">Range</span><span class="sxs-lookup"><span data-stu-id="4f164-116">Range</span></span>                                |
|-------|--------------------------------------|
| <span data-ttu-id="4f164-117">0</span><span class="sxs-lookup"><span data-stu-id="4f164-117">0</span></span>     | <span data-ttu-id="4f164-118">+ 63.75/-64,0 H, + 31.75/-32.0 V</span><span class="sxs-lookup"><span data-stu-id="4f164-118">+63.75/-64.0 H, +31.75/-32.0 V</span></span>       |
| <span data-ttu-id="4f164-119">1</span><span class="sxs-lookup"><span data-stu-id="4f164-119">1</span></span>     | <span data-ttu-id="4f164-120">+127,75/-128,0 H, +63,75/-64,0 V</span><span class="sxs-lookup"><span data-stu-id="4f164-120">+127.75/-128.0 H, +63.75/-64.0 V</span></span>     |
| <span data-ttu-id="4f164-121">2</span><span class="sxs-lookup"><span data-stu-id="4f164-121">2</span></span>     | <span data-ttu-id="4f164-122">+ 511.75/-512.0 H, + 127.75/-128.0 V</span><span class="sxs-lookup"><span data-stu-id="4f164-122">+511.75/-512.0 H, +127.75/-128.0 V</span></span>   |
| <span data-ttu-id="4f164-123">3</span><span class="sxs-lookup"><span data-stu-id="4f164-123">3</span></span>     | <span data-ttu-id="4f164-124">+ 1023.75/-1024.0 H, + 255.75/-256.0 V</span><span class="sxs-lookup"><span data-stu-id="4f164-124">+1023.75/-1024.0 H, +255.75/-256.0 V</span></span> |
| <span data-ttu-id="4f164-125">-1</span><span class="sxs-lookup"><span data-stu-id="4f164-125">-1</span></span>    | <span data-ttu-id="4f164-126">Macroblocco-Adaptive (automatico)</span><span class="sxs-lookup"><span data-stu-id="4f164-126">Macroblock-adaptive (automatic)</span></span>      |



 

<span data-ttu-id="4f164-127">Questa proprietà controlla le dimensioni dell'area del frame in cui il codec eseguirà la ricerca di un elemento che potrebbe aver esposto il movimento tra frame.</span><span class="sxs-lookup"><span data-stu-id="4f164-127">This property controls the size of the frame area that the codec will search for an element that may have exhibited motion between frames.</span></span> <span data-ttu-id="4f164-128">Una finestra di ricerca più ampia consente di trovare un movimento più veloce, ma richiederà più tempo della CPU.</span><span class="sxs-lookup"><span data-stu-id="4f164-128">A larger search window will help find faster motion but will require more CPU time.</span></span> <span data-ttu-id="4f164-129">I requisiti della CPU sono approssimativamente doppi a ogni livello.</span><span class="sxs-lookup"><span data-stu-id="4f164-129">The CPU requirements are approximately doubled at each level.</span></span>

<span data-ttu-id="4f164-130">La modalità automatica (-1) consente di selezionare in modo dinamico la modalità più efficiente.</span><span class="sxs-lookup"><span data-stu-id="4f164-130">The automatic mode (-1) will dynamically select the most efficient mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f164-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f164-131">Requirements</span></span>



| <span data-ttu-id="4f164-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f164-132">Requirement</span></span> | <span data-ttu-id="4f164-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4f164-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f164-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f164-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4f164-135">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4f164-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4f164-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f164-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4f164-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4f164-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f164-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f164-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f164-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f164-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f164-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f164-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f164-141">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4f164-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




