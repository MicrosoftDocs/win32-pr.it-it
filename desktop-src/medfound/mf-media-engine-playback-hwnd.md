---
description: Imposta un handle per una finestra di riproduzione video per il motore multimediale.
ms.assetid: 63889D81-12C5-47C1-B52A-6358E68830C3
title: Attributo MF_MEDIA_ENGINE_PLAYBACK_HWND (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6a9d38d40b04b32244f48289d3334199a7e035
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968878"
---
# <a name="mf_media_engine_playback_hwnd-attribute"></a><span data-ttu-id="030bd-103">\_ \_ \_ Attributo HWND di riproduzione del motore multimediale MF \_</span><span class="sxs-lookup"><span data-stu-id="030bd-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND attribute</span></span>

<span data-ttu-id="030bd-104">Imposta un handle per una finestra di riproduzione video per il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="030bd-104">Sets a handle to a video playback window for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="030bd-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="030bd-105">Data type</span></span>

<span data-ttu-id="030bd-106">**HWND** archiviato come **UInt64**</span><span class="sxs-lookup"><span data-stu-id="030bd-106">**HWND** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="030bd-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="030bd-107">Get/set</span></span>

<span data-ttu-id="030bd-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="030bd-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="030bd-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="030bd-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="remarks"></a><span data-ttu-id="030bd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="030bd-110">Remarks</span></span>

<span data-ttu-id="030bd-111">Questo attributo viene usato con il metodo [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="030bd-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="030bd-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="030bd-112">Requirements</span></span>



| <span data-ttu-id="030bd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="030bd-113">Requirement</span></span> | <span data-ttu-id="030bd-114">Valore</span><span class="sxs-lookup"><span data-stu-id="030bd-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="030bd-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="030bd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="030bd-116">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="030bd-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="030bd-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="030bd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="030bd-118">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="030bd-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="030bd-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="030bd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="030bd-120"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="030bd-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="030bd-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="030bd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="030bd-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="030bd-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




