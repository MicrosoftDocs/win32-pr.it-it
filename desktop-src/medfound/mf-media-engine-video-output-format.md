---
description: Imposta il formato di destinazione di rendering per il motore multimediale.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: Attributo MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761386"
---
# <a name="mf_media_engine_video_output_format-attribute"></a><span data-ttu-id="3be6e-103">\_ \_ \_ Attributo formato video di \_ output del motore multimediale \_ MF</span><span class="sxs-lookup"><span data-stu-id="3be6e-103">MF\_MEDIA\_ENGINE\_VIDEO\_OUTPUT\_FORMAT attribute</span></span>

<span data-ttu-id="3be6e-104">Imposta il formato di destinazione di rendering per il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="3be6e-104">Sets the render-target format for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="3be6e-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3be6e-105">Data type</span></span>

<span data-ttu-id="3be6e-106">**DXGI \_ FORMATO** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3be6e-106">**DXGI\_FORMAT** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3be6e-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="3be6e-107">Remarks</span></span>

<span data-ttu-id="3be6e-108">Impostare questo attributo se si crea il motore multimediale in modalità frame-server.</span><span class="sxs-lookup"><span data-stu-id="3be6e-108">Set this attribute if you create the Media Engine in frame-server mode.</span></span> <span data-ttu-id="3be6e-109">Per altre informazioni, vedere [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="3be6e-109">For more information, see [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="3be6e-110">Il valore dell'attributo è un valore [di \_ formato DXGI](../direct3d9/d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="3be6e-110">The value of the attribute is a [DXGI\_FORMAT](../direct3d9/d3dformat.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3be6e-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3be6e-111">Requirements</span></span>



| <span data-ttu-id="3be6e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3be6e-112">Requirement</span></span> | <span data-ttu-id="3be6e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="3be6e-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3be6e-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3be6e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3be6e-115">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3be6e-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="3be6e-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3be6e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3be6e-117">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="3be6e-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="3be6e-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3be6e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3be6e-119"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="3be6e-119"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be6e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3be6e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be6e-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3be6e-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
