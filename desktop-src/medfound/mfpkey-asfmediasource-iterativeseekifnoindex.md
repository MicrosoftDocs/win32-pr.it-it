---
description: Configura l'origine dei supporti ASF in modo da usare la ricerca iterativa se il file di origine non ha un indice.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: Proprietà MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761447"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a><span data-ttu-id="1ff64-103">MFPKEY \_ ASFMediaSource- \_ Proprietà IterativeSeekIfNoIndex</span><span class="sxs-lookup"><span data-stu-id="1ff64-103">MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex property</span></span>

<span data-ttu-id="1ff64-104">Configura l'origine dei supporti ASF in modo da usare la ricerca iterativa se il file di origine non ha un indice.</span><span class="sxs-lookup"><span data-stu-id="1ff64-104">Configures the ASF media source to use iterative seeking if the source file has no index.</span></span>



<span data-ttu-id="1ff64-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1ff64-105">Data type</span></span>

<span data-ttu-id="1ff64-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="1ff64-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1ff64-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="1ff64-107">PROPVARIANT member</span></span>

<span data-ttu-id="1ff64-108">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="1ff64-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="1ff64-109">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="1ff64-109">VT\_BOOL</span></span>

<span data-ttu-id="1ff64-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="1ff64-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1ff64-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ff64-111">Remarks</span></span>

<span data-ttu-id="1ff64-112">Usare questa proprietà per configurare l'origine del supporto ASF.</span><span class="sxs-lookup"><span data-stu-id="1ff64-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="1ff64-113">Per impostare la proprietà, passare un puntatore **IPropertyStore** al *resolver di origine*.</span><span class="sxs-lookup"><span data-stu-id="1ff64-113">To set the property, pass an **IPropertyStore** pointer to the *source resolver*.</span></span> <span data-ttu-id="1ff64-114">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="1ff64-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="1ff64-115">La *ricerca iterativa* è un algoritmo per trovare una posizione in un file ASF senza indice.</span><span class="sxs-lookup"><span data-stu-id="1ff64-115">*Iterative seeking* is an algorithm to find a position in an ASF file with no index.</span></span> <span data-ttu-id="1ff64-116">Usa una serie di approssimazioni, in base alla velocità in bit media, per avvicinarsi progressivamente al tempo di ricerca di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1ff64-116">It uses a series of approximations, based on the average bit rate, to get progressively closer to the target seek time.</span></span> <span data-ttu-id="1ff64-117">L'algoritmo è simile a una ricerca binaria. La ricerca iterativa può richiedere più tempo della ricerca in base all'indice, quindi è disabilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1ff64-117">(The algorithm is similar to a binary search.) Iterative seeking can take longer than seeking by index, so it is disabled by default.</span></span>

<span data-ttu-id="1ff64-118">Se si imposta questa proprietà, utilizzare le proprietà seguenti per impostare i parametri di ricerca:</span><span class="sxs-lookup"><span data-stu-id="1ff64-118">If you set this property, use the following properties to set the search parameters:</span></span>

-   [<span data-ttu-id="1ff64-119">Numero massimo di MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ff64-119">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count</span></span>](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [<span data-ttu-id="1ff64-120">\_ \_ Tolleranza ITERATIVESEEK ASFMediaSource \_ MFPKEY \_ in \_ millisecondi</span><span class="sxs-lookup"><span data-stu-id="1ff64-120">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond</span></span>](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

<span data-ttu-id="1ff64-121">Queste proprietà impostano rispettivamente il numero massimo di iterazioni e la tolleranza.</span><span class="sxs-lookup"><span data-stu-id="1ff64-121">These properties set the maximum number of iterations and the tolerance, respectively.</span></span> <span data-ttu-id="1ff64-122">L'algoritmo si interrompe quando raggiunge il numero massimo di iterazioni oppure quando trova un pacchetto la cui distanza dal tempo di ricerca rientra nella tolleranza specificata.</span><span class="sxs-lookup"><span data-stu-id="1ff64-122">The algorithm halts when it reaches the maximum number of iterations, or when it finds a packet whose distance from the seek time is within the specified tolerance.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff64-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ff64-123">Requirements</span></span>



| <span data-ttu-id="1ff64-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ff64-124">Requirement</span></span> | <span data-ttu-id="1ff64-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1ff64-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff64-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ff64-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1ff64-127">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1ff64-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1ff64-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ff64-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1ff64-129">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1ff64-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1ff64-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ff64-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ff64-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ff64-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff64-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ff64-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff64-133">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ff64-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




