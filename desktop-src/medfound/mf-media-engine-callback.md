---
description: Contiene un puntatore all'interfaccia di callback per il motore multimediale.
ms.assetid: 5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D
title: Attributo MF_MEDIA_ENGINE_CALLBACK (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173e22f9d87f4a77f9ed4a1d1b405fc040bd32b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320549"
---
# <a name="mf_media_engine_callback-attribute"></a><span data-ttu-id="a438a-103">\_Attributo di \_ callback del motore multimediale MF \_</span><span class="sxs-lookup"><span data-stu-id="a438a-103">MF\_MEDIA\_ENGINE\_CALLBACK attribute</span></span>

<span data-ttu-id="a438a-104">Contiene un puntatore all'interfaccia di callback per il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="a438a-104">Contains a pointer to the callback interface for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="a438a-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a438a-105">Data type</span></span>

<span data-ttu-id="a438a-106">**IMFMediaEngineNotify \* *_ archiviato come _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="a438a-106">**IMFMediaEngineNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="a438a-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="a438a-107">Get/set</span></span>

<span data-ttu-id="a438a-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="a438a-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="a438a-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="a438a-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="a438a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a438a-110">Remarks</span></span>

<span data-ttu-id="a438a-111">Il valore di questo attributo è un puntatore all'interfaccia [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) , implementata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a438a-111">The value of this attribute is a pointer to the [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) interface, implemented by the application.</span></span>

<span data-ttu-id="a438a-112">Questo attributo viene usato con il metodo [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="a438a-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="a438a-113">L'attributo è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a438a-113">The attribute is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="a438a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a438a-114">Requirements</span></span>



| <span data-ttu-id="a438a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a438a-115">Requirement</span></span> | <span data-ttu-id="a438a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a438a-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a438a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a438a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a438a-118">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a438a-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="a438a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a438a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a438a-120">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="a438a-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="a438a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a438a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a438a-122"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="a438a-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a438a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a438a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a438a-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a438a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a438a-125">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="a438a-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> <dt>

[<span data-ttu-id="a438a-126">**IMFMediaEngineNotify**</span><span class="sxs-lookup"><span data-stu-id="a438a-126">**IMFMediaEngineNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify)
</dt> </dl>

 

 




