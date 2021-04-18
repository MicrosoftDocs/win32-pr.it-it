---
description: Imposta il numero massimo di iterazioni di ricerca che l'origine multimediale ASF utilizzerà quando esegue la ricerca iterativa.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: Proprietà MFPKEY_ASFMediaSource_IterativeSeek_Max_Count (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320740"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a><span data-ttu-id="92454-103">\_Proprietà MFPKEY ASFMediaSource \_ IterativeSeek \_ Max \_ Count</span><span class="sxs-lookup"><span data-stu-id="92454-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count property</span></span>

<span data-ttu-id="92454-104">Imposta il numero massimo di iterazioni di ricerca che l'origine multimediale ASF utilizzerà quando esegue la ricerca iterativa.</span><span class="sxs-lookup"><span data-stu-id="92454-104">Sets the maximum number of search iterations the ASF media source will use when it performs iterative seeking.</span></span>



<span data-ttu-id="92454-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="92454-105">Data type</span></span>

<span data-ttu-id="92454-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="92454-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="92454-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="92454-107">PROPVARIANT member</span></span>

<span data-ttu-id="92454-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="92454-108">**ULONG**</span></span>

<span data-ttu-id="92454-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="92454-109">VT\_UI4</span></span>

<span data-ttu-id="92454-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="92454-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="92454-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="92454-111">Remarks</span></span>

<span data-ttu-id="92454-112">Usare questa proprietà per configurare l'origine del supporto ASF.</span><span class="sxs-lookup"><span data-stu-id="92454-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="92454-113">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="92454-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="92454-114">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="92454-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="92454-115">Questa proprietà si applica solo quando è abilitata la ricerca iterativa.</span><span class="sxs-lookup"><span data-stu-id="92454-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="92454-116">Per ulteriori informazioni, vedere [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="92454-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="92454-117">L'intervallo valido di questa proprietà è \[ 1-10 \] , inclusivo.</span><span class="sxs-lookup"><span data-stu-id="92454-117">The valid range of this property is \[1-10\], inclusive.</span></span> <span data-ttu-id="92454-118">Con un numero più elevato, la ricerca iterativa tende a essere più precisa, ma richiede più tempo.</span><span class="sxs-lookup"><span data-stu-id="92454-118">With a higher number, iterative seeking tends to be more accurate but takes longer.</span></span>

<span data-ttu-id="92454-119">Il valore predefinito è 5.</span><span class="sxs-lookup"><span data-stu-id="92454-119">The default value is 5.</span></span>

## <a name="requirements"></a><span data-ttu-id="92454-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92454-120">Requirements</span></span>



| <span data-ttu-id="92454-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="92454-121">Requirement</span></span> | <span data-ttu-id="92454-122">Valore</span><span class="sxs-lookup"><span data-stu-id="92454-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92454-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92454-123">Minimum supported client</span></span><br/> | <span data-ttu-id="92454-124">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="92454-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="92454-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92454-125">Minimum supported server</span></span><br/> | <span data-ttu-id="92454-126">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="92454-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="92454-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92454-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="92454-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92454-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92454-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92454-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92454-130">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92454-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




