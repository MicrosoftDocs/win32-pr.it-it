---
description: Riferimento a livello di picco del volume di un file di Windows Media Audio.
ms.assetid: bb762f9c-cf08-4d32-991e-490eb7b1f579
title: Attributo MF_MT_AUDIO_WMADRC_PEAKREF (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0074046c79f532a4b63472f8ec22b588b2c4020a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528242"
---
# <a name="mf_mt_audio_wmadrc_peakref-attribute"></a><span data-ttu-id="6cf6e-103">\_Attributo PEAKREF di MF mt \_ audio \_ WMADRC \_</span><span class="sxs-lookup"><span data-stu-id="6cf6e-103">MF\_MT\_AUDIO\_WMADRC\_PEAKREF attribute</span></span>

<span data-ttu-id="6cf6e-104">Riferimento a livello di picco del volume di un file di Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-104">Reference peak volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="6cf6e-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6cf6e-105">Data type</span></span>

<span data-ttu-id="6cf6e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6cf6e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6cf6e-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="6cf6e-107">Remarks</span></span>

<span data-ttu-id="6cf6e-108">Questo attributo si applica ai tipi di supporti audio per Windows Media Audio codec.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="6cf6e-109">Specifica il livello del volume di picco originale del contenuto.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-109">It specifies the original peak volume level of the content.</span></span> <span data-ttu-id="6cf6e-110">Il decodificatore può usare questo valore per eseguire il controllo dinamico degli intervalli.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="6cf6e-111">Il metodo [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) aggiunge questo attributo al tipo di supporto se l'intestazione ASF contiene l'attributo [**WM/WMADRCPeakReference**](../wmformat/wm-wmadrcpeakreference.md) .</span><span class="sxs-lookup"><span data-stu-id="6cf6e-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCPeakReference**](../wmformat/wm-wmadrcpeakreference.md) attribute.</span></span> <span data-ttu-id="6cf6e-112">Questo attributo è descritto nella documentazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="6cf6e-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf6e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6cf6e-114">Requirements</span></span>



| <span data-ttu-id="6cf6e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cf6e-115">Requirement</span></span> | <span data-ttu-id="6cf6e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6cf6e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf6e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cf6e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf6e-118">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6cf6e-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6cf6e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cf6e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf6e-120">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="6cf6e-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6cf6e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6cf6e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cf6e-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cf6e-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf6e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6cf6e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf6e-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6cf6e-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6cf6e-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="6cf6e-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6cf6e-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="6cf6e-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6cf6e-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6cf6e-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6cf6e-128">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="6cf6e-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
