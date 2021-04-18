---
description: Imposta Microsoft DirectX Graphics Infrastructure (DXGI) Gestione dispositivi nel motore multimediale.
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: Attributo MF_MEDIA_ENGINE_DXGI_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e731b5aa2449ae772427c6743ec4f97b5d7601
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320484"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a><span data-ttu-id="8b807-103">\_Attributo MF media \_ Engine \_ DXGI \_ Manager</span><span class="sxs-lookup"><span data-stu-id="8b807-103">MF\_MEDIA\_ENGINE\_DXGI\_MANAGER attribute</span></span>

<span data-ttu-id="8b807-104">Imposta Microsoft DirectX Graphics Infrastructure (DXGI) Gestione dispositivi nel motore multimediale.</span><span class="sxs-lookup"><span data-stu-id="8b807-104">Sets the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager on the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="8b807-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8b807-105">Data type</span></span>

<span data-ttu-id="8b807-106">**IMFDXGIDeviceManager \* *_ archiviato come _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="8b807-106">**IMFDXGIDeviceManager\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="8b807-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="8b807-107">Get/set</span></span>

<span data-ttu-id="8b807-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="8b807-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="8b807-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="8b807-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b807-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b807-110">Remarks</span></span>

<span data-ttu-id="8b807-111">Il valore di questo attributo è un puntatore all'interfaccia [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="8b807-111">The value of this attribute is a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="8b807-112">In modalità frame-server questo attributo consente al motore multimediale di usare l'accelerazione hardware per la decodifica video e l'elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="8b807-112">In frame-server mode, this attribute enables the Media Engine to use hardware acceleration for video decoding and video processing.</span></span> <span data-ttu-id="8b807-113">Se l'attributo non è impostato, il motore multimediale usa la decodifica software e l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="8b807-113">If the attribute is not set, the Media Engine uses software decoding and processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b807-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b807-114">Requirements</span></span>



| <span data-ttu-id="8b807-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b807-115">Requirement</span></span> | <span data-ttu-id="8b807-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8b807-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b807-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b807-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8b807-118">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8b807-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="8b807-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b807-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8b807-120">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="8b807-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="8b807-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b807-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b807-122"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b807-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b807-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b807-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b807-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b807-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b807-125">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="8b807-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




