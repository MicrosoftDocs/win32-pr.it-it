---
description: Specifica il numero massimo di campioni di output che una trasformazione Microsoft Media Foundation (MFT) sarà in attesa in qualsiasi momento nella pipeline.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: Attributo MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226378"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a><span data-ttu-id="207d2-103">Attributo per il \_ \_ conteggio di \_ esempio di output minimo \_ \_ di MF SA</span><span class="sxs-lookup"><span data-stu-id="207d2-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="207d2-104">Specifica il numero massimo di campioni di output che una trasformazione Microsoft Media Foundation (MFT) sarà in attesa in qualsiasi momento nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="207d2-104">Specifies the maximum number of output samples that a Microsoft Media Foundation transform (MFT) will have outstanding in the pipeline at any time.</span></span>

## <a name="data-type"></a><span data-ttu-id="207d2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="207d2-105">Data type</span></span>

<span data-ttu-id="207d2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="207d2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="207d2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="207d2-107">Remarks</span></span>

<span data-ttu-id="207d2-108">Questo attributo si applica solo a MFTs che usano un buffer circolare per allocare i propri esempi di output.</span><span class="sxs-lookup"><span data-stu-id="207d2-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="207d2-109">Altri MFTs ignorano questo attributo.</span><span class="sxs-lookup"><span data-stu-id="207d2-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="207d2-110">Per impostare l'attributo:</span><span class="sxs-lookup"><span data-stu-id="207d2-110">To set this attribute:</span></span>

1.  <span data-ttu-id="207d2-111">Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) nel decodificatore per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="207d2-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="207d2-112">Chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) SetAttribute per aggiungere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="207d2-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="207d2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="207d2-113">Requirements</span></span>



| <span data-ttu-id="207d2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="207d2-114">Requirement</span></span> | <span data-ttu-id="207d2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="207d2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="207d2-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="207d2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="207d2-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="207d2-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="207d2-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="207d2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="207d2-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="207d2-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="207d2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="207d2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="207d2-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="207d2-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="207d2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="207d2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="207d2-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="207d2-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="207d2-124">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="207d2-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




