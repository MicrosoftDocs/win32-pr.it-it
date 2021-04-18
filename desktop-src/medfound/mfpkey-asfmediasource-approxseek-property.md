---
description: Specifica se l'origine multimediale ASF utilizza la ricerca approssimativa.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: Proprietà MFPKEY_ASFMediaSource_ApproxSeek (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320749"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a><span data-ttu-id="05e95-103">MFPKEY \_ ASFMediaSource- \_ Proprietà ApproxSeek</span><span class="sxs-lookup"><span data-stu-id="05e95-103">MFPKEY\_ASFMediaSource\_ApproxSeek property</span></span>

<span data-ttu-id="05e95-104">Specifica se l'origine multimediale ASF utilizza la ricerca approssimativa.</span><span class="sxs-lookup"><span data-stu-id="05e95-104">Specifies whether the ASF media source uses approximate seeking.</span></span>



<span data-ttu-id="05e95-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="05e95-105">Data type</span></span>

<span data-ttu-id="05e95-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="05e95-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="05e95-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="05e95-107">PROPVARIANT member</span></span>

<span data-ttu-id="05e95-108">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="05e95-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="05e95-109">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="05e95-109">VT\_BOOL</span></span>

<span data-ttu-id="05e95-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="05e95-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="05e95-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="05e95-111">Remarks</span></span>

<span data-ttu-id="05e95-112">Le applicazioni possono usare questa proprietà per configurare l'origine dei supporti ASF.</span><span class="sxs-lookup"><span data-stu-id="05e95-112">Applications can use this property to configure the ASF media source.</span></span> <span data-ttu-id="05e95-113">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="05e95-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="05e95-114">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="05e95-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="05e95-115">L'origine dei supporti ASF gestisce la ricerca come segue:</span><span class="sxs-lookup"><span data-stu-id="05e95-115">The ASF media source handles seeking as follows:</span></span>

-   <span data-ttu-id="05e95-116">Se il valore di questa proprietà è **Variant \_ true**, l'origine multimediale usa la ricerca approssimativa, che è meno accurata ma più veloce rispetto alla ricerca esatta.</span><span class="sxs-lookup"><span data-stu-id="05e95-116">If the value of this property is **VARIANT\_TRUE**, the media source uses approximate seeking, which is less accurate but faster than exact seeking.</span></span>
-   <span data-ttu-id="05e95-117">Se il valore è **Variant \_ false** e il file ASF include un indice, l'origine multimediale usa la ricerca esatta.</span><span class="sxs-lookup"><span data-stu-id="05e95-117">If the value is **VARIANT\_FALSE** and the ASF file has an index, the media source uses exact seeking.</span></span>
-   <span data-ttu-id="05e95-118">Se il file ASF non contiene un indice, l'origine multimediale USA approxmate seeking a meno che la proprietà [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) non sia impostata su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="05e95-118">If the ASF file does not contain an index, the media source uses approxmate seeking unless the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is set to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="05e95-119">Se il file ASF non contiene un indice e la proprietà [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) è **Variant \_ true**, l'origine multimediale usa la ricerca iterativa.</span><span class="sxs-lookup"><span data-stu-id="05e95-119">If the ASF file does not contain an index and the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is **VARIANT\_TRUE**, the media source uses iterative seeking.</span></span> <span data-ttu-id="05e95-120">La ricerca iterativa è più precisa ma più lenta rispetto alla ricerca approssimativa, ma in genere meno accurata della ricerca esatta.</span><span class="sxs-lookup"><span data-stu-id="05e95-120">Iterative seeking is more accurate but slower than approximate seeking (but generally less accurate than exact seeking).</span></span>
    > [!Note]  
    > <span data-ttu-id="05e95-121">Richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="05e95-121">Requires Windows 7.</span></span>

     

<span data-ttu-id="05e95-122">Il valore predefinito di questa proprietà è **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="05e95-122">The default value of this property is **VARIANT\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="05e95-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05e95-123">Requirements</span></span>



| <span data-ttu-id="05e95-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="05e95-124">Requirement</span></span> | <span data-ttu-id="05e95-125">Valore</span><span class="sxs-lookup"><span data-stu-id="05e95-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05e95-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05e95-126">Minimum supported client</span></span><br/> | <span data-ttu-id="05e95-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05e95-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="05e95-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05e95-128">Minimum supported server</span></span><br/> | <span data-ttu-id="05e95-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05e95-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="05e95-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05e95-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="05e95-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="05e95-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05e95-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05e95-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05e95-133">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05e95-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




