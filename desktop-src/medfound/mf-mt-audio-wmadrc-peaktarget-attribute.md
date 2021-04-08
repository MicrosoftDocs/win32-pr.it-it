---
description: Livello di picco del volume di destinazione di un file di Windows Media Audio.
ms.assetid: 73f4e763-dcb7-48cd-ab80-37635d973da0
title: Attributo MF_MT_AUDIO_WMADRC_PEAKTARGET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48391adfaa19dcc00ea4d7a30b909b4573f67222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968165"
---
# <a name="mf_mt_audio_wmadrc_peaktarget-attribute"></a><span data-ttu-id="26678-103">\_Attributo PEAKTARGET di MF mt \_ audio \_ WMADRC \_</span><span class="sxs-lookup"><span data-stu-id="26678-103">MF\_MT\_AUDIO\_WMADRC\_PEAKTARGET attribute</span></span>

<span data-ttu-id="26678-104">Livello di picco del volume di destinazione di un file di Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="26678-104">Target peak volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="26678-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="26678-105">Data type</span></span>

<span data-ttu-id="26678-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="26678-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="26678-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="26678-107">Remarks</span></span>

<span data-ttu-id="26678-108">Questo attributo si applica ai tipi di supporti audio per Windows Media Audio codec.</span><span class="sxs-lookup"><span data-stu-id="26678-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="26678-109">Specifica il livello di picco del volume di destinazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="26678-109">It specifies the target peak volume level of the content.</span></span> <span data-ttu-id="26678-110">Il decodificatore può usare questo valore per eseguire il controllo dinamico degli intervalli.</span><span class="sxs-lookup"><span data-stu-id="26678-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="26678-111">Il metodo [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) aggiunge questo attributo al tipo di supporto se l'intestazione ASF contiene l'attributo [**WM/WMADRCPeakTarget**](../wmformat/wm-wmadrcpeaktarget.md) .</span><span class="sxs-lookup"><span data-stu-id="26678-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCPeakTarget**](../wmformat/wm-wmadrcpeaktarget.md) attribute.</span></span> <span data-ttu-id="26678-112">Questo attributo è descritto nella documentazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="26678-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="26678-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="26678-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="26678-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26678-114">Requirements</span></span>



| <span data-ttu-id="26678-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="26678-115">Requirement</span></span> | <span data-ttu-id="26678-116">Valore</span><span class="sxs-lookup"><span data-stu-id="26678-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26678-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26678-117">Minimum supported client</span></span><br/> | <span data-ttu-id="26678-118">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="26678-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="26678-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26678-119">Minimum supported server</span></span><br/> | <span data-ttu-id="26678-120">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="26678-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="26678-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26678-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="26678-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="26678-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26678-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26678-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26678-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26678-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="26678-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="26678-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="26678-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="26678-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="26678-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="26678-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="26678-128">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="26678-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
