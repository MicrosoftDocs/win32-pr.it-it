---
description: Impone al codificatore di codificare il fotogramma successivo come fotogramma chiave.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: Proprietà CODECAPI_AVEncVideoForceKeyFrame (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305489"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a><span data-ttu-id="71eaf-103">Proprietà AVEncVideoForceKeyFrame di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="71eaf-103">CODECAPI\_AVEncVideoForceKeyFrame property</span></span>

<span data-ttu-id="71eaf-104">Impone al codificatore di codificare il fotogramma successivo come fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="71eaf-104">Forces the encoder to code the next frame as a key frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="71eaf-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="71eaf-105">Data type</span></span>

<span data-ttu-id="71eaf-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="71eaf-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="71eaf-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="71eaf-107">Property GUID</span></span>

<span data-ttu-id="71eaf-108">**Codecapis \_ AVEncVideoForceKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="71eaf-108">**CODECAPI\_AVEncVideoForceKeyFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="71eaf-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="71eaf-109">Property value</span></span>

<span data-ttu-id="71eaf-110">Se il valore è diverso da zero, il codificatore codifica il frame successivo come fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="71eaf-110">If the value is nonzero, the encoder will code the next frame as a key frame.</span></span> <span data-ttu-id="71eaf-111">Se il valore è zero, il codificatore seleziona se codificare il fotogramma successivo come fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="71eaf-111">If the value is zero, the encoder selects whether to encode the next frame as a key frame.</span></span>

<span data-ttu-id="71eaf-112">Questa proprietà si applica al frame successivo che il codificatore riceve come input.</span><span class="sxs-lookup"><span data-stu-id="71eaf-112">This property applies to the next frame that the encoder receives as input.</span></span> <span data-ttu-id="71eaf-113">Per un Media Foundation Transform (MFT), questo è il frame successivo passato al metodo [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) .</span><span class="sxs-lookup"><span data-stu-id="71eaf-113">For a Media Foundation transform (MFT), this is the next frame that is passed to the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method.</span></span> <span data-ttu-id="71eaf-114">L'impostazione viene reimpostata su zero dopo il frame successivo.</span><span class="sxs-lookup"><span data-stu-id="71eaf-114">The setting resets to zero after the next frame.</span></span>

## <a name="remarks"></a><span data-ttu-id="71eaf-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="71eaf-115">Remarks</span></span>

<span data-ttu-id="71eaf-116">Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="71eaf-116">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71eaf-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71eaf-117">Requirements</span></span>



| <span data-ttu-id="71eaf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="71eaf-118">Requirement</span></span> | <span data-ttu-id="71eaf-119">Valore</span><span class="sxs-lookup"><span data-stu-id="71eaf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71eaf-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71eaf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="71eaf-121">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="71eaf-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="71eaf-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71eaf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="71eaf-123">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="71eaf-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="71eaf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71eaf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="71eaf-125"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="71eaf-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71eaf-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71eaf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71eaf-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="71eaf-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="71eaf-128">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="71eaf-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

