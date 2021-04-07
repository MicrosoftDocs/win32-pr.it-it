---
description: Specifica la velocità in bit media del flusso audio codificato, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).
ms.assetid: 9513ad64-2de9-497d-86ce-46cfdf87e0f8
title: Proprietà AVEncAudioMeanBitRate (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e311686e6113003593c8a6dbe02a9fca1f30b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049044"
---
# <a name="avencaudiomeanbitrate-property"></a><span data-ttu-id="b78f8-104">Proprietà AVEncAudioMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="b78f8-104">AVEncAudioMeanBitRate property</span></span>

<span data-ttu-id="b78f8-105">Specifica la velocità in bit media del flusso audio codificato, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="b78f8-105">Specifies the average bit rate of the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="b78f8-106">Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="b78f8-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="b78f8-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b78f8-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b78f8-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b78f8-108">Data type</span></span>

<span data-ttu-id="b78f8-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b78f8-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b78f8-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="b78f8-110">Property GUID</span></span>

<span data-ttu-id="b78f8-111">**Codecapis \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="b78f8-111">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="b78f8-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b78f8-112">Property value</span></span>

<span data-ttu-id="b78f8-113">I codificatori possono implementare questa proprietà come un set enumerato o come intervallo lineare.</span><span class="sxs-lookup"><span data-stu-id="b78f8-113">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="requirements"></a><span data-ttu-id="b78f8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b78f8-114">Requirements</span></span>



| <span data-ttu-id="b78f8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b78f8-115">Requirement</span></span> | <span data-ttu-id="b78f8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b78f8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b78f8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b78f8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b78f8-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="b78f8-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b78f8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b78f8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b78f8-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b78f8-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b78f8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b78f8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b78f8-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="b78f8-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b78f8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b78f8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78f8-124">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="b78f8-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b78f8-125">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="b78f8-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




