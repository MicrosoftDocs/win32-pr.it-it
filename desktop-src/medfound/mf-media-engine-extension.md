---
description: Contiene un puntatore all'interfaccia IMFMediaEngineExtension.
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: Attributo MF_MEDIA_ENGINE_EXTENSION (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4496b40e9b69091b588ad38ad47d943dce5e1966
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104401830"
---
# <a name="mf_media_engine_extension-attribute"></a><span data-ttu-id="581dd-103">\_Attributo di estensione MF media \_ Engine \_</span><span class="sxs-lookup"><span data-stu-id="581dd-103">MF\_MEDIA\_ENGINE\_EXTENSION attribute</span></span>

<span data-ttu-id="581dd-104">Contiene un puntatore all'interfaccia [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .</span><span class="sxs-lookup"><span data-stu-id="581dd-104">Contains a pointer to the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="581dd-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="581dd-105">Data type</span></span>

<span data-ttu-id="581dd-106">**IMFMediaEngineExtension \* *_ archiviato come _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="581dd-106">**IMFMediaEngineExtension\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="581dd-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="581dd-107">Get/set</span></span>

<span data-ttu-id="581dd-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="581dd-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="581dd-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="581dd-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="581dd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="581dd-110">Remarks</span></span>

<span data-ttu-id="581dd-111">Questo attributo viene usato con il metodo [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="581dd-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="581dd-112">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="581dd-112">This attribute is optional.</span></span> <span data-ttu-id="581dd-113">Usarlo per fornire un oggetto che implementa l'interfaccia [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .</span><span class="sxs-lookup"><span data-stu-id="581dd-113">Use it to provide an object that implements the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span> <span data-ttu-id="581dd-114">Questa interfaccia consente all'applicazione di caricare le risorse multimediali personalizzate.</span><span class="sxs-lookup"><span data-stu-id="581dd-114">This interface enables the application to load custom media resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="581dd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="581dd-115">Requirements</span></span>



| <span data-ttu-id="581dd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="581dd-116">Requirement</span></span> | <span data-ttu-id="581dd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="581dd-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="581dd-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="581dd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="581dd-119">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="581dd-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="581dd-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="581dd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="581dd-121">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="581dd-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="581dd-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="581dd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="581dd-123"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="581dd-123"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="581dd-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="581dd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581dd-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="581dd-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




