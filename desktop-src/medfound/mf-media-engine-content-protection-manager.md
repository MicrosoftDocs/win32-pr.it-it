---
description: Consente al motore multimediale di riprodurre contenuto protetto.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: Attributo MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb99d1df36c9b9adbf1c099d619df60e1144b87
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320550"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a><span data-ttu-id="005b4-103">\_Attributo MF media \_ Engine \_ Content \_ Protection \_ Manager</span><span class="sxs-lookup"><span data-stu-id="005b4-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="005b4-104">Consente al motore multimediale di riprodurre contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="005b4-104">Enables the Media Engine to play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="005b4-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="005b4-105">Data type</span></span>

<span data-ttu-id="005b4-106">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="005b4-106">**IUnknown\***</span></span>

## <a name="remarks"></a><span data-ttu-id="005b4-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="005b4-107">Remarks</span></span>

<span data-ttu-id="005b4-108">Il valore di questo attributo è un puntatore all'interfaccia [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .</span><span class="sxs-lookup"><span data-stu-id="005b4-108">The value of this attribute is a pointer to the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span> <span data-ttu-id="005b4-109">Il chiamante deve implementare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="005b4-109">The caller must implement the interface.</span></span>

<span data-ttu-id="005b4-110">Questo attributo può essere uno degli attributi passati a [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="005b4-110">This attribute can be one of the attributes passed to [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="005b4-111">È necessario se il contenuto protetto deve essere riprodotto.</span><span class="sxs-lookup"><span data-stu-id="005b4-111">It is required if protected content is to be played.</span></span>

## <a name="requirements"></a><span data-ttu-id="005b4-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="005b4-112">Requirements</span></span>



| <span data-ttu-id="005b4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="005b4-113">Requirement</span></span> | <span data-ttu-id="005b4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="005b4-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="005b4-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="005b4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="005b4-116">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="005b4-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="005b4-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="005b4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="005b4-118">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="005b4-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="005b4-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="005b4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="005b4-120"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="005b4-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="005b4-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="005b4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="005b4-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="005b4-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="005b4-123">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="005b4-123">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




