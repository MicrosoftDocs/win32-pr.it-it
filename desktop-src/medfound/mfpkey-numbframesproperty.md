---
description: Specifica il numero di frame predittivi bidirezionali (fotogrammi B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: Proprietà MFPKEY_NUMBFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310622"
---
# <a name="mfpkey_numbframes-property"></a><span data-ttu-id="f5297-103">\_Proprietà NUMBFRAMES di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="f5297-103">MFPKEY\_NUMBFRAMES Property</span></span>

<span data-ttu-id="f5297-104">Specifica il numero di frame predittivi bidirezionali (fotogrammi B).</span><span class="sxs-lookup"><span data-stu-id="f5297-104">Specifies the number of bidirectional predictive frames (B-frames).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f5297-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f5297-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f5297-106">g \_ wszWMVCNumBFrames</span><span class="sxs-lookup"><span data-stu-id="f5297-106">g\_wszWMVCNumBFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="f5297-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f5297-107">Data Type</span></span>

<span data-ttu-id="f5297-108">VT-I4</span><span class="sxs-lookup"><span data-stu-id="f5297-108">VT-I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f5297-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="f5297-109">Default Value</span></span>

<span data-ttu-id="f5297-110">0</span><span class="sxs-lookup"><span data-stu-id="f5297-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="f5297-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5297-111">Remarks</span></span>

<span data-ttu-id="f5297-112">Per impostazione predefinita, Windows Media Video 9 utilizza solo i fotogrammi (I-frame), noti anche come fotogrammi chiave o frame di ancoraggio, che sono frame completamente codificati e frame predittivi (fotogrammi P), che vengono codificati come differenza rispetto al frame I precedente.</span><span class="sxs-lookup"><span data-stu-id="f5297-112">By default, Windows Media Video 9 uses only intraframes (I-frames), also known as key frames or anchor frames, which are fully encoded frames, and predictive frames (P-frames), which are encoded as a difference from the previous I-frame.</span></span> <span data-ttu-id="f5297-113">I frame B sono diversi dai fotogrammi P perché archiviano le differenze rispetto al frame precedente e le differenze rispetto al frame seguente.</span><span class="sxs-lookup"><span data-stu-id="f5297-113">B-frames are different from P-frames because they store both the differences from the previous frame and the differences from the following frame.</span></span>

<span data-ttu-id="f5297-114">Quando si configura il codec per l'utilizzo di fotogrammi B, verrà utilizzato il numero specificato di fotogrammi B tra ogni coppia di frame del tipo I o P.</span><span class="sxs-lookup"><span data-stu-id="f5297-114">When you configure the codec to uses B-frames, it will use the specified number of B-frames between each pair of frames of either I or P type.</span></span>

<span data-ttu-id="f5297-115">Se, ad esempio, una sequenza di frame senza fotogrammi B è "IPPPPPPPPI", la stessa codifica di sequenza con due fotogrammi B sarà "IBBPBBPBBI".</span><span class="sxs-lookup"><span data-stu-id="f5297-115">For example, if a sequence of frames without B-frames is "IPPPPPPPPI" then the same sequence encoding with two B-frames would be "IBBPBBPBBI".</span></span>

<span data-ttu-id="f5297-116">Per la maggior parte del contenuto, uno o due fotogrammi B sono appropriati.</span><span class="sxs-lookup"><span data-stu-id="f5297-116">For most content either one or two B-frames are appropriate.</span></span> <span data-ttu-id="f5297-117">Con una frequenza dati più elevata, un frame B è in genere la scelta ottimale.</span><span class="sxs-lookup"><span data-stu-id="f5297-117">At higher data rates, one B-frame is normally the optimal choice.</span></span> <span data-ttu-id="f5297-118">Sono raramente utili tre o più.</span><span class="sxs-lookup"><span data-stu-id="f5297-118">Three or more are rarely useful.</span></span>

<span data-ttu-id="f5297-119">L'intervallo valido di valori per questa proprietà è compreso tra 0 e 7.</span><span class="sxs-lookup"><span data-stu-id="f5297-119">The valid range of values for this property is 0 to 7.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5297-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5297-120">Requirements</span></span>



| <span data-ttu-id="f5297-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5297-121">Requirement</span></span> | <span data-ttu-id="f5297-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f5297-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5297-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5297-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f5297-124">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f5297-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f5297-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5297-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f5297-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5297-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5297-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5297-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5297-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5297-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5297-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5297-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5297-130">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5297-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




