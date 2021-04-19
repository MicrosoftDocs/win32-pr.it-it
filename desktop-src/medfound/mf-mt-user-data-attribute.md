---
description: Contiene dati di formato aggiuntivi per un tipo di supporto.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: Attributo MF_MT_USER_DATA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6042ded0e2d441b0f86c5e1f97557959ce08cd1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316444"
---
# <a name="mf_mt_user_data-attribute"></a><span data-ttu-id="2ab7a-103">\_ \_ Attributo dati utente MF mt \_</span><span class="sxs-lookup"><span data-stu-id="2ab7a-103">MF\_MT\_USER\_DATA attribute</span></span>

<span data-ttu-id="2ab7a-104">Contiene dati di formato aggiuntivi per un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-104">Contains additional format data for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="2ab7a-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2ab7a-105">Data type</span></span>

<span data-ttu-id="2ab7a-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="2ab7a-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="2ab7a-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ab7a-107">Remarks</span></span>

<span data-ttu-id="2ab7a-108">Il significato dei dati in questo attributo dipende dal formato descritto dal tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-108">The meaning of the data in this attribute depends on the format that is described by the media type.</span></span>



| <span data-ttu-id="2ab7a-109">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="2ab7a-109">Format Type</span></span>                                                                                                           | <span data-ttu-id="2ab7a-110">Dati di formato aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="2ab7a-110">Additional Format Data</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab7a-111">Codec Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-111">Windows Media codec.</span></span>                                                                                                  | <span data-ttu-id="2ab7a-112">Dati privati di codec.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-112">Codec private data.</span></span>                                                                                                                       |
| <span data-ttu-id="2ab7a-113">La struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) è stata convertita.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-113">Converted [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span>   | <span data-ttu-id="2ab7a-114">Dati aggiuntivi visualizzati dopo la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , esclusa la tabella dei colori o le maschere colori.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-114">Extra data that appears after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, not including the color table or color masks.</span></span> |
| <span data-ttu-id="2ab7a-115">La struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) o [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) è stata convertita.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-115">Converted [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> | <span data-ttu-id="2ab7a-116">Dati aggiuntivi visualizzati dopo la struttura del formato audio.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-116">Extra data that appears after the audio format structure.</span></span>                                                                                 |



 

<span data-ttu-id="2ab7a-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab7a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ab7a-118">Requirements</span></span>



| <span data-ttu-id="2ab7a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ab7a-119">Requirement</span></span> | <span data-ttu-id="2ab7a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2ab7a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab7a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ab7a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2ab7a-122">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2ab7a-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2ab7a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ab7a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2ab7a-124">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="2ab7a-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2ab7a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ab7a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ab7a-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ab7a-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ab7a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ab7a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab7a-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2ab7a-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2ab7a-129">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="2ab7a-129">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="2ab7a-130">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="2ab7a-130">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="2ab7a-131">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2ab7a-131">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2ab7a-132">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="2ab7a-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
