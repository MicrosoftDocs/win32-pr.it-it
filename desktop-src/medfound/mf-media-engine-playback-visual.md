---
description: Imposta un oggetto visivo Microsoft DirectComposition come area di riproduzione per il motore multimediale.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: Attributo MF_MEDIA_ENGINE_PLAYBACK_VISUAL (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320701"
---
# <a name="mf_media_engine_playback_visual-attribute"></a><span data-ttu-id="c36a2-103">\_ \_ \_ Attributo visivo per la riproduzione del motore multimediale \_ MF</span><span class="sxs-lookup"><span data-stu-id="c36a2-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_VISUAL attribute</span></span>

<span data-ttu-id="c36a2-104">Imposta un oggetto visivo Microsoft DirectComposition come area di riproduzione per il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="c36a2-104">Sets a Microsoft DirectComposition visual as the playback region for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="c36a2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c36a2-105">Data type</span></span>

<span data-ttu-id="c36a2-106">**IDCompositionVisual \* *_ archiviato come _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="c36a2-106">**IDCompositionVisual\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="c36a2-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="c36a2-107">Get/set</span></span>

<span data-ttu-id="c36a2-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="c36a2-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="c36a2-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="c36a2-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="c36a2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c36a2-110">Remarks</span></span>

<span data-ttu-id="c36a2-111">Per ulteriori informazioni su DirectComposition, vedere [DirectComposition](../directcomp/directcomposition-portal.md) e [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span><span class="sxs-lookup"><span data-stu-id="c36a2-111">For more information on DirectComposition, see [DirectComposition](../directcomp/directcomposition-portal.md) and [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span></span>

<span data-ttu-id="c36a2-112">Questo attributo viene usato con il metodo [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="c36a2-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="c36a2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c36a2-113">Requirements</span></span>



| <span data-ttu-id="c36a2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c36a2-114">Requirement</span></span> | <span data-ttu-id="c36a2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c36a2-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c36a2-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c36a2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c36a2-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c36a2-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="c36a2-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c36a2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c36a2-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c36a2-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="c36a2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c36a2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c36a2-121"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="c36a2-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c36a2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c36a2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c36a2-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c36a2-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
