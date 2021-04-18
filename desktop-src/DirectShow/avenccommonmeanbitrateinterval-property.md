---
description: Specifica l'intervallo di tempo in base al quale viene applicata la velocità in bit media. Questa proprietà viene utilizzata insieme alla proprietà AVEncCommonMeanBitRate.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Proprietà AVEncCommonMeanBitRateInterval (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482524"
---
# <a name="avenccommonmeanbitrateinterval-property"></a><span data-ttu-id="fc453-104">Proprietà AVEncCommonMeanBitRateInterval</span><span class="sxs-lookup"><span data-stu-id="fc453-104">AVEncCommonMeanBitRateInterval property</span></span>

<span data-ttu-id="fc453-105">Specifica l'intervallo di tempo in base al quale viene applicata la velocità in bit media.</span><span class="sxs-lookup"><span data-stu-id="fc453-105">Specifies the time interval over which the average bit rate applies.</span></span> <span data-ttu-id="fc453-106">Questa proprietà viene utilizzata insieme alla proprietà [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="fc453-106">This property is used in conjunction with the [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property.</span></span>

<span data-ttu-id="fc453-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fc453-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fc453-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fc453-108">Data type</span></span>

<span data-ttu-id="fc453-109">**UInt64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="fc453-109">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fc453-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="fc453-110">Property GUID</span></span>

<span data-ttu-id="fc453-111">**Codecapis \_ AVEncCommonMeanBitRateInterval**</span><span class="sxs-lookup"><span data-stu-id="fc453-111">**CODECAPI\_AVEncCommonMeanBitRateInterval**</span></span>

## <a name="property-value"></a><span data-ttu-id="fc453-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fc453-112">Property value</span></span>

<span data-ttu-id="fc453-113">Questa proprietà ha un intervallo lineare di valori.</span><span class="sxs-lookup"><span data-stu-id="fc453-113">This property has a linear range of values.</span></span> <span data-ttu-id="fc453-114">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="fc453-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc453-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc453-115">Remarks</span></span>

<span data-ttu-id="fc453-116">Per la codifica con velocità in bit variabile (VBR) a due passaggi, il valore zero indica che l'intervallo di tempo è l'intera durata del contenuto.</span><span class="sxs-lookup"><span data-stu-id="fc453-116">For two-pass variable bit rate (VBR) encoding, the value zero indicates that the time interval is the entire duration of the content.</span></span> <span data-ttu-id="fc453-117">Per la codifica CBR (constant bit rate) a passaggio singolo, il valore zero indica che il codificatore seleziona l'intervallo (in genere 0,5 secondi).</span><span class="sxs-lookup"><span data-stu-id="fc453-117">For single-pass constant bit rate (CBR) encoding, the value zero indicates that the encoder selects the interval (typically 0.5 seconds).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc453-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc453-118">Requirements</span></span>



| <span data-ttu-id="fc453-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc453-119">Requirement</span></span> | <span data-ttu-id="fc453-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fc453-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc453-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc453-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fc453-122">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="fc453-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fc453-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc453-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fc453-124">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fc453-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fc453-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc453-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc453-126"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc453-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc453-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc453-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc453-128">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="fc453-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fc453-129">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fc453-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




