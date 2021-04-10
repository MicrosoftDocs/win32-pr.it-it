---
description: Specifica le dimensioni del buffer utilizzato durante la codifica. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Proprietà AVEncCommonBufferSize (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125250"
---
# <a name="avenccommonbuffersize-property"></a><span data-ttu-id="8234a-104">Proprietà AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="8234a-104">AVEncCommonBufferSize property</span></span>

<span data-ttu-id="8234a-105">Specifica le dimensioni del buffer utilizzato durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="8234a-105">Specifies the size of the buffer used during encoding.</span></span> <span data-ttu-id="8234a-106">Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="8234a-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="8234a-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8234a-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8234a-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8234a-108">Data type</span></span>

<span data-ttu-id="8234a-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="8234a-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8234a-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="8234a-110">Property GUID</span></span>

<span data-ttu-id="8234a-111">**Codecapis \_ AVEncCommonBufferSize**</span><span class="sxs-lookup"><span data-stu-id="8234a-111">**CODECAPI\_AVEncCommonBufferSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="8234a-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8234a-112">Property value</span></span>

<span data-ttu-id="8234a-113">Questa proprietà ha un intervallo lineare di valori.</span><span class="sxs-lookup"><span data-stu-id="8234a-113">This property has a linear range of values.</span></span> <span data-ttu-id="8234a-114">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="8234a-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span> <span data-ttu-id="8234a-115">Gli intervalli di parametri non sono supportati per i codificatori della fotocamera H. 264 UVC 1,5.</span><span class="sxs-lookup"><span data-stu-id="8234a-115">Parameter ranges are not supported for H.264 UVC 1.5 camera encoders.</span></span>

## <a name="remarks"></a><span data-ttu-id="8234a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8234a-116">Remarks</span></span>

<span data-ttu-id="8234a-117">Per alcuni formati video, le dimensioni del buffer vengono specificate in bit e per altre vengono specificate in byte.</span><span class="sxs-lookup"><span data-stu-id="8234a-117">For some video formats the buffer size is specified in bits and for others it is specified in bytes.</span></span> <span data-ttu-id="8234a-118">Per informazioni specifiche, vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="8234a-118">See the remarks below for specific information.</span></span>

<span data-ttu-id="8234a-119">Per il video MPEG questa proprietà definisce la dimensione del buffer VBV (video buffer Verifier).</span><span class="sxs-lookup"><span data-stu-id="8234a-119">For MPEG video, this property defines the video buffer verifier (VBV) buffer size.</span></span> <span data-ttu-id="8234a-120">Le dimensioni del buffer sono in bit.</span><span class="sxs-lookup"><span data-stu-id="8234a-120">The size of the buffer is in bits.</span></span>

<span data-ttu-id="8234a-121">Per il video e la Windows Media Video H. 264, la proprietà definisce la dimensione del decodificatore di riferimento ipotetico (HRD).</span><span class="sxs-lookup"><span data-stu-id="8234a-121">For H.264 video and Windows Media Video, the property defines the hypothetical reference decoder (HRD) size.</span></span> <span data-ttu-id="8234a-122">Dimensioni del buffer in byte.</span><span class="sxs-lookup"><span data-stu-id="8234a-122">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="8234a-123">Per le fotocamere di codifica UVC 1,5 H264, il valore CPB inviato al codificatore della fotocamera deve essere allineato a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="8234a-123">For UVC 1.5 H264 encoding cameras, the CPB value sent to the camera encoder must be 16-bit aligned.</span></span> <span data-ttu-id="8234a-124">Dimensioni del buffer in byte.</span><span class="sxs-lookup"><span data-stu-id="8234a-124">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="8234a-125">Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="8234a-125">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="8234a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8234a-126">Requirements</span></span>



| <span data-ttu-id="8234a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8234a-127">Requirement</span></span> | <span data-ttu-id="8234a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8234a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8234a-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8234a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8234a-130">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="8234a-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8234a-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8234a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8234a-132">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8234a-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8234a-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8234a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8234a-134"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="8234a-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8234a-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8234a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8234a-136">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="8234a-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8234a-137">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8234a-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

