---
description: Specifica la velocità in bit codificata media, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).
ms.assetid: 8519685a-4f5b-44af-ad46-09eba7a198c6
title: Proprietà AVEncCommonMeanBitRate (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4eaec7fc6578e6e69a45616ee6de059bb7a378b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522473"
---
# <a name="avenccommonmeanbitrate-property"></a><span data-ttu-id="f1e14-104">Proprietà AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="f1e14-104">AVEncCommonMeanBitRate property</span></span>

<span data-ttu-id="f1e14-105">Specifica la velocità in bit codificata media, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="f1e14-105">Specifies the average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="f1e14-106">Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="f1e14-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="f1e14-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f1e14-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="f1e14-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f1e14-108">Data type</span></span>

<span data-ttu-id="f1e14-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="f1e14-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f1e14-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="f1e14-110">Property GUID</span></span>

<span data-ttu-id="f1e14-111">**Codecapis \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="f1e14-111">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="f1e14-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f1e14-112">Property value</span></span>

<span data-ttu-id="f1e14-113">I codificatori possono implementare questa proprietà come un set enumerato o come intervallo lineare.</span><span class="sxs-lookup"><span data-stu-id="f1e14-113">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1e14-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1e14-114">Remarks</span></span>

<span data-ttu-id="f1e14-115">Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="f1e14-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e14-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1e14-116">Requirements</span></span>



| <span data-ttu-id="f1e14-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1e14-117">Requirement</span></span> | <span data-ttu-id="f1e14-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f1e14-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e14-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1e14-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e14-120">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="f1e14-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f1e14-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1e14-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e14-122">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f1e14-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f1e14-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1e14-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1e14-124"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1e14-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e14-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1e14-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e14-126">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="f1e14-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="f1e14-127">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="f1e14-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

