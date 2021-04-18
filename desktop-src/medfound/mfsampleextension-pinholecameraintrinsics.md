---
description: Contiene le funzioni intrinseche della fotocamera pinhole per l'esempio.
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: Attributo MFSampleExtension_PinholeCameraIntrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb9e78641c0baab0e9eda3083aafaf8fe92229f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310234"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a><span data-ttu-id="7ded6-103">\_Attributo PinholeCameraIntrinsics di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="7ded6-103">MFSampleExtension\_PinholeCameraIntrinsics attribute</span></span>

<span data-ttu-id="7ded6-104">Contiene le funzioni intrinseche della fotocamera pinhole per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="7ded6-104">Contains the pinhole camera intrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="7ded6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7ded6-105">Data type</span></span>

<span data-ttu-id="7ded6-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="7ded6-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="7ded6-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="7ded6-107">Get/set</span></span>

<span data-ttu-id="7ded6-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="7ded6-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="7ded6-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="7ded6-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="7ded6-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="7ded6-110">Applies to</span></span>

[<span data-ttu-id="7ded6-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="7ded6-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="7ded6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ded6-112">Remarks</span></span>

<span data-ttu-id="7ded6-113">Il valore dell'attributo è un [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span><span class="sxs-lookup"><span data-stu-id="7ded6-113">The value of the attribute is a [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span></span>

<span data-ttu-id="7ded6-114">Questo attributo è facoltativo per supportare le fotocamere non calibrate.</span><span class="sxs-lookup"><span data-stu-id="7ded6-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ded6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ded6-115">Requirements</span></span>



| <span data-ttu-id="7ded6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ded6-116">Requirement</span></span> | <span data-ttu-id="7ded6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7ded6-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ded6-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ded6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7ded6-119">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7ded6-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ded6-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ded6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7ded6-121">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ded6-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7ded6-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ded6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ded6-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ded6-123"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




