---
description: Contiene la fotocamera estrinseca per l'esempio.
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: Attributo MFSampleExtension_CameraExtrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3340f1ab84061fa00e12fa65960f1b2902690816
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309098"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a><span data-ttu-id="63945-103">\_Attributo CameraExtrinsics di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="63945-103">MFSampleExtension\_CameraExtrinsics attribute</span></span>

<span data-ttu-id="63945-104">Contiene la fotocamera estrinseca per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="63945-104">Contains the camera extrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="63945-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="63945-105">Data type</span></span>

<span data-ttu-id="63945-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="63945-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="63945-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="63945-107">Get/set</span></span>

<span data-ttu-id="63945-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="63945-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="63945-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="63945-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="63945-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="63945-110">Applies to</span></span>

[<span data-ttu-id="63945-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="63945-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="63945-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="63945-112">Remarks</span></span>

<span data-ttu-id="63945-113">Il valore dell'attributo è un [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span><span class="sxs-lookup"><span data-stu-id="63945-113">The value of the attribute is a [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span></span>

<span data-ttu-id="63945-114">Questo attributo è facoltativo per supportare le fotocamere non calibrate.</span><span class="sxs-lookup"><span data-stu-id="63945-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="63945-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63945-115">Requirements</span></span>



| <span data-ttu-id="63945-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="63945-116">Requirement</span></span> | <span data-ttu-id="63945-117">Valore</span><span class="sxs-lookup"><span data-stu-id="63945-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63945-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63945-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63945-119">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="63945-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63945-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63945-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63945-121">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="63945-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="63945-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63945-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="63945-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="63945-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63945-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63945-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63945-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63945-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




