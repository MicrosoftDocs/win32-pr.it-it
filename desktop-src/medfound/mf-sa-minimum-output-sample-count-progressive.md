---
description: Indica il numero minimo di campioni progressivi che la trasformazione Microsoft Media Foundation (MFT) deve consentire di oustanding in un determinato momento.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: Attributo MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232381"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a><span data-ttu-id="ad313-103">\_ \_ \_ \_ \_ \_ Attributo progressivo numero minimo di output sa di MF</span><span class="sxs-lookup"><span data-stu-id="ad313-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT\_PROGRESSIVE attribute</span></span>

<span data-ttu-id="ad313-104">Indica il numero minimo di campioni progressivi che la trasformazione Microsoft Media Foundation (MFT) deve consentire di oustanding in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="ad313-104">Indicates the minimum number of progressive samples that the Microsoft Media Foundation transform (MFT) should allow to be oustanding at any given time.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad313-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ad313-105">Data type</span></span>

<span data-ttu-id="ad313-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ad313-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ad313-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad313-107">Remarks</span></span>

<span data-ttu-id="ad313-108">Questo attributo si applica solo a MFTs che usano un buffer circolare per allocare i propri esempi di output.</span><span class="sxs-lookup"><span data-stu-id="ad313-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="ad313-109">Altri MFTs ignorano questo attributo.</span><span class="sxs-lookup"><span data-stu-id="ad313-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="ad313-110">Per impostare l'attributo:</span><span class="sxs-lookup"><span data-stu-id="ad313-110">To set this attribute:</span></span>

1.  <span data-ttu-id="ad313-111">Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) nel decodificatore per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="ad313-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="ad313-112">Chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) SetAttribute per aggiungere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="ad313-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad313-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad313-113">Requirements</span></span>



| <span data-ttu-id="ad313-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad313-114">Requirement</span></span> | <span data-ttu-id="ad313-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ad313-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad313-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad313-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ad313-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ad313-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ad313-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad313-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ad313-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="ad313-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ad313-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad313-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad313-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad313-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad313-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad313-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad313-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad313-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




