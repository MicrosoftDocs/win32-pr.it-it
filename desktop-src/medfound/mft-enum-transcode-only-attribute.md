---
description: Specifica se un decodificatore è ottimizzato per la transcodifica anziché per la riproduzione.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: Attributo MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401690"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a><span data-ttu-id="c433c-103">\_ \_ \_ Attributo attributo solo transcodifica dell'enumerazione MFT \_</span><span class="sxs-lookup"><span data-stu-id="c433c-103">MFT\_ENUM\_TRANSCODE\_ONLY\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="c433c-104">Specifica se un decodificatore è ottimizzato per la transcodifica anziché per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c433c-104">Specifies whether a decoder is optimized for transcoding rather than for playback.</span></span>

<span data-ttu-id="c433c-105">Attualmente, questo attributo si applica solo ai decodificatori basati su hardware che usano il mini driver AVStream.</span><span class="sxs-lookup"><span data-stu-id="c433c-105">Currently, this attribute applies only to hardware-based decoders that use the AVStream mini-driver.</span></span> <span data-ttu-id="c433c-106">L'attributo viene archiviato nel registro di sistema nelle informazioni sulle funzionalità del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="c433c-106">The attribute is stored in the registry under the decoder's capabilities information.</span></span> <span data-ttu-id="c433c-107">Per ulteriori informazioni, vedere la documentazione relativa a [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="c433c-107">For more information, see the documentation for [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span></span>

<span data-ttu-id="c433c-108">Le applicazioni in genere non utilizzano questo attributo.</span><span class="sxs-lookup"><span data-stu-id="c433c-108">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="c433c-109">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c433c-109">Data type</span></span>

<span data-ttu-id="c433c-110">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c433c-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="c433c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c433c-111">Remarks</span></span>

<span data-ttu-id="c433c-112">Se questa voce del registro di sistema è presente e uguale a 1, la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) ignora il decodificatore, a meno che il chiamante non abbia specificato il flag di **\_ enumerazione MFT \_ flag \_ transcode \_ only** in **MFTEnumEx**.</span><span class="sxs-lookup"><span data-stu-id="c433c-112">If this registry entry is present and equal to 1, the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function skips the decoder unless the caller specified the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in **MFTEnumEx**.</span></span>

<span data-ttu-id="c433c-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c433c-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c433c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c433c-114">Requirements</span></span>



| <span data-ttu-id="c433c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c433c-115">Requirement</span></span> | <span data-ttu-id="c433c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c433c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c433c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c433c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c433c-118">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c433c-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c433c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c433c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c433c-120">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c433c-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c433c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c433c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c433c-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="c433c-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c433c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c433c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c433c-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c433c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c433c-125">**MFTEnumEx**</span><span class="sxs-lookup"><span data-stu-id="c433c-125">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
