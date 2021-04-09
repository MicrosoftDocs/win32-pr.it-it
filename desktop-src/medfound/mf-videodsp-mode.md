---
description: Imposta la modalità di elaborazione del Stabilizzazione video MFT.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: Attributo MF_VIDEODSP_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130127"
---
# <a name="mf_videodsp_mode-attribute"></a><span data-ttu-id="c47a5-103">\_ \_ Attributo modalità MF VIDEODSP</span><span class="sxs-lookup"><span data-stu-id="c47a5-103">MF\_VIDEODSP\_MODE attribute</span></span>

<span data-ttu-id="c47a5-104">Imposta la modalità di elaborazione del [**stabilizzazione video MFT**](video-stabilization-mft.md).</span><span class="sxs-lookup"><span data-stu-id="c47a5-104">Sets the processing mode of the [**Video Stabilization MFT**](video-stabilization-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="c47a5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c47a5-105">Data type</span></span>

<span data-ttu-id="c47a5-106">**MFVideoDSPMode** archiviato come **UIINT32**</span><span class="sxs-lookup"><span data-stu-id="c47a5-106">**MFVideoDSPMode** stored as **UIINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c47a5-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c47a5-107">Remarks</span></span>

<span data-ttu-id="c47a5-108">Il valore di questo attributo è un valore di enumerazione [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) .</span><span class="sxs-lookup"><span data-stu-id="c47a5-108">The value of this attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="c47a5-109">Questo attributo può essere usato per abilitare o disabilitare la stabilizzazione dell'immagine e può essere aggiornato per ogni esempio di output.</span><span class="sxs-lookup"><span data-stu-id="c47a5-109">This attribute can be used to enable or disable the image stabilization, and can be updated for each output sample.</span></span>

<span data-ttu-id="c47a5-110">Per impostare l'attributo:</span><span class="sxs-lookup"><span data-stu-id="c47a5-110">To set this attribute:</span></span>

1.  <span data-ttu-id="c47a5-111">Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sulla MFT per la stabilizzazione video per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="c47a5-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video stabilization MFT to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="c47a5-112">Chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) SetAttribute per impostare l'attributo.</span><span class="sxs-lookup"><span data-stu-id="c47a5-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="c47a5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c47a5-113">Requirements</span></span>



| <span data-ttu-id="c47a5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c47a5-114">Requirement</span></span> | <span data-ttu-id="c47a5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c47a5-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c47a5-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c47a5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c47a5-117">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c47a5-117">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c47a5-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c47a5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c47a5-119">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c47a5-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c47a5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c47a5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c47a5-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c47a5-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c47a5-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c47a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c47a5-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c47a5-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c47a5-124">**Stabilizzazione video MFT**</span><span class="sxs-lookup"><span data-stu-id="c47a5-124">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




