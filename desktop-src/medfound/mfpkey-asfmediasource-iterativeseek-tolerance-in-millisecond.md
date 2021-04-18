---
description: Imposta la tolleranza, in millisecondi, utilizzata quando l'origine multimediale ASF esegue la ricerca iterativa.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: Proprietà MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320667"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a><span data-ttu-id="d26a3-103">MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance \_ , \_ Proprietà in millisecondi</span><span class="sxs-lookup"><span data-stu-id="d26a3-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond property</span></span>

<span data-ttu-id="d26a3-104">Imposta la tolleranza, in millisecondi, utilizzata quando l'origine multimediale ASF esegue la ricerca iterativa.</span><span class="sxs-lookup"><span data-stu-id="d26a3-104">Sets the tolerance, in milliseconds, that is used when the ASF media source performs iterative seeking.</span></span>



<span data-ttu-id="d26a3-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d26a3-105">Data type</span></span>

<span data-ttu-id="d26a3-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="d26a3-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d26a3-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="d26a3-107">PROPVARIANT member</span></span>

<span data-ttu-id="d26a3-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="d26a3-108">**ULONG**</span></span>

<span data-ttu-id="d26a3-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="d26a3-109">VT\_UI4</span></span>

<span data-ttu-id="d26a3-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="d26a3-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="d26a3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d26a3-111">Remarks</span></span>

<span data-ttu-id="d26a3-112">Usare questa proprietà per configurare l'origine del supporto ASF.</span><span class="sxs-lookup"><span data-stu-id="d26a3-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="d26a3-113">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="d26a3-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="d26a3-114">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="d26a3-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="d26a3-115">Questa proprietà si applica solo quando è abilitata la ricerca iterativa.</span><span class="sxs-lookup"><span data-stu-id="d26a3-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="d26a3-116">Per ulteriori informazioni, vedere [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="d26a3-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="d26a3-117">L'algoritmo di ricerca iterativo si interrompe se trova un pacchetto la cui distanza dal tempo di ricerca rientra nella tolleranza specificata.</span><span class="sxs-lookup"><span data-stu-id="d26a3-117">The iterative seeking algorithm halts if it finds a packet whose distance from the seek time is within the specified tolerance.</span></span> <span data-ttu-id="d26a3-118">Il valore predefinito è 8000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="d26a3-118">The default value is 8000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="d26a3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d26a3-119">Requirements</span></span>



| <span data-ttu-id="d26a3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d26a3-120">Requirement</span></span> | <span data-ttu-id="d26a3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d26a3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d26a3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d26a3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d26a3-123">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d26a3-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d26a3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d26a3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d26a3-125">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d26a3-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d26a3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d26a3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d26a3-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d26a3-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d26a3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d26a3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d26a3-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d26a3-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




