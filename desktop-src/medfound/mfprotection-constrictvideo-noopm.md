---
description: Questo attributo specifica una protezione aggiuntiva offerta da un'autorità di attendibilità video output quando un connettore non offre la protezione dell'output.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: Attributo MFPROTECTION_CONSTRICTVIDEO_NOOPM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966993"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a><span data-ttu-id="061a9-103">MFPROTECTION \_ CONSTRICTVIDEO- \_ attributo NOOPM</span><span class="sxs-lookup"><span data-stu-id="061a9-103">MFPROTECTION\_CONSTRICTVIDEO\_NOOPM attribute</span></span>

<span data-ttu-id="061a9-104">Questo attributo specifica una protezione aggiuntiva offerta da un'autorità di attendibilità video output quando un connettore non offre la protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="061a9-104">This attribute specifies additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="061a9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="061a9-105">Data type</span></span>

<span data-ttu-id="061a9-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="061a9-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="061a9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="061a9-107">Remarks</span></span>

<span data-ttu-id="061a9-108">Si tratta di una protezione aggiuntiva offerta da un servizio OTA (video output Trust Authority) quando un connettore non offre la protezione dell'output (vedere [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span><span class="sxs-lookup"><span data-stu-id="061a9-108">This is an additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection (see [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span></span> <span data-ttu-id="061a9-109">In questo caso, l'OTA può offrire questa protezione il cui effetto è identico a quello di [MFPROTECTION \_ CONSTRICTVIDEO](mfprotection-constrictvideo.md) Protection.</span><span class="sxs-lookup"><span data-stu-id="061a9-109">In this case the OTA may offer this protection whose effect is the same as the [MFPROTECTION\_CONSTRICTVIDEO](mfprotection-constrictvideo.md) protection.</span></span> <span data-ttu-id="061a9-110">Questa operazione viene definita per evitare confusione con le chiamate precedenti a [**IMFOutputPolicy:: GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interazioni in cui \_ è stata usata la protezione MFPROTECTION CONSTRICTVIDEO per identificare lo pseudo-connettore Desktop Window Manager.</span><span class="sxs-lookup"><span data-stu-id="061a9-110">This is defined to avoid confusion with previous calls to [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interactions where the presence of MFPROTECTION\_CONSTRICTVIDEO protection was used to help identify the desktop window manager pseudo-connector.</span></span>

## <a name="requirements"></a><span data-ttu-id="061a9-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="061a9-111">Requirements</span></span>



| <span data-ttu-id="061a9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="061a9-112">Requirement</span></span> | <span data-ttu-id="061a9-113">Valore</span><span class="sxs-lookup"><span data-stu-id="061a9-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="061a9-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="061a9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="061a9-115">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="061a9-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="061a9-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="061a9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="061a9-117">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="061a9-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="061a9-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="061a9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="061a9-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="061a9-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="061a9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="061a9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061a9-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="061a9-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




