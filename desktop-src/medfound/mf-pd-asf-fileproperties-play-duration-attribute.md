---
description: Specifica il tempo necessario per riprodurre un file con estensione ASF (Advanced Systems Format), in unità da 100 nanosecondi.
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: Attributo MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac62dfbd86dfcbd001555343309568033787186b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967945"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a><span data-ttu-id="16555-103">\_ \_ \_ \_ Attributo Duration del gioco FileProperties ASF di MF PD \_</span><span class="sxs-lookup"><span data-stu-id="16555-103">MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION attribute</span></span>

<span data-ttu-id="16555-104">Specifica il tempo necessario per riprodurre un file con estensione ASF (Advanced Systems Format), in unità da 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="16555-104">Specifies the time needed to play an Advanced Systems Format (ASF) file, in 100-nanosecond units.</span></span>

<span data-ttu-id="16555-105">Questo valore include il tempo di preiscrizione.</span><span class="sxs-lookup"><span data-stu-id="16555-105">This value includes the preroll time.</span></span> <span data-ttu-id="16555-106">Per recuperare la durata effettiva della riproduzione, ottenere il valore dell'attributo [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="16555-106">To retrieve the actual playback duration, get the value of the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute.</span></span> <span data-ttu-id="16555-107">Tuttavia, se il valore di preroll è maggiore della durata della riproduzione, il valore di **MF \_ PD \_ Duration** è zero.</span><span class="sxs-lookup"><span data-stu-id="16555-107">However, if the preroll value is greater than the play duration, the value of **MF\_PD\_DURATION** is zero.</span></span>

## <a name="data-type"></a><span data-ttu-id="16555-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="16555-108">Data type</span></span>

<span data-ttu-id="16555-109">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="16555-109">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="16555-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="16555-110">Remarks</span></span>

<span data-ttu-id="16555-111">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="16555-111">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="16555-112">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="16555-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="examples"></a><span data-ttu-id="16555-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="16555-113">Examples</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



## <a name="requirements"></a><span data-ttu-id="16555-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16555-114">Requirements</span></span>



| <span data-ttu-id="16555-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="16555-115">Requirement</span></span> | <span data-ttu-id="16555-116">Valore</span><span class="sxs-lookup"><span data-stu-id="16555-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16555-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16555-117">Minimum supported client</span></span><br/> | <span data-ttu-id="16555-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16555-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="16555-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16555-119">Minimum supported server</span></span><br/> | <span data-ttu-id="16555-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16555-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="16555-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16555-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="16555-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="16555-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16555-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16555-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16555-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="16555-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="16555-125">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="16555-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="16555-126">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="16555-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="16555-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="16555-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="16555-128">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="16555-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="16555-129">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="16555-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="16555-130">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="16555-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




