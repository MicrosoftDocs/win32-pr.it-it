---
description: Specifica i limiti dell'area di interesse, che indica l'area del frame che richiede una qualità diversa.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: Attributo MFSampleExtension_ROIRectangle (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310233"
---
# <a name="mfsampleextension_roirectangle-attribute"></a><span data-ttu-id="b0ca9-103">\_Attributo ROIRectangle di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="b0ca9-103">MFSampleExtension\_ROIRectangle attribute</span></span>

<span data-ttu-id="b0ca9-104">Specifica i limiti dell'area di interesse, che indica l'area del frame che richiede una qualità diversa.</span><span class="sxs-lookup"><span data-stu-id="b0ca9-104">Specifies the bounds of the region of interest which indicates the region of the frame that requires different quality.</span></span>

## <a name="data-type"></a><span data-ttu-id="b0ca9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b0ca9-105">Data type</span></span>

<span data-ttu-id="b0ca9-106">**[**ROI \_ AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** archiviata come **BLOB**</span><span class="sxs-lookup"><span data-stu-id="b0ca9-106">**[**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** stored as **BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="b0ca9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0ca9-107">Remarks</span></span>

<span data-ttu-id="b0ca9-108">Dopo aver impostato correttamente [CODEcapis \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) su un valore diverso da zero in un codificatore MFT, l'applicazione può impostare questo attributo sugli esempi di input e aspettarsi che venga rispettato.</span><span class="sxs-lookup"><span data-stu-id="b0ca9-108">After successfully setting [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) to a non-zero value on an encoder MFT, the application can set this attribute on input samples and expect it to be honored.</span></span>

<span data-ttu-id="b0ca9-109">Se [CODEcapis \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) non è impostato su un valore diverso da zero, l' \_ attributo MFSampleExtension ROIRectangle viene ignorato negli esempi di input.</span><span class="sxs-lookup"><span data-stu-id="b0ca9-109">If [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) is not set to a non-zero value, the MFSampleExtension\_ROIRectangle attribute is ignored on input samples.</span></span>

<span data-ttu-id="b0ca9-110">MFSampleExtension \_ ROIRectangle è impostato su un esempio di input e viene applicato solo all'esempio di input corrente.</span><span class="sxs-lookup"><span data-stu-id="b0ca9-110">MFSampleExtension\_ROIRectangle is set on an input sample and is only applied to the current input sample.</span></span>

<span data-ttu-id="b0ca9-111">Il campo **QPDelta** nella struttura [**dell' \_ area del ROI**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) specifica il Delta del parametro di quantizzazione per l'area specificata dal resto del frame.</span><span class="sxs-lookup"><span data-stu-id="b0ca9-111">The **QPDelta** field on the [**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) structure specifies the quantization parameter delta for the specified region from the rest of the frame.</span></span> <span data-ttu-id="b0ca9-112">Se **QPDelta** è un valore positivo, significa che l'applicazione desidera che il rettangolo abbia una qualità inferiore rispetto al resto del frame.</span><span class="sxs-lookup"><span data-stu-id="b0ca9-112">If **QPDelta** is positive, this indicates the application wants the rectangle to have lower quality than the rest of the frame.</span></span>

<span data-ttu-id="b0ca9-113">**Codificatori H. 264/AVC:** **QPDelta** deve essere compreso tra \[ -25, + 25 \] .</span><span class="sxs-lookup"><span data-stu-id="b0ca9-113">**H.264/AVC encoders:** **QPDelta** shall be between \[-25, +25\].</span></span> <span data-ttu-id="b0ca9-114">Il codificatore deve garantire che la versione QP finale sia in un intervallo valido per il video standard.</span><span class="sxs-lookup"><span data-stu-id="b0ca9-114">The encoder shall ensure that the final QP is in a valid range for the video standard.</span></span>

<span data-ttu-id="b0ca9-115">Non è necessario che l'area specificata sia MB allineata.</span><span class="sxs-lookup"><span data-stu-id="b0ca9-115">The specified region is not required to be MB aligned.</span></span> <span data-ttu-id="b0ca9-116">I codificatori hanno la possibilità di decidere il limite effettivo.</span><span class="sxs-lookup"><span data-stu-id="b0ca9-116">Encoders have flexibility to decide the actual boundary.</span></span> <span data-ttu-id="b0ca9-117">Si consiglia di coprire l'intera area specificata.</span><span class="sxs-lookup"><span data-stu-id="b0ca9-117">It is recommended to cover the entire specified region.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0ca9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0ca9-118">Requirements</span></span>



| <span data-ttu-id="b0ca9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0ca9-119">Requirement</span></span> | <span data-ttu-id="b0ca9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b0ca9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ca9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0ca9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b0ca9-122">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b0ca9-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="b0ca9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0ca9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b0ca9-124">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b0ca9-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b0ca9-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0ca9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0ca9-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0ca9-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0ca9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0ca9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0ca9-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0ca9-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




