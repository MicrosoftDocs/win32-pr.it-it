---
description: Specifica i tipi di frame (I, P o B) a cui viene applicato il parametro di quantizzazione (QP).
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: Proprietà CODECAPI_AVEncVideoEncodeFrameTypeQP (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127975"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a><span data-ttu-id="e7ba9-103">Proprietà AVEncVideoEncodeFrameTypeQP di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="e7ba9-103">CODECAPI\_AVEncVideoEncodeFrameTypeQP property</span></span>

<span data-ttu-id="e7ba9-104">Specifica i tipi di frame (I, P o B) a cui viene applicato il parametro di quantizzazione (QP).</span><span class="sxs-lookup"><span data-stu-id="e7ba9-104">Specifies the frame types (I, P, or B) that the quantization parameter (QP) is applied to.</span></span>

## <a name="data-type"></a><span data-ttu-id="e7ba9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e7ba9-105">Data type</span></span>

<span data-ttu-id="e7ba9-106">**ULONGULONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="e7ba9-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e7ba9-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="e7ba9-107">Property GUID</span></span>

<span data-ttu-id="e7ba9-108">**Codecapis \_ AVEncVideoEncodeFrameTypeQP**</span><span class="sxs-lookup"><span data-stu-id="e7ba9-108">**CODECAPI\_AVEncVideoEncodeFrameTypeQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ba9-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7ba9-109">Remarks</span></span>

<span data-ttu-id="e7ba9-110">Per i codificatori che supportano l'impostazione di un parametro di quantizzazione (QP) per diversi tipi di frame (I, P, B), devono esporre questa API oltre a [CODEcapite \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md).</span><span class="sxs-lookup"><span data-stu-id="e7ba9-110">For encoders which support setting a quantization parameter (QP) for different frame types (I, P, B), they shall expose this API in addition to [CODECAPI\_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md).</span></span> <span data-ttu-id="e7ba9-111">Se un codificatore supporta solo un singolo QP per tutti i tipi di frame, dovrà supportare solo codecapite \_ AVEncVideoEncodeQP.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-111">If an encoder supports only a single QP for all frame types, they shall support only CODECAPI\_AVEncVideoEncodeQP.</span></span>

<span data-ttu-id="e7ba9-112">Si tratta di una proprietà di codifica dinamica che indica che è possibile impostare un nuovo valore in qualsiasi momento durante la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-112">This is a dynamic encoding property meaning that a new value can be set any time during the encoding session.</span></span>

<span data-ttu-id="e7ba9-113">**Codificatori H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="e7ba9-113">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="e7ba9-114">Il codificatore deve supportare [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="e7ba9-114">Encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="e7ba9-115">Un set di campi a 4 16 bit viene usato per specificare il frame query al secondo nella codifica Fixed-QP.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-115">A set of four 16-bit fields are used to specify the frame QPs in fixed-QP encoding.</span></span> <span data-ttu-id="e7ba9-116">I campi sono:</span><span class="sxs-lookup"><span data-stu-id="e7ba9-116">The fields are:</span></span>

-   <span data-ttu-id="e7ba9-117">**Bits 0-15:** QP usato per I frame I, intervallo valido \[ 0, 51 \] .</span><span class="sxs-lookup"><span data-stu-id="e7ba9-117">**Bits 0-15:** QP used for I frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="e7ba9-118">**Bits 16-31:** QP usato per i frame P, intervallo valido \[ 0, 51 \] .</span><span class="sxs-lookup"><span data-stu-id="e7ba9-118">**Bits 16-31:** QP used for P frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="e7ba9-119">**Bits 32-47:** QP utilizzato per i frame B, intervallo valido \[ 0, 51\]</span><span class="sxs-lookup"><span data-stu-id="e7ba9-119">**Bits 32-47:** QP used for B frames, valid range \[0, 51\]</span></span>
-   <span data-ttu-id="e7ba9-120">**Bits 48-63:** riservato</span><span class="sxs-lookup"><span data-stu-id="e7ba9-120">**Bits 48-63:** reserved</span></span>

<span data-ttu-id="e7ba9-121">Quando questo codecapi è supportato, I codificatori supporteranno le impostazioni di QP per il tipo di frame I, P e B.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-121">When this CodecAPI is supported, encoders shall support QP setting on frame type of I, P, and B.</span></span>

<span data-ttu-id="e7ba9-122">Il valore predefinito deve essere 0x0000001a001a001a.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-122">Default value shall be 0x0000001a001a001a.</span></span> <span data-ttu-id="e7ba9-123">QP uguale a 26 per I, P e B.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-123">QP equal to 26 for I, P and B.</span></span>

<span data-ttu-id="e7ba9-124">Quando [CODEcapites \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) seleziona un livello temporale specifico, il [**valore**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) di codecapites \_ AVEncVideoEncodeFrameTypeQP imposta QP per i frame I, P e B su tale livello temporale.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-124">When [CODECAPI\_AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) selects a specific temporal layer, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) of CODECAPI\_AVEncVideoEncodeFrameTypeQP shall set QP for I, P, and B frames on that temporal layer.</span></span> <span data-ttu-id="e7ba9-125">Per impostazione predefinita, imposta la query QP per I frame I, P e B sul livello temporale di base livello temporale 0.</span><span class="sxs-lookup"><span data-stu-id="e7ba9-125">By default, it sets QP for I, P, and B frames on base temporal layer temporal layer 0.</span></span>

<span data-ttu-id="e7ba9-126">[CODEcapi \_ ](codecapi-avencvideomaxqp.md)Per definire e limitare l'intervallo di QP per query al secondo di tutti i tipi di immagine, i, P e B, è necessario usare AVEncVideoMaxQP e [codecapit \_ AVEncVideoMinQP](codecapi-avencvideominqp.md)</span><span class="sxs-lookup"><span data-stu-id="e7ba9-126">[CODECAPI\_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) and [CODECAPI\_AVEncVideoMinQP](codecapi-avencvideominqp.md) shall be used to define and limit the QP range for QPs of all picture types, I, P and B.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ba9-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7ba9-127">Requirements</span></span>



| <span data-ttu-id="e7ba9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7ba9-128">Requirement</span></span> | <span data-ttu-id="e7ba9-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e7ba9-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ba9-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7ba9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ba9-131">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e7ba9-131">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="e7ba9-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7ba9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ba9-133">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e7ba9-133">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e7ba9-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7ba9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7ba9-135"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7ba9-135"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7ba9-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7ba9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ba9-137">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7ba9-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

